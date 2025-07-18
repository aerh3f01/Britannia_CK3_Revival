# ⚙️ Technical Development Guide
*Comprehensive technical documentation for Britannia Expansion development*

---

## 🏗️ Project Architecture

### 📁 File Structure Overview
```
Britannia Expansion/
├── descriptor.mod              # Mod metadata and version info
├── thumbnail.png              # Workshop thumbnail
├── common/                    # Core game mechanics
│   ├── bookmark_portraits/    # Character portraits for bookmarks
│   ├── bookmarks/            # Custom start dates
│   │   ├── bookmarks/        # Bookmark definitions
│   │   └── groups/           # Bookmark group organization
│   ├── coat_of_arms/         # Heraldic designs
│   ├── court_positions/      # Welsh-specific court roles
│   ├── decisions/            # Player decision trees
│   ├── defines/              # Game constant modifications
│   ├── dna_data/            # Character appearance genetics
│   ├── landed_titles/        # Territorial hierarchy
│   ├── scripted_effects/     # Reusable effect scripts
│   ├── scripted_triggers/    # Conditional logic scripts
│   └── struggle/             # Welsh independence struggle system
├── events/                   # Event chain definitions
├── gfx/                     # Graphics and visual assets
│   ├── coat_of_arms/        # Heraldic graphics
│   ├── interface/           # UI elements
│   ├── models/              # 3D model assets
│   └── portraits/           # Character portraits
├── gui/                     # User interface definitions
├── history/                 # Historical starting conditions
│   ├── characters/          # Historical figure definitions
│   ├── cultures/            # Culture setup at game start
│   └── titles/              # Title ownership history
├── localization/            # Text and translations
│   └── replace/english/     # English language files
├── map_data/               # Geographic data
└── music/                  # Audio assets
```

---

## 🔧 Core Systems

### 🏰 Title System (Landed Titles)

#### Welsh Kingdom Structure
```paradox
# File: common/landed_titles/01_be_landed_titles.txt

k_gwynedd = {
    color = { 135 25 3 }                    # Kingdom color on map
    capital = c_cardiganshire               # Kingdom capital
    
    ai_primary_priority = {                 # AI preference logic
        if = {
            limit = { culture = culture:welsh }
            add = @correct_culture_primary_score
        }
    }
    
    can_create = {                          # Creation requirements
        trigger_if = {
            culture = { has_cultural_pillar = heritage_brythonic }
        }
    }
    
    # Duchy definitions within kingdom
    d_gwynedd = {
        color = { 100 0 0 }
        capital = c_cardiganshire
        
        # County definitions within duchy
        c_cardiganshire = {
            color = { 110 10 0 }
            # Barony definitions within county
        }
    }
}
```

#### Technical Considerations
- **Color Consistency**: Welsh kingdoms use red-based color schemes
- **Historical Accuracy**: Capitals match historical seat of power
- **AI Behavior**: Cultural preferences ensure Welsh AI acts appropriately
- **Creation Logic**: Requirements reflect historical unification patterns

### 🎭 Event System

#### Event Structure Template
```paradox
# File: events/be_welsh_kingdom_events.txt

namespace = be_welsh_kingdom

be_welsh_kingdom.1001 = {
    type = character_event                   # Event type
    title = be_welsh_kingdom.1001.t         # Localization key for title
    desc = {                                 # Multiple description options
        desc = be_welsh_kingdom.1001.desc.intro
        triggered_desc = {                   # Conditional descriptions
            trigger = { has_trait = ambitious }
            desc = be_welsh_kingdom.1001.desc.ambitious
        }
    }
    theme = realm                           # Visual theme
    
    left_portrait = {                       # Character portraits
        character = scope:scoped_welsh_king
        animation = personality_honorable    # Character animation
    }
    
    immediate = {                           # Immediate effects
        play_music_cue = "mx_cue_epic_sacral_moment"
        save_scope_as = scoped_welsh_king
        create_welsh_kingdom_scripted_effect = yes
    }
    
    option = {                              # Player choice
        name = be_welsh_kingdom.1001.a      # Option text
        
        # Effects of choosing this option
        add_prestige = 500
        trigger_event = {
            id = be_welsh_kingdom.1002
            days = 30
        }
    }
    
    # Additional options...
}
```

#### Event Design Principles
- **Historical Context**: Each event based on documented history
- **Player Agency**: Meaningful choices with different outcomes
- **Cultural Authenticity**: Welsh values and customs reflected in options
- **Cascading Effects**: Events that trigger future event chains

### ⚖️ Decision System

#### Decision Template
```paradox
# File: common/decisions/01_major_decisions_wales.txt

reunite_the_north_decision = {
    picture = "gfx/interface/illustrations/decisions/decision_realm.dds"
    major = yes                             # Major decision (appears prominently)
    ai_check_interval = 120                 # AI consideration frequency
    desc = reunite_the_north_decision_desc  # Description localization
    
    is_shown = {                            # When decision appears
        game_start_date = 1066.1.1          # Historical date restriction
        culture = culture:welsh              # Cultural requirement
        NOT = { exists = title:k_gwynedd.holder }  # Availability condition
    }
    
    is_valid_showing_failures_only = {      # Validation with error messages
        is_independent_ruler = yes
        is_at_war = no
        custom_description = {               # Custom validation message
            text = needs_welsh_heritage
            culture = { has_cultural_pillar = heritage_brythonic }
        }
    }
    
    effect = {                              # Decision consequences
        show_as_tooltip = {                 # Preview effects
            create_welsh_kingdom_scripted_effect = yes
        }
        trigger_event = {                   # Launch event chain
            id = be_welsh_kingdom.1001
        }
    }
    
    ai_will_do = {                          # AI decision-making logic
        base = 100
        
        modifier = {                        # AI preference modifiers
            factor = 2
            has_trait = ambitious
        }
        
        modifier = {
            factor = 0.5
            is_at_war = yes
        }
    }
}
```

### 🎯 Scripted Effects & Triggers

#### Scripted Effects
```paradox
# File: common/scripted_effects/01_be_kingdom_effects.txt

create_welsh_kingdom_scripted_effect = {
    # Create the Kingdom of Wales title
    create_title = {
        tier = kingdom
        name = k_wales
        holder = this
    }
    
    # Add cultural bonuses
    add_character_modifier = {
        modifier = welsh_unity_bonus
        years = 10
    }
    
    # Trigger vassal reactions
    every_vassal = {
        limit = { culture = culture:welsh }
        add_opinion = {
            target = root
            modifier = unified_wales_opinion
            opinion = 20
        }
    }
    
    # Historical notification
    every_player = {
        trigger_event = {
            id = be_welsh_kingdom.9001  # World notification
        }
    }
}
```

#### Scripted Triggers
```paradox
# File: common/scripted_triggers/01_be_court_position_triggers.txt

is_suitable_welsh_bard_trigger = {
    culture = culture:welsh                  # Cultural requirement
    learning >= 10                          # Skill requirement
    OR = {
        has_trait = poet                     # Relevant traits
        has_trait = scholar
        has_trait = gregarious
    }
    NOT = { has_trait = shy }               # Disqualifying traits
    age >= 16                               # Age requirement
    is_imprisoned = no                      # Availability requirement
}

can_form_kingdom_of_wales_trigger = {
    culture = { has_cultural_pillar = heritage_brythonic }
    completely_controls = title:d_gwynedd
    completely_controls = title:d_powys
    OR = {
        completely_controls = title:d_deheubarth
        any_held_title = {
            tier = duchy
            title_province = { geographical_region = ghw_wales }
        }
    }
    prestige_level >= 3                     # Minimum prestige requirement
}
```

---

## 🎨 Localization System

### 📝 Text File Structure
```yaml
# File: localization/replace/english/be_titles_l_english.yml

l_english:
 # Titles
 k_gwynedd:0 "Kingdom of Gwynedd"
 k_gwynedd_adj:0 "Gwynedd"
 d_gwynedd:0 "Duchy of Gwynedd"
 d_gwynedd_adj:0 "Gwynedd"
 
 # Characters
 owain_gwynedd:0 "Owain Gwynedd"
 owain_gwynedd_nickname:0 "the Great"
 
 # Events
 be_welsh_kingdom.1001.t:0 "The Crown of Wales"
 be_welsh_kingdom.1001.desc.intro:0 "The ancient kingdoms of Wales have long..."
 be_welsh_kingdom.1001.a:0 "A crown worthy of Cadwalader!"
 
 # Decisions
 reunite_the_north_decision:0 "Reunite the Welsh Kingdoms"
 reunite_the_north_decision_desc:0 "The scattered Welsh kingdoms..."
 
 # Custom descriptions
 needs_welsh_heritage:0 "Must be of Welsh heritage"
 unified_wales_opinion:0 "Unified Wales"
```

### 🌍 Localization Best Practices

#### Welsh Language Integration
```yaml
# Authentic Welsh terms with English explanations
pencerdd_court_position:0 "Pencerdd"
pencerdd_court_position_desc:0 "The Pencerdd (Chief Poet) holds the most prestigious..."

# Phonetic guides for non-Welsh speakers
llywelyn_pronunciation:0 "Llywelyn [HLOO-eh-lin]"

# Cultural context explanations
cyfraith_hywel:0 "Cyfraith Hywel (Law of Hywel Dda)"
cyfraith_hywel_tooltip:0 "Traditional Welsh legal system established by Hywel the Good"
```

#### Dynamic Text System
```yaml
# Context-sensitive descriptions
be_kingdom_formation.desc:1 "[CHARACTER.GetFirstName] stands before the assembled Welsh lords..."
be_kingdom_formation.desc:2 "In the shadow of Snowdon, [CHARACTER.GetFirstName] prepares..."

# Conditional text blocks
welsh_victory_notification:0 "[winner.GetTitledFirstName] has achieved a great victory against the [loser.GetCulture.GetName] forces at [county.GetName]!"
```

---

## 🎯 Balance & Gameplay Design

### ⚖️ Power Balance Considerations

#### Welsh Kingdom Strength
```paradox
# Balanced to be competitive but not overpowered
k_gwynedd = {
    # Moderate income base
    tax_mult = 1.0
    levy_mult = 1.1                         # Slight military advantage
    
    # Cultural bonuses
    culture = {
        martial_custom = martial_custom_mountain_warriors
        traditions = {
            tradition_hill_dwellers
            tradition_longbow_competitions
            tradition_poetry_competitions
        }
    }
}
```

#### Cultural Advantages & Disadvantages
```paradox
welsh_mountain_bonus = {
    supply_limit_mult = 0.1                 # Lower supply in mountains
    garrison_size = 0.2                     # Better castle defense
    hostile_county_attrition = 0.15        # Attrition for invaders
}

welsh_diplomatic_penalty = {
    same_culture_opinion = 10               # Welsh unity
    different_culture_opinion = -5         # Suspicion of foreigners
}
```

### 🎮 Player Experience Design

#### Progression Arcs
1. **Early Game**: Uniting fragmented Welsh kingdoms
2. **Mid Game**: Resisting Norman expansion
3. **Late Game**: Welsh cultural renaissance or English integration

#### Meaningful Choices
- **Cultural Preservation vs. Adaptation**: Maintain traditions or modernize
- **Independence vs. Accommodation**: Resist or work with English overlords
- **Military vs. Diplomatic**: Warrior culture or political maneuvering
- **Religious Path**: Celtic Christianity vs. Roman Catholicism

---

## 🐛 Testing & Quality Assurance

### 🧪 Testing Framework

#### Automated Testing Checklist
```
□ Mod loads without errors
□ All events trigger correctly
□ Decision logic functions properly
□ AI behavior performs as expected
□ No script errors in logs
□ Localization keys all resolve
□ Graphics load properly
□ Performance impact acceptable
```

#### Historical Accuracy Testing
```
□ Character dates and lifespans accurate
□ Geographic locations historically correct
□ Cultural practices authentically represented
□ Timeline of events follows historical record
□ Cause-and-effect relationships logical
□ Alternative history paths plausible
```

#### Gameplay Balance Testing
```
□ Welsh kingdoms competitive with neighbors
□ Player choices have meaningful consequences
□ AI Welsh rulers behave appropriately
□ Economic balance maintained
□ Military strength appropriate
□ Cultural bonuses significant but not overpowered
```

### 📊 Performance Monitoring

#### Script Performance
```paradox
# Efficient scripting practices
every_county = {
    limit = { 
        culture = culture:welsh          # Narrow scope early
        county_opinion <= 0             # Specific conditions
    }
    # Minimal operations within loop
}

# Avoid expensive operations in frequently called events
trigger_event = {
    id = be_performance_check.0001
    days = { 365 730 }                  # Yearly events only
}
```

#### Memory Management
- **Scope Management**: Properly save and clear character scopes
- **Event Cleanup**: Remove temporary modifiers and flags
- **Trigger Optimization**: Use most restrictive conditions first
- **Loop Efficiency**: Minimize operations within large loops

---

## 🔄 Version Control & Release Management

### 📦 Release Process

#### Version Numbering
- **Major Versions** (1.0, 2.0): New culture additions
- **Minor Versions** (1.1, 1.2): Feature additions within culture
- **Patch Versions** (1.1.1): Bug fixes and balance adjustments

#### Pre-Release Checklist
```
□ All code reviewed and tested
□ Historical accuracy verified
□ Localization complete and proofread
□ Steam Workshop description updated
□ Changelog documented
□ Compatibility tested with latest CK3
□ Performance impact assessed
□ Community feedback incorporated
```

### 🔀 Branching Strategy
```
main                    # Stable release branch
├── develop            # Integration branch for features
├── feature/events     # Event development
├── feature/decisions  # Decision system work
├── hotfix/1.1.1      # Critical bug fixes
└── research/scotland  # Future culture research
```

### 📋 Issue Management

#### Bug Report Template
```markdown
**Bug Description**: Clear description of the issue
**Steps to Reproduce**: Step-by-step reproduction
**Expected Behavior**: What should happen
**Actual Behavior**: What actually happens
**CK3 Version**: Game version number
**Mod Version**: Britannia Expansion version
**Save File**: Attached if possible
**Screenshots**: Visual evidence
```

#### Feature Request Template
```markdown
**Feature Description**: Detailed feature explanation
**Historical Basis**: Historical sources and context
**Gameplay Impact**: How it would affect player experience
**Implementation Ideas**: Suggested technical approach
**Priority Level**: High/Medium/Low importance
**Cultural Significance**: Why it matters for Welsh culture
```

---

## 🚀 Deployment & Distribution

### 📤 Steam Workshop Deployment

#### Workshop Metadata
```ini
# descriptor.mod
version="1.1.0"
tags={
    "Historical"
    "Culture"
    "Events"
    "Gameplay"
    "Utilities"
}
name="Britannia Expansion"
picture="thumbnail.png"
supported_version="1.9.*.*"
remote_file_id="2979045549"
```

#### Deployment Process
1. **Testing**: Comprehensive testing on multiple save files
2. **Documentation**: Update all documentation files
3. **Workshop**: Upload to Steam Workshop with detailed description
4. **GitHub**: Tag release with version number
5. **Community**: Announce in community channels
6. **Monitor**: Watch for bug reports and feedback

### 📱 Community Communication

#### Update Announcements
```markdown
# Britannia Expansion v1.1 - Welsh Events & Resistance

## New Features
- 🎭 12 new Welsh resistance events (1067-1136)
- ⚔️ Norman invasion event chains
- 🏰 Enhanced Welsh military traditions
- 📜 Historical figure improvements

## Bug Fixes
- Fixed issue with Welsh kingdom formation
- Corrected character birth dates
- Improved AI decision-making

## Compatibility
- Full compatibility with CK3 v1.9.*
- Save game compatible (new features require new game)
```

---

<div align="center">
  <p><strong>⚙️ Technical excellence in service of historical authenticity ⚙️</strong></p>
  <p><em>This guide ensures consistent, high-quality development practices for the Britannia Expansion project.</em></p>
  
  <p>
    <a href="README.md">← Back to Main Documentation</a> •
    <a href="CONTRIBUTING.md">Contributing Guidelines</a> •
    <a href="roadmap.md">Development Roadmap</a>
  </p>
</div>
