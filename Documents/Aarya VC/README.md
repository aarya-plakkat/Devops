# 🗣️ Aarya VC – Talking Head Avatar Platform

Welcome to **Aarya VC**, an open-source platform for creating interactive, animated talking head avatars with real-time lipsync, audio playback, and expressive facial animations.

## 🚀 Features

- **3D Avatars**: Supports GLB avatars with customizable moods and body types.
- **Real-Time Lipsync**: Multilingual lipsync modules for English, German, French, Finnish, Lithuanian, and more.
- **Audio Playback**: Integrates Google, Microsoft, and ElevenLabs voices for natural speech synthesis.
- **Dynamic Bones**: Realistic hair and body movement using physics-based animation.
- **Blendshape Animation**: Advanced facial expressions and viseme mapping for lifelike communication.
- **Modular Design**: Easily extend with new avatars, voices, and animation modules.
- **Web-Based**: Runs directly in the browser with Three.js and WebGL.

## 📁 Project Structure

```
├── index.html              # Main demo page
├── modules/                # Core JS modules
│   ├── talkinghead.mjs    # Main talking head engine
│   ├── lipsync-*.mjs      # Language-specific lipsync modules
│   ├── dynamicbones.mjs   # Physics-based bone animation
│   └── playback-worklet.js # Audio playback worklet
├── avatars/                # 3D avatar models
├── audio/                  # Sample audio files
├── blender/                # Blender scripts for avatar preparation
├── examples/               # Example HTML demos
│   ├── minimal.html       # Minimal implementation
│   ├── azure-audio-streaming.html
│   └── azure-blendshapes.html
├── siteconfig.js          # Configuration for avatars and voices
└── SETUP_GUIDE.md         # Setup instructions
```

## 🛠️ Getting Started

### Prerequisites

- A modern web browser with WebGL support
- Local web server (for development)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/aarya-vc.git
   cd aarya-vc
   ```

2. **Start a local server**
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   ```

3. **Open in browser**
   Navigate to `http://localhost:8000/index.html`

4. **Explore examples**
   Check out the `examples/` folder for different implementation demos

## 🎨 Customization

### Adding Custom Avatars

Edit `siteconfig.js` to add your own avatar configurations:

```javascript
avatars: {
  'YourAvatar': {
    url: './avatars/your-avatar.glb',
    body: 'F',
    avatarMood: 'neutral'
  }
}
```

### Configuring Voices

Choose from Google, Microsoft, or ElevenLabs TTS services:

```javascript
googleVoices: {
  "en-F": { id: "en-GB-Standard-A" },
  "en-M": { id: "en-GB-Standard-D" }
}
```

## 🔧 Blender Scripts

The `blender/` folder contains utility scripts for preparing avatars:

- `build-visemes-from-arkit.py` - Generate viseme blendshapes
- `rename-*-shapekeys.py` - Rename shapekeys for different avatar formats
- `rename-mixamo-bones.py` - Bone renaming for Mixamo rigs

## 📚 Examples

- **minimal.html** - Basic talking head implementation
- **azure-audio-streaming.html** - Azure Speech Service integration
- **azure-blendshapes.html** - Advanced facial animation with Azure
- **mp3.html** - Play pre-recorded MP3 with lipsync

## 🌐 Supported Languages

- English (en)
- German (de)
- French (fr)
- Finnish (fi)
- Lithuanian (lt)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

MIT License © 2024 Mika Suominen

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## 🙏 Acknowledgments

Built with:
- [Three.js](https://threejs.org/) - 3D graphics library
- [WebGL](https://www.khronos.org/webgl/) - Hardware-accelerated graphics
- Various TTS services (Google, Microsoft, ElevenLabs)

---

**Made with ❤️ by the Aarya VC Team**
"# Avatar-speech" 
