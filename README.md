# CityForge AI

A stunning 3D isometric city-building simulation game powered by Google's Gemini AI. Build and manage your virtual metropolis with AI-generated goals, dynamic news events, and beautiful procedurally generated buildings.

![CityForge AI](https://img.shields.io/badge/Built%20with-React%20%2B%20Three.js-61DAFB?style=for-the-badge&logo=react)
![Gemini AI](https://img.shields.io/badge/Powered%20by-Gemini%20AI-4285F4?style=for-the-badge&logo=google)

---

## 📋 Project Information

- **Project Name:** GenAI_slingshot
- **Course:** AI for Games
- **Institution:** Polytechnique Sousse
- **Professor:** Mme Souha Banneni
- **Academic Year:** 2025-2026
- **Authors:**
  - **Aymen Mabrouk** ([GitHub](https://github.com/AymenMB))
  - **Mohammed Amine Ben Charrada**

---

## 🎮 Features

### 🏗️ City Building
- **Isometric 3D Graphics**: Beautiful isometric view powered by Three.js and React Three Fiber
- **Multiple Building Types**: 
  - 🏠 **Residential** - Houses for your citizens (generates population)
  - 🏪 **Commercial** - Shops and businesses (generates income)
  - 🏭 **Industrial** - Factories for production (generates high income)
  - 🌳 **Parks** - Green spaces for citizen happiness
  - 🛣️ **Roads** - Connect your city infrastructure
- **Procedural Buildings**: Each building is uniquely generated with variants for visual diversity
- **Dynamic Systems**:
  - Animated traffic with cars driving on roads
  - Citizens walking around parks and roads
  - Floating clouds and flying birds
  - Smoke stacks on factories
  - Realistic shadows and lighting

### 🤖 AI-Powered Gameplay
- **Smart City Advisor**: Gemini AI generates contextual goals based on your city's current state
- **Dynamic Objectives**: AI creates challenging but achievable goals:
  - Population targets
  - Money milestones
  - Building count requirements
- **Live News Feed**: AI-generated news headlines that react to your city's development
- **Adaptive Difficulty**: Goals scale with your city's progress

### 🎨 Visual Excellence
- **Modern UI/UX**: Sleek glassmorphism design with smooth animations
- **Real-time Stats**: Track your treasury, population, and day counter
- **Interactive Toolbar**: Easy-to-use building placement system
- **Hover Previews**: See buildings before you place them
- **Responsive Design**: Optimized for both desktop and mobile devices

### ⚙️ Game Mechanics
- **Economic System**: Balance income and expenses
- **Population Management**: Build homes to attract citizens
- **Resource Generation**: Different buildings generate money and population
- **Day/Night Cycle**: Game progresses in real-time ticks
- **Sandbox Mode**: Play without AI for creative freedom

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **Google Gemini API Key** - [Get one here](https://aistudio.google.com/app/apikey)

### Installation

1. **Clone or download this repository**
   ```bash
   cd "d:/cycleing/5eme/ai for games"
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up your environment variables**
   
   Create a `.env.local` file in the root directory:
   ```bash
   # Create the file
   echo GEMINI_API_KEY=your_api_key_here > .env.local
   ```
   
   Replace `your_api_key_here` with your actual Gemini API key from [Google AI Studio](https://aistudio.google.com/app/apikey).

   **Example `.env.local` file:**
   ```env
   GEMINI_API_KEY=AIzaSyAbc123YourActualAPIKeyHere
   ```

### Running Locally

1. **Start the development server**
   ```bash
   npm run dev
   ```

2. **Open your browser**
   
   Navigate to: `http://localhost:3000`

3. **Start building!**
   - Choose whether to enable AI City Advisor
   - Click "Start Building" to begin
   - Select building types from the toolbar
   - Click on tiles to place buildings
   - Complete AI-generated goals to earn rewards

### Building for Production

To create an optimized production build:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## 🎯 How to Play

### Basic Controls
- **Mouse/Touch**: Click or tap on tiles to place buildings
- **Camera**: 
  - Drag to rotate the view
  - Scroll to zoom in/out
  - Right-click drag to pan

### Building Your City

1. **Start with Roads** 🛣️
   - Roads are cheap (💰 $10)
   - They connect your city and enable traffic

2. **Build Houses** 🏠
   - Cost: 💰 $100
   - Generates: 👥 +5 population/day
   - Maximum capacity: 50 citizens per house

3. **Add Shops** 🏪
   - Cost: 💰 $200
   - Generates: 💵 +$15/day

4. **Construct Factories** 🏭
   - Cost: 💰 $400
   - Generates: 💵 +$40/day
   - Features animated smoke stacks

5. **Create Parks** 🌳
   - Cost: 💰 $50
   - Generates: 👥 +1 population/day
   - Improves city aesthetics

6. **Bulldoze** ✕
   - Cost: 💰 $5
   - Remove unwanted buildings

### AI Advisor Mode

When enabled, the AI City Advisor will:
- Generate contextual goals based on your city's state
- Provide monetary rewards for completing objectives
- Create dynamic news events that reflect your city's development
- Adapt challenges to your progress

### Sandbox Mode

Disable AI for creative freedom:
- No goals or objectives
- Build at your own pace
- Perfect for experimenting with city layouts

## 🛠️ Technology Stack

### Frontend
- **React 19** - Modern UI framework
- **TypeScript** - Type-safe development
- **Three.js** - 3D graphics engine
- **React Three Fiber** - React renderer for Three.js
- **React Three Drei** - Useful helpers for R3F

### AI Integration
- **Google Gemini AI** - Generates goals and news events
- **@google/genai** - Official Gemini SDK

### Build Tools
- **Vite** - Lightning-fast build tool
- **Tailwind CSS** - Utility-first CSS (via CDN)

## 📁 Project Structure

```
ai for games/
├── components/
│   ├── IsoMap.tsx          # 3D isometric map with Three.js
│   ├── UIOverlay.tsx       # Game UI (stats, toolbar, news)
│   └── StartScreen.tsx     # Initial game screen
├── services/
│   └── geminiService.ts    # AI integration for goals & news
├── App.tsx                 # Main game logic and state
├── types.ts                # TypeScript type definitions
├── constants.tsx           # Game configuration
├── index.tsx               # React entry point
├── index.html              # HTML template
├── vite.config.ts          # Vite configuration
├── package.json            # Dependencies
└── .env.local              # Environment variables (create this)
```

## 🎨 Customization

### Adjusting Game Settings

Edit `constants.tsx` to modify:
- **Grid Size**: Change `GRID_SIZE` (default: 15x15)
- **Tick Rate**: Adjust `TICK_RATE_MS` (default: 2000ms)
- **Starting Money**: Modify `INITIAL_MONEY` (default: $1000)
- **Building Costs**: Update values in `BUILDINGS` object
- **Income/Population Generation**: Modify `incomeGen` and `popGen` values

### Changing AI Behavior

Edit `services/geminiService.ts` to:
- Adjust AI model (default: `gemini-2.5-flash`)
- Modify temperature for creativity
- Customize prompt engineering
- Change goal generation logic

## 🐛 Troubleshooting

### API Key Issues
**Problem**: "API key error" or AI features not working

**Solution**:
1. Verify your `.env.local` file exists in the root directory
2. Ensure the key is named exactly `GEMINI_API_KEY`
3. Check that your API key is valid at [Google AI Studio](https://aistudio.google.com/app/apikey)
4. Restart the development server after changing `.env.local`

### Build Errors
**Problem**: npm install fails or build errors

**Solution**:
```bash
# Clear cache and reinstall
rm -rf node_modules package-lock.json
npm install
```

### Performance Issues
**Problem**: Game runs slowly

**Solution**:
- Reduce grid size in `constants.tsx`
- Lower the number of cars/citizens in `IsoMap.tsx`
- Disable shadows in the Canvas component
- Use a more powerful device

### Port Already in Use
**Problem**: Port 3000 is already in use

**Solution**:
```bash
# Use a different port
npm run dev -- --port 3001
```

## 📝 License

This project is licensed under the Apache-2.0 License.

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 🎓 Learning Resources

- [React Documentation](https://react.dev/)
- [Three.js Documentation](https://threejs.org/docs/)
- [React Three Fiber](https://docs.pmnd.rs/react-three-fiber/)
- [Google Gemini API](https://ai.google.dev/docs)
- [Vite Guide](https://vitejs.dev/guide/)

## 🌟 Acknowledgments

Built with modern web technologies and powered by Google's Gemini AI for an intelligent gaming experience.

---

**Enjoy building your city! 🏙️✨**
