# ⚔️ Welsh Historical Events Database
*Comprehensive chronological events for Britannia Expansion (867-1453)*

---

## 📅 Event Structure & Implementation

### 🎯 Event Categories
- **Political Events**: Royal succession, kingdom formation, diplomatic relations
- **Military Events**: Battles, conquests, rebellions, raids
- **Cultural Events**: Religious ceremonies, artistic achievements, legal reforms
- **Social Events**: Court gatherings, marriages, family dynamics
- **Economic Events**: Trade developments, resource management, territorial changes
- **Religious Events**: Ecclesiastical appointments, monastery foundations, pilgrimages

### 🔧 Technical Implementation
Each event includes:
- **Historical Date**: Exact year/season when possible
- **Primary Characters**: Key figures involved
- **Prerequisites**: Political/cultural conditions required
- **Multiple Outcomes**: Historical and alternative history paths
- **Cascading Effects**: Events triggered by outcomes
- **Cultural Impact**: Effect on Welsh identity and unity

---

## 🏰 Early Medieval Period (867-1066)

### 📊 Timeline Overview
This period establishes the foundation of medieval Welsh kingdoms and their relationships with Viking raiders, Anglo-Saxon England, and each other.

### 🎭 Key Events

#### **878 - The Viking Raids Begin**
**Event ID**: `be_early_wales.0001`
**Historical Context**: Viking raids along Welsh coasts intensify
**Primary Characters**: Local Welsh rulers, Viking war leaders
**Trigger Conditions**: 
- Date: 878.3.15 (Spring)
- Coastal Welsh counties
- Viking activity in Irish Sea

**Event Chain**:
```
Option A: "Fortify our coastal settlements"
→ Gain defensive bonuses, lose gold
→ Follow-up: Coastal defense events

Option B: "Negotiate with the raiders"
→ Pay tribute, gain temporary peace
→ Follow-up: Diplomatic complications

Option C: "Rally our warriors for counterattack"
→ Military confrontation
→ Follow-up: Victory/defeat consequences
```

**Historical Outcome**: Mixed resistance and accommodation
**Game Impact**: Establishes Viking relationship mechanics

#### **895 - The Assembly of Gwynedd**
**Event ID**: `be_early_wales.0015`
**Historical Context**: Welsh kingdoms discuss united response to threats
**Primary Characters**: Kings of Gwynedd, Powys, Deheubarth
**Trigger Conditions**:
- Date: 895.6.1 (Summer)
- Multiple Welsh kingdoms exist
- External threat level high

**Event Chain**:
```
Option A: "We must unite against our enemies"
→ Temporary alliance bonus
→ Follow-up: Joint military campaigns

Option B: "Each kingdom must guard its own"
→ Maintain independence
→ Follow-up: Individual defense events

Option C: "Let us elect a High King"
→ Attempt at Welsh unification
→ Follow-up: Succession disputes
```

**Historical Outcome**: Limited cooperation, maintained independence
**Game Impact**: Early Welsh unity mechanics

#### **942 - The Laws of Hywel Dda**
**Event ID**: `be_early_wales.0032`
**Historical Context**: Hywel Dda codifies Welsh law
**Primary Characters**: Hywel Dda, legal scholars, nobility
**Trigger Conditions**:
- Date: 942.9.15 (Autumn)
- Hywel Dda rules significant Welsh territory
- High learning skill or scholarly advisor

**Event Chain**:
```
Option A: "These laws will unite all Welsh people"
→ Legal unity bonus, cultural prestige
→ Follow-up: Legal reform implementation

Option B: "We must preserve local customs too"
→ Balanced approach, regional variations
→ Follow-up: Regional legal disputes

Option C: "Why change the old ways?"
→ Resist legal reform
→ Follow-up: Traditional vs. modern conflicts
```

**Historical Outcome**: Comprehensive legal code established
**Game Impact**: Unlocks Welsh legal decisions and cultural bonuses

---

## ⚔️ Norman Conquest Period (1066-1100)

### 📊 Timeline Overview
Critical period where Welsh kingdoms face Norman expansion while adapting to the post-Conquest political landscape.

### 🎭 Major Event Chains

#### **1067 - The Herefordshire Campaign**
**Event ID**: `be_norman_period.1067`
**Historical Context**: Welsh kingdoms raid English border territories
**Primary Characters**: Bleddyn ap Cynfyn, Rhiwallon ap Cynfyn, Eadric the Wild
**Trigger Conditions**:
- Date: 1067.8.20 (Late Summer)
- Welsh ruler controls border territory
- Norman conquest of England completed

**Event Chain**:
```
Main Event: "The Border Beckons"
→ Option A: "Strike while the Normans consolidate"
  → Successful raid: Gain gold, prestige, territory
  → Failed raid: Lose prestige, face retaliation
  
→ Option B: "Wait and watch the situation"
  → Diplomatic complications with Normans
  → Follow-up: Norman pressure events
  
→ Option C: "Offer alliance to Saxon rebels"
  → Joint rebellion against Normans
  → Follow-up: Alliance management events
```

**Cascading Events**:
- `be_norman_period.1068` - Norman Retaliation
- `be_norman_period.1069` - Saxon Alliance Consequences
- `be_norman_period.1070` - Border Fortification Decisions

#### **1081 - Gruffydd ap Cynan's Return**
**Event ID**: `be_norman_period.1081`
**Historical Context**: Gruffydd ap Cynan attempts to reclaim Gwynedd throne
**Primary Characters**: Gruffydd ap Cynan, Trahaearn ap Caradog, Robert of Rhuddlan
**Trigger Conditions**:
- Date: 1081.5.15 (Spring)
- Gwynedd throne disputed
- Character has valid claim

**Event Chain**:
```
Main Event: "The Exile's Return"
→ Option A: "I am the rightful king of Gwynedd"
  → Civil war begins
  → Follow-up: Legitimacy struggles
  
→ Option B: "Let us negotiate a peaceful solution"
  → Diplomatic resolution attempt
  → Follow-up: Power-sharing arrangements
  
→ Option C: "The time is not yet right"
  → Delay claim, build support
  → Follow-up: Preparation and alliance events
```

**Cascading Events**:
- `be_norman_period.1082` - The Battle for Gwynedd
- `be_norman_period.1083` - Norman Intervention
- `be_norman_period.1084` - Irish Sea Politics

#### **1093 - The Death of Rhys ap Tewdwr**
**Event ID**: `be_norman_period.1093`
**Historical Context**: Last independent king of Deheubarth dies fighting Normans
**Primary Characters**: Rhys ap Tewdwr, Norman knights, Deheubarth nobility
**Trigger Conditions**:
- Date: 1093.4.10 (Spring)
- Rhys ap Tewdwr rules Deheubarth
- Norman pressure in South Wales

**Event Chain**:
```
Main Event: "The Last Stand of Deheubarth"
→ Option A: "We die as free Welshmen!"
  → Heroic last battle
  → Follow-up: Martyrdom and resistance inspiration
  
→ Option B: "Perhaps terms can be negotiated"
  → Attempt diplomatic solution
  → Follow-up: Vassal status complications
  
→ Option C: "Retreat to fight another day"
  → Strategic withdrawal
  → Follow-up: Guerrilla resistance events
```

**Cascading Events**:
- `be_norman_period.1094` - The Norman Conquest of South Wales
- `be_norman_period.1095` - Deheubarth Resistance Movement
- `be_norman_period.1096` - Welsh Unity Crisis

---

## 🏰 High Medieval Period (1100-1282)

### 📊 Timeline Overview
Period of Welsh renaissance, territorial expansion, and ultimate confrontation with Plantagenet England.

### 🎭 Major Event Chains

#### **1136 - The Great Welsh Uprising**
**Event ID**: `be_high_medieval.1136`
**Historical Context**: Coordinated Welsh rebellion against Norman rule
**Primary Characters**: Owain Gwynedd, Gruffydd ap Rhys, Morgan ab Owain
**Trigger Conditions**:
- Date: 1136.1.1 (New Year)
- Multiple Welsh rulers under Norman pressure
- Stephen's civil war in England

**Event Chain**:
```
Main Event: "The Year of Liberty"
→ Option A: "All Wales must rise as one!"
  → Coordinated rebellion
  → Follow-up: Inter-Welsh coordination challenges
  
→ Option B: "Each kingdom for itself"
  → Independent risings
  → Follow-up: Isolated resistance struggles
  
→ Option C: "Wait for English weakness to increase"
  → Delayed response
  → Follow-up: Missed opportunity consequences
```

**Cascading Events**:
- `be_high_medieval.1137` - The Liberation of Ceredigion
- `be_high_medieval.1138` - Norman Counter-Offensive
- `be_high_medieval.1139` - Welsh Territorial Gains

#### **1157 - Henry II's Welsh Campaign**
**Event ID**: `be_high_medieval.1157`
**Historical Context**: Henry II attempts to reassert English control over Wales
**Primary Characters**: Henry II, Owain Gwynedd, Madog ap Maredudd
**Trigger Conditions**:
- Date: 1157.7.15 (Summer)
- Henry II consolidates English power
- Welsh territorial expansion threatens English interests

**Event Chain**:
```
Main Event: "The Plantagenet Intervention"
→ Option A: "We will resist with all our strength"
  → Military confrontation
  → Follow-up: Battle of Ewloe events
  
→ Option B: "Submit to preserve our people"
  → Diplomatic submission
  → Follow-up: Vassal relationship management
  
→ Option C: "Negotiate from a position of strength"
  → Strategic diplomacy
  → Follow-up: Treaty negotiation events
```

**Cascading Events**:
- `be_high_medieval.1158` - The Battle of Ewloe
- `be_high_medieval.1159` - Welsh Diplomatic Strategy
- `be_high_medieval.1160` - Henry's Welsh Settlement

#### **1165 - The Battle of Crogen**
**Event ID**: `be_high_medieval.1165`
**Historical Context**: Welsh forces decisively defeat Henry II's invasion
**Primary Characters**: Owain Gwynedd, Rhys ap Gruffydd, Henry II
**Trigger Conditions**:
- Date: 1165.8.10 (Summer)
- Henry II launches major Welsh campaign
- Welsh alliance formed

**Event Chain**:
```
Main Event: "Victory in the Mountains"
→ Option A: "Press our advantage against the English"
  → Pursue retreating English army
  → Follow-up: Welsh territorial expansion
  
→ Option B: "Consolidate our victory"
  → Strengthen defenses
  → Follow-up: Diplomatic negotiations
  
→ Option C: "Seek immediate peace"
  → Quick diplomatic resolution
  → Follow-up: Terms negotiation
```

**Cascading Events**:
- `be_high_medieval.1166` - Welsh Ascendancy
- `be_high_medieval.1167` - Henry's Withdrawal
- `be_high_medieval.1168` - Welsh Independence Confirmed

#### **1176 - The First National Eisteddfod**
**Event ID**: `be_high_medieval.1176`
**Historical Context**: Rhys ap Gruffydd hosts first national poetry competition
**Primary Characters**: Rhys ap Gruffydd, Welsh bards, cultural leaders
**Trigger Conditions**:
- Date: 1176.12.25 (Christmas)
- Rhys ap Gruffydd controls Cardigan
- Welsh cultural renaissance underway

**Event Chain**:
```
Main Event: "A Festival of Welsh Arts"
→ Option A: "Let all Wales celebrate our culture"
  → Grand cultural festival
  → Follow-up: Cultural unity bonuses
  
→ Option B: "Honor our greatest poets and musicians"
  → Elite cultural event
  → Follow-up: Artistic patronage
  
→ Option C: "Include foreign artists as well"
  → International cultural exchange
  → Follow-up: Diplomatic cultural benefits
```

**Cascading Events**:
- `be_high_medieval.1177` - Cultural Renaissance
- `be_high_medieval.1178` - Bardic Traditions Formalized
- `be_high_medieval.1179` - Welsh Identity Strengthened

#### **1267 - The Treaty of Montgomery**
**Event ID**: `be_high_medieval.1267`
**Historical Context**: Henry III recognizes Llywelyn ap Gruffydd as Prince of Wales
**Primary Characters**: Llywelyn ap Gruffydd, Henry III, English negotiators
**Trigger Conditions**:
- Date: 1267.9.29 (Autumn)
- Llywelyn controls most of Wales
- English civil war creates opportunity

**Event Chain**:
```
Main Event: "The Prince of Wales Recognized"
→ Option A: "Accept the title and its terms"
  → Official recognition as Prince of Wales
  → Follow-up: Tribute and vassalage obligations
  
→ Option B: "Demand better terms"
  → Negotiate improved conditions
  → Follow-up: Diplomatic complications
  
→ Option C: "Reject English overlordship entirely"
  → Maintain independence claim
  → Follow-up: Continued conflict
```

**Cascading Events**:
- `be_high_medieval.1268` - Welsh Principality Established
- `be_high_medieval.1269` - Tribute and Homage Issues
- `be_high_medieval.1270` - Welsh Administrative Reforms

---

## 🗡️ Conquest Period (1276-1295)

### 📊 Timeline Overview
Edward I's systematic conquest of Wales and the end of Welsh independence.

### 🎭 Major Event Chains

#### **1276 - Edward I's First Welsh War**
**Event ID**: `be_conquest.1276`
**Historical Context**: Edward I begins systematic conquest of Wales
**Primary Characters**: Edward I, Llywelyn ap Gruffydd, Dafydd ap Gruffydd
**Trigger Conditions**:
- Date: 1276.11.12 (Late Autumn)
- Edward I consolidates English crown
- Welsh tribute disputes

**Event Chain**:
```
Main Event: "The Plantagenet Conquest Begins"
→ Option A: "We will fight for every valley and hill"
  → Total resistance strategy
  → Follow-up: Guerrilla warfare events
  
→ Option B: "Seek negotiated settlement"
  → Diplomatic resistance
  → Follow-up: Terms negotiation
  
→ Option C: "Preserve what we can"
  → Strategic withdrawal
  → Follow-up: Selective resistance
```

**Cascading Events**:
- `be_conquest.1277` - The Siege of Dolforwyn
- `be_conquest.1278` - Edward's Castle Building
- `be_conquest.1279` - Welsh Territorial Losses

#### **1282 - The Final Welsh War**
**Event ID**: `be_conquest.1282`
**Historical Context**: Dafydd ap Gruffydd's rebellion triggers final conquest
**Primary Characters**: Llywelyn ap Gruffydd, Dafydd ap Gruffydd, Edward I
**Trigger Conditions**:
- Date: 1282.3.22 (Spring)
- Dafydd starts rebellion
- Llywelyn decides response

**Event Chain**:
```
Main Event: "The Last War of Independence"
→ Option A: "Support my brother's rebellion"
  → Join the final war
  → Follow-up: Last stand events
  
→ Option B: "Try to restrain the situation"
  → Diplomatic intervention
  → Follow-up: Family conflict
  
→ Option C: "Distance myself from this folly"
  → Abandon the rebellion
  → Follow-up: Political isolation
```

**Cascading Events**:
- `be_conquest.1283` - The Death of Llywelyn
- `be_conquest.1284` - The Execution of Dafydd
- `be_conquest.1285` - Welsh Submission

#### **1284 - The Statute of Rhuddlan**
**Event ID**: `be_conquest.1284`
**Historical Context**: Edward I establishes English administration in Wales
**Primary Characters**: Edward I, Welsh nobility, English administrators
**Trigger Conditions**:
- Date: 1284.3.19 (Spring)
- Welsh conquest completed
- Edward I organizes new administration

**Event Chain**:
```
Main Event: "The New Order"
→ Option A: "Accept the new system for survival"
  → Collaboration with English rule
  → Follow-up: Administrative integration
  
→ Option B: "Preserve Welsh customs where possible"
  → Cultural resistance
  → Follow-up: Underground preservation
  
→ Option C: "Plan for future resistance"
  → Secret organization
  → Follow-up: Conspiracy events
```

**Cascading Events**:
- `be_conquest.1285` - Welsh Administrative Integration
- `be_conquest.1286` - Cultural Suppression Policies
- `be_conquest.1287` - Underground Welsh Networks

---

## 🔥 Rebellion Period (1400-1415)

### 📊 Timeline Overview
Owain Glyndŵr's rebellion represents the last great Welsh independence movement.

### 🎭 Major Event Chains

#### **1400 - The Glyndŵr Rebellion Begins**
**Event ID**: `be_rebellion.1400`
**Historical Context**: Owain Glyndŵr proclaims himself Prince of Wales
**Primary Characters**: Owain Glyndŵr, Henry IV, Reginald Grey
**Trigger Conditions**:
- Date: 1400.9.16 (Autumn)
- Land dispute with Reginald Grey
- Welsh grievances accumulated

**Event Chain**:
```
Main Event: "The Last Prince of Wales"
→ Option A: "Proclaim myself Prince of Wales"
  → Begin full rebellion
  → Follow-up: Raising Welsh support
  
→ Option B: "Seek legal redress first"
  → Legal challenges to English rule
  → Follow-up: Court proceedings
  
→ Option C: "Rally support before acting"
  → Build coalition
  → Follow-up: Alliance building
```

**Cascading Events**:
- `be_rebellion.1401` - The Spread of Rebellion
- `be_rebellion.1402` - The Battle of Bryn Glas
- `be_rebellion.1403` - French Alliance Negotiations

#### **1404 - The Pennal Letter**
**Event ID**: `be_rebellion.1404`
**Historical Context**: Glyndŵr seeks French support and papal recognition
**Primary Characters**: Owain Glyndŵr, Charles VI of France, Pope Benedict XIII
**Trigger Conditions**:
- Date: 1404.3.31 (Spring)
- Glyndŵr controls significant Welsh territory
- French-English conflicts ongoing

**Event Chain**:
```
Main Event: "The Welsh Alliance Strategy"
→ Option A: "Seek formal French alliance"
  → International diplomacy
  → Follow-up: French military support
  
→ Option B: "Appeal to the Avignon Pope"
  → Religious legitimacy
  → Follow-up: Ecclesiastical support
  
→ Option C: "Focus on Scottish connections"
  → Celtic alliance
  → Follow-up: Scottish military aid
```

**Cascading Events**:
- `be_rebellion.1405` - French Expeditionary Force
- `be_rebellion.1406` - Welsh Parliamentary Assembly
- `be_rebellion.1407` - International Recognition

#### **1409 - The Rebellion's Decline**
**Event ID**: `be_rebellion.1409`
**Historical Context**: English counter-offensive begins to succeed
**Primary Characters**: Owain Glyndŵr, Henry IV, Prince Henry (future Henry V)
**Trigger Conditions**:
- Date: 1409.6.15 (Summer)
- English pressure increasing
- Welsh territorial losses mounting

**Event Chain**:
```
Main Event: "The Tide Turns"
→ Option A: "Fight to the bitter end"
  → Guerrilla warfare continuation
  → Follow-up: Mountain resistance
  
→ Option B: "Seek honorable terms"
  → Negotiated settlement
  → Follow-up: Pardon negotiations
  
→ Option C: "Disappear into the mountains"
  → Legendary disappearance
  → Follow-up: Folk hero status
```

**Cascading Events**:
- `be_rebellion.1410` - The Last Strongholds
- `be_rebellion.1411` - Glyndŵr's Disappearance
- `be_rebellion.1412` - Welsh Cultural Suppression

---

## ⛪ Religious and Cultural Events

### 🎭 Religious Event Chains

#### **1120 - The Foundation of Margam Abbey**
**Event ID**: `be_religious.1120`
**Historical Context**: Cistercian monastery established in Glamorgan
**Primary Characters**: Robert, Earl of Gloucester, Cistercian monks
**Trigger Conditions**:
- Date: 1120.5.25 (Spring)
- Norman lord controls territory
- Religious patronage decision

**Event Chain**:
```
Main Event: "A New Monastery"
→ Option A: "Support the Cistercian reform"
  → Found major monastery
  → Follow-up: Religious influence growth
  
→ Option B: "Maintain Welsh religious traditions"
  → Support Celtic monasticism
  → Follow-up: Cultural preservation
  
→ Option C: "Balance both approaches"
  → Diplomatic religious policy
  → Follow-up: Religious harmony
```

#### **1188 - Gerald of Wales Tours Wales**
**Event ID**: `be_religious.1188`
**Historical Context**: Giraldus Cambrensis preaches Third Crusade in Wales
**Primary Characters**: Gerald of Wales, Baldwin of Exeter, Welsh nobility
**Trigger Conditions**:
- Date: 1188.3.1 (Spring)
- Third Crusade proclaimed
- Gerald of Wales active

**Event Chain**:
```
Main Event: "The Crusade Preacher"
→ Option A: "Take the cross for the Holy Land"
  → Join Third Crusade
  → Follow-up: Crusading preparations
  
→ Option B: "Wales needs its defenders at home"
  → Refuse crusade call
  → Follow-up: Local priorities
  
→ Option C: "Send representatives but stay"
  → Compromise position
  → Follow-up: Diplomatic balance
```

### 🎨 Cultural Event Chains

#### **1194 - The Laws of Hywel Dda Revised**
**Event ID**: `be_cultural.1194`
**Historical Context**: Welsh legal scholars update traditional law codes
**Primary Characters**: Welsh legal scholars, Prince/King, court officials
**Trigger Conditions**:
- Date: 1194.11.11 (Autumn)
- Welsh ruler with legal reform ambitions
- High learning skill or scholarly advisor

**Event Chain**:
```
Main Event: "Updating Ancient Laws"
→ Option A: "Modernize while preserving tradition"
  → Legal reform with cultural continuity
  → Follow-up: Legal modernization benefits
  
→ Option B: "Preserve the old ways exactly"
  → Traditional legal conservation
  → Follow-up: Cultural purity bonuses
  
→ Option C: "Adopt some English legal practices"
  → Legal syncretism
  → Follow-up: Administrative efficiency
```

---

## 🎯 Event Implementation Guide

### 📊 Event Mechanics

#### **Trigger Systems**
- **Date-based**: Historical accuracy for major events
- **Condition-based**: Political situations, character traits, relationships
- **Random factors**: Historical uncertainty and player agency
- **Cascading triggers**: Events that spawn from previous events

#### **Multiple Outcomes**
- **Historical Path**: What actually happened in history
- **Alternative Paths**: Plausible alternative outcomes
- **Player Agency**: Meaningful choices affecting future events
- **Cultural Impact**: Effects on Welsh identity and unity

#### **Character Integration**
- **Primary Characters**: Historical figures central to events
- **Supporting Characters**: Court members, family, advisors
- **Relationship Effects**: How events affect character relationships
- **Trait Development**: Events that can modify character traits

### 🎨 Localization Requirements

#### **Event Text Structure**
```yaml
# Event Title
be_event.####.t: "Historical Event Title"

# Event Description
be_event.####.desc: "Detailed historical context and current situation..."

# Option Texts
be_event.####.a: "Historical choice option"
be_event.####.b: "Alternative choice option" 
be_event.####.c: "Player agency option"

# Flavor Text
be_event.####.flavor: "Additional atmospheric text"

# Conditional Text
be_event.####.desc_ambitious: "Text for ambitious characters"
```

#### **Cultural Authenticity**
- **Welsh terminology**: Proper use of Welsh titles and concepts
- **Historical accuracy**: Verified historical information
- **Cultural context**: Understanding of medieval Welsh society
- **Period language**: Appropriate tone and terminology

---

<div align="center">
  <p><strong>⚔️ These events bring Welsh medieval history to life in CK3 ⚔️</strong></p>
  <p><em>Each event is grounded in historical evidence while providing meaningful player choices and authentic cultural experiences.</em></p>
</div>
