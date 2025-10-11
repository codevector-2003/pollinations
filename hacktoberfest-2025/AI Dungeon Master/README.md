# 🎭 AI Dungeon Master

**An immersive text-based RPG powered by AI-generated storytelling, dynamic image generation, and interactive gameplay. Experience solo D&D adventures with an intelligent AI dungeon master that creates unique stories, characters, and visuals in real-time.**

![AI Dungeon Master](https://image.pollinations.ai/prompt/fantasy-rpg-dungeon-master-medieval-castle-digital-art-atmospheric?width=800&height=400&model=flux)

## 🌟 **Project Overview**

Transform your RPG experience with cutting-edge AI technology! This project combines advanced language models with real-time image generation to create an infinite, personalized fantasy adventure. Every story is unique, every scene is visualized, and every choice matters.

### 🎯 **Why This Project?**

Traditional text-based RPGs lack visual immersion and dynamic storytelling. AI Dungeon Master solves this by:
- **Dynamic Narratives**: Stories that adapt and evolve based on your choices
- **Visual Storytelling**: Every scene comes alive with AI-generated artwork
- **Infinite Adventures**: No pre-written storylines - pure AI creativity
- **Personalized Experience**: Your character, backstory, and choices shape the entire adventure

---

## ⚡ **Tech Stack**

### **Frontend Framework**
- **React 18** + **TypeScript** + **Vite** - Modern, fast development stack
- **Tailwind CSS v4** - Latest utility-first styling with @tailwindcss/postcss
- **shadcn/ui** + **Radix UI** - Beautiful, accessible components
- **Framer Motion** - Smooth animations and transitions

### **AI Integration**
- **Text Generation**: Pollinations `/api/text/v1/chat/completions`
- **Image Generation**: Pollinations `/api/image/prompt/` with Flux model
- **Context-Aware Processing**: Smart prompt engineering for consistent storytelling

### **State Management & Storage**
- **React Hooks** - useState, useEffect for state management
- **localStorage** - Persistent save/load functionality with data validation
- **Story History Tracking** - Complete adventure chronicle system

---

## 🎮 **Key Features**

### ✨ **Character Creation System**
- **3 Distinct Classes**: 
  - **⚔️ Warrior**: High HP (150), Low Mana (30) - Tank and melee specialist
  - **🧙 Mage**: Low HP (80), High Mana (120) - Magical powerhouse
  - **🗡️ Rogue**: Balanced HP (100), Medium Mana (60) - Stealth and agility
- **Custom Backstories**: AI generates unique opening scenes based on your character's history
- **AI-Generated Avatars**: Personalized character portraits created from descriptions

### 🤖 **Advanced AI Storytelling**
- **Context-Aware Narratives**: Stories that remember and build on previous choices
- **Dynamic Enemy Generation**: Context-appropriate enemies based on current scenes
- **Automatic Item Discovery**: Smart item detection and generation from story events
- **Mood-Based Storytelling**: Peaceful, tense, combat, mysterious, and joyful scene types

### 🎨 **Immersive Visual Experience**
- **Real-Time Scene Generation**: Every story moment gets a unique AI-generated image
- **Fallback System**: Robust error handling ensures beautiful visuals always display
- **Loading States**: Smooth loading indicators while images generate
- **Character Avatars**: Personalized portraits for your unique character

### ⚔️ **Strategic Combat System**
- **D20 Mechanics**: Classic tabletop RPG dice rolling (1-20)
- **Turn-Based Combat**: Strategic decision-making with multiple options
- **Dynamic Damage**: Class-based damage calculations (Warriors hit harder!)
- **Combat Animations**: Engaging visual feedback with dice rolling effects
- **Context-Based Encounters**: Enemies that fit the current story situation

### 🎒 **Advanced Inventory Management**
- **Visual Item Grid**: Beautiful grid layout with AI-generated item images
- **Item Categories**: Weapons, armor, consumables, and miscellaneous items
- **Rarity System**: Common, uncommon, rare, epic, and legendary items
- **Automatic Discovery**: Items are automatically detected and added from story events
- **Item Details**: Rich descriptions and visual representations

### 💾 **Robust Save System**
- **Complete State Preservation**: Save character, inventory, story progress, and history
- **Data Validation**: Corrupted save detection and automatic cleanup
- **Version Control**: Save compatibility checking for future updates
- **Debug Tools**: Browser console commands for save inspection and testing

### 📜 **Story History Chronicle**
- **Complete Adventure Timeline**: View your entire adventure from beginning to current
- **Visual Timeline**: Beautiful interface showing story progression with timestamps
- **Choice Tracking**: See all the decisions that shaped your adventure
- **Image Archive**: Every scene image preserved in your personal chronicle

---

## 🚀 **Quick Start Guide**

### **Prerequisites**
- **Node.js 18+**
- **npm** or **yarn**
- Modern web browser with JavaScript enabled

### **Installation**

```bash
# Clone the repository
git clone https://github.com/pollinations/pollinations.git
cd pollinations/hacktoberfest-2025/AI\ Dungeon\ Master

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:5174](http://localhost:5174) in your browser and begin your adventure!

### **Production Build**

```bash
# Build for production
npm run build

# Preview production build
npm run preview
```

---

## 🎲 **Complete Gameplay Guide**

### **1. Character Creation (The Foundation)**
1. **Enter Character Name**: Choose a memorable name for your hero
2. **Select Class**: Pick from three distinct archetypes:
   - **⚔️ Warrior**: Tank role, high survivability, melee combat focus
   - **🧙 Mage**: Glass cannon, powerful spells, magical abilities
   - **🗡️ Rogue**: Balanced approach, stealth, agility, versatility
3. **Write Backstory**: Craft a compelling background (AI uses this for story generation!)
4. **Avatar Generation**: Watch as AI creates your character's portrait

### **2. Story Interaction (The Adventure)**
- **Read Scenes**: Immerse yourself in AI-generated narrative with visual accompaniment
- **Make Choices**: Select from 4 contextual options that shape your story
- **Environmental Awareness**: Notice how your surroundings influence available actions
- **Character Agency**: Your backstory and class influence story opportunities

### **3. Combat Encounters (The Challenge)**
- **Detection**: AI automatically identifies when enemies appear in your story
- **Dice Rolling**: Experience classic D&D mechanics with visual dice animations
- **Strategic Options**: Choose between aggressive attacks, magical abilities, or defensive maneuvers
- **Consequences**: Combat outcomes directly affect story progression

### **4. Inventory & Progression (The Growth)**
- **Item Discovery**: Items automatically appear based on story events
- **Visual Management**: Organize equipment in an intuitive grid interface
- **Strategic Usage**: Different items provide various advantages in different situations
- **Collection Goals**: Rare and legendary items provide meaningful progression

### **5. Save & Continue (The Persistence)**
- **Manual Saves**: Click "💾 Save Game" to preserve progress at any time
- **Automatic Loading**: Game automatically resumes where you left off
- **Story History**: Use "📜 View Story History" to review your complete adventure

---

## 🔧 **API Integration Details**

### **Story Generation API**
```javascript
// POST /api/text/v1/chat/completions
{
  "model": "openai",
  "messages": [
    {
      "role": "system", 
      "content": "You are a creative dungeon master for a fantasy RPG..."
    },
    {
      "role": "user", 
      "content": "Continue the story for Gandara, a Mage. Previous scene: ..."
    }
  ]
}
```

### **Image Generation API**
```javascript
// GET /api/image/prompt/{encoded_prompt}
// Example: fantasy rpg scene, ancient temple, digital art, atmospheric
https://image.pollinations.ai/prompt/fantasy%20rpg%20scene%20ancient%20temple%20digital%20art%20atmospheric?width=1024&height=768&model=flux
```

### **Error Handling & Fallbacks**
- **Text Generation**: Fallback to generic adventure text if API fails
- **Image Generation**: Automatic fallback images ensure visual consistency
- **Network Issues**: Graceful degradation with user feedback

---

## 🏗️ **Project Architecture**

```
src/
├── components/
│   ├── ui/                    # shadcn/ui component library
│   │   ├── button.tsx
│   │   ├── dialog.tsx
│   │   ├── progress.tsx
│   │   └── scroll-area.tsx
│   ├── CharacterCreation.tsx  # Character creation form and logic
│   ├── MainGameScreen.tsx     # Main game interface controller
│   ├── PlayerStatsCard.tsx    # Character stats display (HP, Mana, Level)
│   ├── SceneArea.tsx          # Scene image and text display with fallbacks
│   ├── StoryText.tsx          # Formatted story text component
│   ├── ChoicesSection.tsx     # Interactive choice buttons
│   ├── InventoryGrid.tsx      # Visual inventory management
│   ├── InventoryModal.tsx     # Detailed inventory popup
│   ├── CombatModal.tsx        # Turn-based combat interface
│   └── StoryHistory.tsx       # Adventure timeline chronicle
├── App.tsx                    # Main application logic and state management
├── main.tsx                   # Application entry point
├── index.css                  # Global styles and Tailwind imports
└── vite-env.d.ts             # TypeScript environment declarations
```

---

## 🎨 **Game Mechanics Deep Dive**

### **Character System**
```typescript
interface Character {
  name: string;
  class: 'Warrior' | 'Mage' | 'Rogue';
  backstory: string;
  level: number;
  hp: number;
  maxHp: number;
  mana: number;
  maxMana: number;
  avatar: string;
}
```

### **Combat Mechanics**
- **Initiative**: Player attacks first
- **Attack Resolution**: D20 roll vs D20 roll (higher wins)
- **Damage Calculation**: Winner deals D6 + class modifier damage
- **Class Modifiers**: Warriors get damage bonus, Mages get mana abilities
- **Victory Conditions**: Reduce enemy HP to 0 or below

### **Inventory System**
```typescript
interface InventoryItem {
  id: string;
  name: string;
  description: string;
  image: string;
  type: 'weapon' | 'armor' | 'consumable' | 'misc';
  rarity: 'common' | 'uncommon' | 'rare' | 'epic' | 'legendary';
  quantity: number;
  value?: number;
}
```

### **Story Progression**
```typescript
interface StoryEntry {
  id: string;
  description: string;
  image: string;
  timestamp: number;
  characterChoice?: string;
}
```

---

## 🎯 **Available Scripts**

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with hot reload |
| `npm run build` | Create optimized production build |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint for code quality checks |

---

## 🌟 **Advanced Features**

### **Current Implementation**
- ✅ **Real-time AI Integration**: Both text and image generation
- ✅ **Context-Aware Storytelling**: Stories build on previous choices
- ✅ **Robust Error Handling**: Fallbacks for all AI generation failures
- ✅ **Responsive Design**: Beautiful UI on all device sizes
- ✅ **Persistent State**: Complete save/load with data validation
- ✅ **Visual Polish**: Smooth animations and loading states
- ✅ **Story Chronicles**: Complete adventure history tracking
- ✅ **Auto-Discovery**: Items and enemies generated from story context

### **Future Enhancement Roadmap**
- 🔮 **Multiplayer Support**: Multiple players with shared AI dungeon master
- 📜 **Quest System**: Structured objectives and rewards
- 🗺️ **World Mapping**: Visual world generation and exploration
- 📈 **Character Progression**: Experience points and leveling system
- 🎭 **NPC Relationships**: Persistent character interactions
- 📄 **Adventure Export**: PDF generation of complete stories
- 🎵 **Dynamic Audio**: AI-generated ambient sounds and music

---

## 🎨 **Visual Design Philosophy**

### **Theme & Aesthetic**
- **Medieval Fantasy**: Rich, warm earth tones with golden accents
- **Typography**: Cinzel for headers (fantasy feel), system fonts for readability
- **Color Palette**: Deep browns (#2c1e12), warm golds (#d4a76a), parchment (#f5e6d3)
- **Layout**: Card-based design with clear visual hierarchy

### **User Experience**
- **Accessibility**: ARIA labels, keyboard navigation, screen reader support
- **Performance**: Optimized images, lazy loading, efficient state management
- **Responsiveness**: Mobile-first design with desktop enhancements
- **Feedback**: Loading states, error messages, success confirmations

---

## 🏆 **Project Achievements**

### **Hacktoberfest 2025 - Advanced Difficulty**
- ✅ **Complex AI Integration**: Multiple API endpoints with error handling
- ✅ **Real-time Content Generation**: Dynamic text and image creation
- ✅ **Advanced State Management**: Complex game state with persistence
- ✅ **Modern Tech Stack**: Latest React, TypeScript, and Tailwind CSS
- ✅ **Production Ready**: Error handling, loading states, responsive design
- ✅ **Comprehensive Documentation**: Detailed README with gameplay guide

### **Lines of Code: 1000+**
- React components with TypeScript interfaces
- AI integration with robust error handling
- Save/load system with data validation
- Combat mechanics with visual feedback
- Inventory management with visual components

---

## 🎮 **Live Demo**

**Start Your Adventure**: [http://localhost:5174](http://localhost:5174)

1. Run `npm run dev`
2. Open the URL in your browser
3. Create your character
4. Begin your AI-powered fantasy adventure!

---

## 🛠️ **Development & Debugging**

### **Console Commands for Testing**
```javascript
// Check save data
checkSaveData()

// Clear save data for fresh start
clearSaveData()

// Inspect current game state
console.log('Current game state:', gameState)
```

### **Common Issues & Solutions**
- **Images not loading**: Check network connectivity, fallbacks will display
- **Story generation slow**: AI processing time varies, loading indicators show progress
- **Save not working**: Check browser localStorage permissions
- **Combat not triggering**: Ensure enemy keywords are present in story text

---

## 📝 **Contributing**

This project is part of **Hacktoberfest 2025**. Contributions welcome!

### **How to Contribute**
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### **Contribution Ideas**
- New character classes or abilities
- Additional combat mechanics
- Enhanced UI/UX improvements
- Performance optimizations
- New AI integration features

---

## 📄 **License**

This project is part of the Pollinations ecosystem. Check the main repository for license details.

---

**🎭 Embark on your AI-powered fantasy adventure! Every story is unique, every choice matters, and every scene comes alive with AI-generated visuals. ⚔️✨**

*Developed for Hacktoberfest 2025 - Showcasing the future of AI-powered interactive storytelling*
```
