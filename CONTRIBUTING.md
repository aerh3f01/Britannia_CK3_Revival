# 🔧 Contributing to Britannia Expansion
*Guidelines for contributing to the Welsh-focused CK3 modification*

---

## 🎯 How to Contribute

We welcome contributions from historians, modders, players, and anyone passionate about Welsh culture and medieval history. There are many ways to help improve Britannia Expansion!

---

## 📚 Types of Contributions

### 🔬 Historical Research
**Help ensure historical accuracy and cultural authenticity**

#### Primary Sources
- Welsh chronicles (Brut y Tywysogion, Brut y Saeson)
- Legal texts (Laws of Hywel Dda)
- Religious manuscripts and saints' lives
- Archaeological evidence and reports

#### Academic Resources
- Peer-reviewed historical studies
- University dissertations on Welsh medieval history
- Museum archives and collections
- Expert consultations with medieval historians

#### Cultural Knowledge
- Welsh language expertise for authentic naming
- Traditional cultural practices and customs
- Folklore and mythology integration
- Modern Welsh cultural perspectives on historical representation

### 💻 Technical Development

#### Code Contributions
- Bug fixes and technical improvements
- New event chains and decision trees
- Enhanced game mechanics
- Performance optimizations

#### Localization
- Welsh language translations
- Other language support
- Cultural context explanations
- Historical annotation for events

#### Graphics & Design
- Historical Welsh heraldry and coat of arms
- Period-appropriate interface elements
- Character portraits and clothing
- Map enhancements and geographical accuracy

### 🎮 Testing & Quality Assurance

#### Gameplay Testing
- Balance testing for competitive play
- Event chain verification
- Bug discovery and reporting
- User experience feedback

#### Historical Validation
- Fact-checking historical events
- Cultural authenticity verification
- Timeline accuracy confirmation
- Character behavior validation

---

## 🏗️ Development Setup

### Prerequisites
- **Crusader Kings 3**: Latest version required
- **Git**: For version control
- **Text Editor**: VS Code, Notepad++, or similar
- **CK3 Modding Knowledge**: Basic understanding helpful

### Getting Started

#### 1. Fork the Repository
```bash
# Clone your fork
git clone https://github.com/yourusername/Britannia_CK3_Revival.git
cd Britannia_CK3_Revival
```

#### 2. Set Up Development Environment
- Install CK3 in default location
- Enable CK3 Developer Mode
- Set up mod folder symbolic links
- Configure debugging tools

#### 3. Understanding the Codebase
```
Britannia Expansion/
├── common/                 # Core game mechanics
│   ├── decisions/         # Player decision options
│   ├── events/           # Scripted event chains  
│   ├── landed_titles/    # Kingdom and duchy definitions
│   └── cultures/         # Welsh culture mechanics
├── history/              # Historical starting conditions
├── localization/         # Text and language files
└── gfx/                 # Graphics and visual assets
```

---

## 📝 Contribution Guidelines

### 🎯 Historical Accuracy Standards

#### Source Requirements
- **Primary Sources**: Medieval documents preferred
- **Academic Sources**: Peer-reviewed historical studies
- **Archaeological Evidence**: Material culture findings
- **Expert Consultation**: Professional historian review when possible

#### Cultural Sensitivity
- Respectful representation of Welsh culture
- Avoiding stereotypes and misconceptions
- Consulting Welsh cultural experts
- Balancing historical accuracy with gameplay

### 💻 Code Standards

#### File Organization
```
# Event files
events/be_[category]_events.txt

# Decision files  
decisions/[major|minor]_decisions_[culture].txt

# Localization
localization/replace/english/[category]_l_english.yml
```

#### Naming Conventions
- **Events**: `be_category.####` (e.g., `be_welsh_kingdom.1001`)
- **Decisions**: `descriptive_name_decision`
- **Variables**: `snake_case_naming`
- **Triggers**: `descriptive_trigger_name`

#### Code Documentation
```paradox
# Historical Context: Brief explanation of historical basis
# Gameplay Impact: What this changes for the player
# Balance Considerations: Why this is balanced

event_name = {
    # Event code with clear comments
}
```

### 🌐 Localization Standards

#### Text Guidelines
- **Historical Language**: Period-appropriate terminology
- **Cultural Authenticity**: Welsh terms where appropriate
- **Clear Communication**: Understandable for modern players
- **Immersive Tone**: Maintaining medieval atmosphere

#### Welsh Language Integration
- Accurate Welsh spelling and pronunciation
- Cultural context for Welsh terms
- English explanations when needed
- Consultation with Welsh speakers

---

## 🔄 Contribution Process

### 📋 Before Starting

#### 1. Check Existing Issues
- Review [GitHub Issues](https://github.com/aerh3f01/Britannia_CK3_Revival/issues)
- Check [Project Roadmap](roadmap.md)
- Discuss major changes in [Discussions](https://github.com/aerh3f01/Britannia_CK3_Revival/discussions)

#### 2. Create an Issue
- Describe your proposed contribution
- Provide historical context and sources
- Discuss implementation approach
- Get feedback before starting work

### 🔧 Development Process

#### 1. Create Feature Branch
```bash
git checkout -b feature/your-feature-name
```

#### 2. Make Changes
- Follow coding standards
- Include historical documentation
- Test thoroughly
- Write clear commit messages

#### 3. Document Changes
- Update relevant documentation
- Add historical context notes
- Include testing information
- Update changelog if needed

### 📤 Submitting Changes

#### 1. Prepare Pull Request
- **Title**: Clear, descriptive summary
- **Description**: Detailed explanation of changes
- **Historical Context**: Sources and justification
- **Testing**: How you verified the changes work

#### 2. Pull Request Review
- Maintainer review for historical accuracy
- Community feedback on gameplay impact
- Technical review for code quality
- Integration testing with existing features

#### 3. Incorporation
- Address any feedback
- Make requested changes
- Final approval and merge
- Credit in contributors list

---

## 🎓 Research Guidelines

### 📚 Historical Research Process

#### 1. Source Identification
- Primary medieval sources
- Modern academic interpretations
- Archaeological evidence
- Cultural context from Welsh communities

#### 2. Verification
- Cross-reference multiple sources
- Check for historical consensus
- Identify areas of scholarly debate
- Consult Welsh history experts

#### 3. Game Integration
- Balance historical accuracy with fun gameplay
- Consider player agency and choice
- Maintain immersion and authenticity
- Provide educational value

### 📖 Documentation Requirements

#### Historical Events
```markdown
## Event: [Event Name]
**Date**: [Historical date range]
**Sources**: [Primary and secondary sources]
**Context**: [Historical background]
**Gameplay Integration**: [How it fits in CK3]
**Cultural Significance**: [Why it matters for Welsh culture]
```

#### Character Research
```markdown
## Character: [Historical Figure]
**Lifespan**: [Birth-death dates]
**Position**: [Political/social role]
**Sources**: [Historical documentation]
**Cultural Impact**: [Significance to Welsh culture]
**Game Representation**: [How portrayed in mod]
```

---

## 🏆 Recognition & Credits

### 🎖️ Contributor Categories

#### Historical Consultants
- Researchers providing historical accuracy
- Cultural experts ensuring authenticity
- Academic advisors and reviewers

#### Technical Contributors
- Code development and bug fixes
- Graphics and visual design
- Localization and translation

#### Community Contributors
- Testing and quality assurance
- Feedback and suggestions
- Documentation improvements

### 📜 Credit System
All contributors receive appropriate credit in:
- Mod description and documentation
- In-game credits screen
- GitHub contributors list
- Steam Workshop acknowledgments

---

## 🤝 Community Standards

### 💬 Communication Guidelines

#### Respectful Discourse
- Constructive criticism and feedback
- Professional communication standards
- Cultural sensitivity and awareness
- Focus on improving the mod

#### Collaborative Spirit
- Sharing knowledge and resources
- Supporting other contributors
- Helping newcomers learn
- Building inclusive community

### 🎯 Quality Expectations

#### Historical Accuracy
- Verifiable sources required
- Multiple source confirmation preferred
- Acknowledgment of historical uncertainties
- Transparent about creative interpretations

#### Technical Quality
- Thoroughly tested code
- Clear documentation
- Performance consideration
- Compatibility maintenance

---

## 📞 Getting Help

### 🆘 Support Channels

#### Technical Questions
- **GitHub Issues**: Bug reports and technical problems
- **GitHub Discussions**: General development questions
- **Code Review**: Pull request feedback and suggestions

#### Historical Questions
- **Research Discussions**: Historical accuracy and sources
- **Cultural Consultation**: Welsh cultural authenticity
- **Academic Connections**: Professional historian network

#### Community Support
- **Discord Server**: Real-time community interaction
- **Steam Workshop**: Player feedback and suggestions
- **Reddit Communities**: CK3 modding and Welsh history groups

### 📚 Learning Resources

#### CK3 Modding
- [Official CK3 Modding Documentation](https://ck3.paradoxwikis.com/Modding)
- Community modding tutorials
- Example mods and code references
- Modding tools and utilities

#### Welsh History
- Academic course materials
- Museum educational resources
- Documentary films and series
- Historical society publications

---

<div align="center">
  <p><strong>🏴󠁧󠁢󠁷󠁬󠁳󠁿 Diolch yn fawr! Thank you very much! 🏴󠁧󠁢󠁷󠁬󠁳󠁿</strong></p>
  <p><em>Together we can create an authentic and engaging representation of medieval Welsh culture in Crusader Kings 3.</em></p>
  
  <p>
    <a href="README.md">← Back to Main Documentation</a> •
    <a href="roadmap.md">Development Roadmap</a> •
    <a href="WELSH_CULTURE_GUIDE.md">Welsh Culture Guide</a>
  </p>
</div>
