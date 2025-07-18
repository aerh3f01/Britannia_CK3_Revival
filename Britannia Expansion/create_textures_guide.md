# Welsh Mod Texture Creation Guide

## 🎨 Overview
This guide provides step-by-step instructions for creating all the DDS texture files needed for the Welsh mod's visual enhancement system.

## 📋 Required Textures List

### Court Position Icons (64x64)
- `welsh_court_position_pencerdd.dds` - Chief Poet icon
- `welsh_court_position_bardd_teulu.dds` - Household Bard icon
- `welsh_court_position_distain.dds` - Steward icon
- `welsh_court_position_penteulu.dds` - Captain of Guard icon
- `welsh_court_position_ynad.dds` - Judge icon

### Decision Icons (48x48)
- `welsh_eisteddfod_icon.dds` - Poetry competition
- `welsh_language_promotion_icon.dds` - Language preservation
- `welsh_law_codification_icon.dds` - Legal system
- `welsh_cultural_festival_icon.dds` - Cultural events
- `welsh_bardic_competition_icon.dds` - Bardic contests

### Artifact Icons (56x56)
- `welsh_artifact_harp.dds` - Triple harp
- `welsh_artifact_crown.dds` - Crown of Wales
- `welsh_artifact_sword.dds` - Welsh sword
- `welsh_artifact_shield.dds` - Welsh shield
- `welsh_artifact_manuscript.dds` - Legal manuscript
- `welsh_artifact_torque.dds` - Golden torque
- `welsh_artifact_ring.dds` - Prince's ring

### UI Elements (Various sizes)
- `welsh_dragon_emblem.dds` (64x64) - Main dragon symbol
- `welsh_dragon_small.dds` (24x24) - Small dragon accent
- `welsh_dragon_watermark.dds` (32x32) - Watermark
- `welsh_icon_frame.dds` (72x72) - Icon border
- `welsh_icon_border.dds` (80x80) - Icon frame
- `welsh_corner_decoration.dds` (32x32) - Celtic corners
- `welsh_corner_small.dds` (16x16) - Small corners
- `welsh_knotwork_small.dds` (24x24) - Celtic knots
- `welsh_authenticity_seal.dds` (16x16) - Authenticity mark
- `welsh_rank_indicator.dds` (24x24) - Rank symbol

### Background Textures (512x512, tileable)
- `welsh_parchment_background.dds` - Parchment texture
- `welsh_pattern_border.dds` - Celtic border pattern
- `welsh_pattern_subtle.dds` - Subtle background pattern
- `welsh_event_border.dds` - Event window border

### Illustrations (256x256)
- `welsh_event_illustration_default.dds` - Default event image
- `welsh_illumination_corner.dds` - Illuminated manuscript style
- `welsh_illustration_frame.dds` - Illustration border

### Portrait Frames (128x128)
- `welsh_portrait_frame.dds` - Basic portrait frame
- `welsh_portrait_frame_ornate.dds` - Ornate portrait frame

## 🛠️ Tools Required

### Primary Tools
1. **GIMP** (Free) with DDS plugin
2. **Paint.NET** (Free) with DDS plugin
3. **Photoshop** (Paid) with NVIDIA DDS plugin
4. **Krita** (Free) with DDS support

### DDS Plugins
- **GIMP**: DDS plugin from registry.gimp.org
- **Paint.NET**: DDS FileType plugin
- **Photoshop**: NVIDIA Texture Tools Exporter

## 🎨 Design Guidelines

### Color Palette
- **Primary Red**: RGB(204, 41, 54) - Welsh flag red
- **Welsh White**: RGB(248, 248, 255) - Slightly blue-tinted white
- **Celtic Gold**: RGB(212, 175, 55) - Accent color
- **Welsh Green**: RGB(34, 102, 68) - Landscape green
- **Bronze**: RGB(139, 87, 42) - Ancient metal
- **Slate Grey**: RGB(79, 89, 102) - Welsh slate

### Style Guidelines
- **Historical Accuracy**: Based on medieval Welsh art
- **Celtic Motifs**: Dragons, knotwork, spirals
- **Clean Lines**: Readable at small sizes
- **High Contrast**: Clear visibility in game UI
- **Consistent Style**: Cohesive visual language

## 📐 Technical Specifications

### DDS Format Settings
- **Compression**: BC3 (DXT5) for most textures
- **Mipmaps**: Generate for all textures
- **Alpha Channel**: Include for transparency
- **Power of 2**: All dimensions must be powers of 2

### Size Guidelines
- **Icons**: Clear and readable at target size
- **Backgrounds**: Seamlessly tileable
- **Illustrations**: High detail for larger display
- **UI Elements**: Crisp at intended display size

## 🎯 Symbol Meanings

### Welsh Dragons
- **Red Dragon (Y Ddraig Goch)**: National symbol of Wales
- **Variations**: Rampant, passant, head only
- **Usage**: Primary symbol for Welsh identity

### Celtic Knotwork
- **Endless Knots**: Continuity and eternity
- **Spiral Patterns**: Growth and expansion
- **Interlaced Designs**: Unity and connection
- **Border Patterns**: Decorative frameworks

### Court Position Symbols
- **Pencerdd**: Harp or lyre (chief poet)
- **Bardd Teulu**: Quill or scroll (household bard)
- **Distain**: Keys or ledger (steward)
- **Penteulu**: Sword or shield (captain)
- **Ynad**: Scales or gavel (judge)

## 🖼️ Creation Process

### Step 1: Concept Design
1. Research historical Welsh symbols
2. Sketch concepts on paper
3. Choose primary symbols for each icon
4. Plan color usage and contrast

### Step 2: Base Creation
1. Create new document at target size
2. Set up transparent background
3. Add base shapes and symbols
4. Apply color palette

### Step 3: Detailing
1. Add Celtic knotwork details
2. Apply shading and highlights
3. Ensure readability at small size
4. Test contrast and visibility

### Step 4: DDS Export
1. Export as DDS with BC3 compression
2. Generate mipmaps
3. Verify file size and quality
4. Test in-game if possible

## 🧪 Testing Checklist

### Visual Quality
- [ ] Clear and readable at target size
- [ ] Proper contrast and visibility
- [ ] Consistent style with other icons
- [ ] Appropriate use of Welsh symbols

### Technical Quality
- [ ] Correct DDS format and compression
- [ ] Proper file size (not too large)
- [ ] Mipmaps generated correctly
- [ ] No compression artifacts

### Game Integration
- [ ] File named correctly
- [ ] Located in proper directory
- [ ] Referenced correctly in .gfx file
- [ ] Displays properly in game

## 📚 Resources

### Historical References
- **National Museum Wales**: Welsh medieval art
- **Llyfrgell Genedlaethol Cymru**: Historical manuscripts
- **Cadw**: Welsh heritage and archaeology
- **Medieval Welsh manuscripts**: Book of Kells, Lindisfarne Gospels

### Symbol References
- **Welsh dragon variations**: Historical depictions
- **Celtic art books**: Traditional patterns and motifs
- **Medieval illuminated manuscripts**: Style references
- **Archaeological artifacts**: Authentic symbols and designs

### Online Resources
- **Wikipedia**: Welsh symbols and heraldry
- **Celtic art galleries**: Traditional patterns
- **CK3 modding community**: Technical guidance
- **Historical art databases**: Reference images

## 🎨 Alternative: AI-Generated Textures

If creating textures manually is challenging, consider:

### AI Art Tools
1. **DALL-E 2/3**: High-quality image generation
2. **Midjourney**: Artistic style generation
3. **Stable Diffusion**: Free, customizable
4. **Adobe Firefly**: Integrated with Creative Suite

### AI Prompts for Welsh Textures
- "Medieval Welsh dragon symbol, red and gold, Celtic knotwork, icon style"
- "Ancient Welsh harp, carved wood, golden strings, symbolic icon"
- "Celtic manuscript illumination, Welsh symbols, parchment background"
- "Welsh coat of arms, red dragon, medieval heraldry, clean icon design"

## 📝 Next Steps

1. **Install Required Software**: GIMP with DDS plugin (free option)
2. **Download Reference Images**: Historical Welsh symbols
3. **Start with Court Position Icons**: Begin with most important textures
4. **Test Each Texture**: Verify quality and game compatibility
5. **Iterate and Improve**: Refine based on testing results

## 🔧 Automation Scripts

Consider creating batch processing scripts for:
- Converting PNG to DDS format
- Resizing images to correct dimensions
- Applying consistent compression settings
- Organizing files in correct directories

This guide provides the framework for creating professional-quality textures for the Welsh mod. Start with the most important icons (court positions) and gradually build the complete texture set.
