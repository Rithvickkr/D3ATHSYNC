# D3ATHSYNC 🎯

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/Node.js-v16+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)

![image](https://github.com/user-attachments/assets/37572752-c56c-4753-b801-279242409f0e)



Welcome to **D3ATHSYNC**, a heart-pounding augmented reality (AR) deathmatch game that turns your environment into a high-stakes battlefield! Powered by cutting-edge web tech, this two-player, real-time shooter leverages PoseNet for body tracking and WebGL for immersive AR visuals. Lock horns with an opponent in a relentless duel where precision, strategy, and lightning-fast reflexes crown the champion.

## 🎮 Game Overview

D3ATHSYNC is a browser-based, multiplayer AR game where two players clash in a brutal head-to-head deathmatch. Using TensorFlow.js with PoseNet, the game tracks players' body movements to detect hits, overlaying a virtual crosshair and tactical HUD on your webcam's video feed. Choose from three lethal weapons, aim with deadly intent, and outsmart your rival to sync their demise.

## ✨ Key Features

- **🎯 Augmented Reality Carnage**: Dive into real-time AR with a video feed enhanced by a 3D crosshair and futuristic HUD, driven by Three.js
- **🤖 PoseNet Hit Detection**: Machine learning tracks head, torso, and lower body for pinpoint hit accuracy, with damage scaling by hit zone and weapon type
- **🌐 Multiplayer Mayhem**: Supports two players via Socket.IO, with live health updates and seamless game state sync
- **⚔️ Weapon Arsenal**: Pick from three distinct weapons:
  - **Sniper Rifle**: High damage (40 for headshots), long range, tight hit radius, 400ms cooldown
  - **Tactical Pistol**: Medium damage (20 for headshots), close range, 200ms cooldown
  - **Combat Shotgun**: Extreme damage (20 for headshots), close range, wide hit radius, 600ms cooldown
- **🔊 Immersive Audio**: Gunfire and hit sound effects amplify the chaos
- **🎨 Slick Interface**: Cyberpunk-inspired HUD with health bars, weapon status, and countdown timers, optimized for desktop and mobile
- **📷 Camera Flexibility**: Switch between available webcams for the optimal AR experience

## 🚀 Getting Started

Set up and deploy D3ATHSYNC locally or on a server to unleash the chaos.

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- A modern browser (Chrome, Firefox, or Safari) with webcam access
- An internet connection for multiplayer functionality

### Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/d3athsync.git
   cd d3athsync
   ```

2. **Backend Setup:**
   ```bash
   # Navigate to the backend directory
   cd server
   npm install
   
   # Start the backend server
   npm start
   ```
   The server runs on `http://localhost:3001` by default.

3. **Frontend Setup:**
   ```bash
   # Navigate to the frontend directory
   cd client
   npm install
   
   # Start the frontend development server
   npm run dev
   ```
   The frontend runs on `http://localhost:3000` by default.

4. **Audio Files:**
   Place audio files (`sniper.mp3`, `pistol.mp3`, `shotgun.mp3`, `hit.mp3`) in the frontend's `public/` directory.

5. **Environment Configuration:**
   - For production, update the `allowedOrigins` array in the backend (`server/index.js`) with your deployed frontend URLs
   - Update the Socket.IO connection URL in the frontend (`client/src/components/Game.tsx`) to point to your backend server (e.g., `https://your-backend-server.com`)

### Deployment

- **Backend**: Deploy to Render, Heroku, or similar. Set the `PORT` environment variable.
- **Frontend**: Deploy to Vercel or Netlify. Update the backend URL in the frontend code.
- **HTTPS**: Ensure HTTPS for webcam access in production (browser requirement).

## 🎥 Gameplay

### Joining the Fight
1. Launch the game in a browser and allow webcam access
2. Select a camera and weapon, then hit "Enter Ready State" to gear up
3. Wait for a second player to join and ready up

### Combat
- A 5-second countdown kicks off when both players are ready
- Aim by moving your body or camera, with the crosshair marking your target zone
- Hit the "FIRE" button to shoot, with weapon-specific cooldowns
- Land hits on your opponent's head, torso, or lower body. Damage varies by hit location and weapon

### Victory
- Drop your opponent's health to 0 to win
- The game ends with a victory or defeat screen. Hit "New Mission" to reset and dive back in

## 🛠️ Tech Stack

### Backend
- Node.js with Express.js
- Socket.IO for real-time multiplayer
- CORS for secure cross-origin requests

### Frontend
- React with TypeScript
- Three.js for AR rendering
- TensorFlow.js with PoseNet for body tracking
- Tailwind CSS (via inline styles) for the HUD
- Socket.IO-client for multiplayer communication

### Other
- WebGL for hardware-accelerated graphics
- HTML5 Audio for sound effects

## 📋 Future Enhancements

- [ ] Support for more players or AI opponents
- [ ] New weapons and power-ups
- [ ] AR environmental mapping for cover and obstacles
- [ ] PoseNet optimization for low-end devices
- [ ] Spectator mode and match replays

## 🤝 Contributing

Want to join the fray? Contributions are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a pull request

Follow the Code of Conduct and ensure tests pass.

## 🐛 Bug Reports & Support

Spot a glitch? Got questions? Open an issue on GitHub or join our Discord community (link TBD). Include detailed bug reproduction steps, browser, device, and logs.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🙌 Acknowledgments

- [TensorFlow.js](https://www.tensorflow.org/js) for PoseNet and WebGL
- [Three.js](https://threejs.org/) for AR rendering
- [Socket.IO](https://socket.io/) for real-time multiplayer
- Inspired by classic deathmatch shooters and AR innovations

---

**Sync up and dominate! Deploy D3ATHSYNC, grab a rival, and claim the battlefield!** 🔫
