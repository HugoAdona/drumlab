# DrumLab 🥁

A powerful and intuitive web-based drum machine built by Hugo Adona. Create beats, mix patterns, and unleash your rhythm creativity directly in your browser.

## 🎵 Features

- **Step Sequencer**: Classic 16-step sequencing with visual feedback
- **Multiple Drum Kits**: Various drum sounds including hip-hop, electronic, acoustic, and vintage
- **Real-time Playback**: Hear your beats as you create them
- **Pattern Management**: Save, load, and manage multiple drum patterns
- **Tempo Control**: Adjustable BPM from 60 to 180+
- **Volume Mixing**: Individual volume controls for each drum element
- **Swing & Groove**: Add swing and groove to your patterns
- **Export Options**: Save your beats as audio files
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Keyboard Shortcuts**: Quick access to all functions

## 🎹 Demo

Try DrumLab live: [Demo Link](#) *(Update with your deployed URL)*

## 🎵 Sound Library

- **Kick Drums**: Punchy 808s, acoustic kicks, electronic bass drums
- **Snares**: Crisp snares, claps, rim shots
- **Hi-hats**: Closed hats, open hats, shakers
- **Cymbals**: Crashes, rides, splashes
- **Percussion**: Toms, cowbells, tambourines, and more
- **Electronic**: Synthesized drums, digital percussion

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Audio**: Web Audio API
- **UI Framework**: Vanilla JS with modern CSS
- **Audio Processing**: AudioContext, AudioBuffer
- **Storage**: LocalStorage for pattern saving
- **Icons**: Custom SVG icons

## 🚀 Getting Started

### Prerequisites

- Modern web browser with Web Audio API support
- No additional software required!

### Installation

1. Clone the repository:
```bash
git clone https://github.com/HugoAdona/drumlab.git
cd drumlab
```

2. Serve the files locally:

**Using Python:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

**Using Node.js:**
```bash
npx serve .
```

**Using PHP:**
```bash
php -S localhost:8000
```

3. Open your browser and navigate to `http://localhost:8000`

### Quick Start

1. **Select a Kit**: Choose from available drum kits
2. **Create a Pattern**: Click on the step sequencer grid to add beats
3. **Press Play**: Hit the play button to hear your creation
4. **Adjust Settings**: Modify tempo, volume, and swing
5. **Save Your Work**: Use the save function to store your patterns

## 🎹 Usage Guide

### Basic Controls

- **Play/Pause**: Start or stop playback
- **Stop**: Stop and reset to beginning
- **Tempo**: Adjust BPM with the tempo slider
- **Volume**: Master volume control
- **Swing**: Add groove to your patterns

### Step Sequencer

- **Click Steps**: Click on grid squares to activate/deactivate beats
- **Pattern Length**: Choose between 8, 16, or 32 steps
- **Clear Pattern**: Reset the current pattern
- **Random Pattern**: Generate a random beat pattern

### Drum Elements

Each row represents a different drum sound:
- **Kick**: Bass drum patterns
- **Snare**: Snare drum hits
- **Hi-hat**: Hi-hat patterns (closed/open)
- **Crash**: Cymbal accents
- **Percussion**: Additional percussion elements

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Spacebar` | Play/Pause |
| `S` | Stop |
| `C` | Clear pattern |
| `R` | Random pattern |
| `1-8` | Select drum kit |
| `↑/↓` | Adjust tempo |
| `Enter` | Save pattern |

## 🎨 Customization

### Adding New Drum Kits

1. Add audio files to the `sounds/` directory
2. Update the kit configuration in `js/kits.js`:

```javascript
const drumKits = {
  'custom-kit': {
    name: 'Custom Kit',
    sounds: {
      kick: 'sounds/custom/kick.wav',
      snare: 'sounds/custom/snare.wav',
      hihat: 'sounds/custom/hihat.wav',
      // ... more sounds
    }
  }
};
```

### Styling

Customize the appearance by modifying:
- `css/main.css` - Main styling
- `css/sequencer.css` - Step sequencer styles
- `css/controls.css` - Control panel styles

## 📁 Project Structure

```
drumlab/
├── index.html              # Main HTML file
├── css/
│   ├── main.css           # Main stylesheet
│   ├── sequencer.css      # Sequencer styles
│   ├── controls.css       # Control panel styles
│   └── responsive.css     # Mobile responsiveness
├── js/
│   ├── app.js             # Main application logic
│   ├── sequencer.js       # Step sequencer functionality
│   ├── audio.js           # Audio engine
│   ├── kits.js            # Drum kit definitions
│   └── storage.js         # Pattern storage
├── sounds/
│   ├── kit1/              # Drum kit 1 samples
│   ├── kit2/              # Drum kit 2 samples
│   └── ...                # Additional kits
├── assets/
│   ├── icons/             # UI icons
│   └── images/            # Background images
├── README.md
└── LICENSE
```

## 🎵 Pattern Format

Patterns are stored in JSON format:

```json
{
  "name": "My Beat",
  "tempo": 120,
  "swing": 0,
  "kit": "hip-hop",
  "steps": 16,
  "pattern": {
    "kick": [1,0,0,0,1,0,0,0,1,0,0,0,1,0,0,0],
    "snare": [0,0,0,0,1,0,0,0,0,0,0,0,1,0,0,0],
    "hihat": [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1]
  }
}
```

## 🚀 Deployment

### GitHub Pages

1. Push your code to GitHub
2. Go to repository Settings > Pages
3. Select source branch (main/master)
4. Your drum machine will be live at `https://yourusername.github.io/drumlab`

### Netlify

1. Connect your GitHub repository
2. No build process needed
3. Deploy instantly

### Vercel

1. Import from GitHub
2. No configuration required
3. Auto-deploy on commits

## 🎹 Performance Tips

- **Audio Context**: The Web Audio API requires user interaction to start
- **Preload Sounds**: All drum samples are preloaded for smooth playback
- **Buffer Management**: Efficient audio buffer handling for minimal latency
- **Mobile Optimization**: Touch-friendly interface for mobile devices

## 🤝 Contributing

Beat makers and developers welcome! Contributions help make DrumLab even better.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewDrumKit`)
3. Commit your Changes (`git commit -m 'Add epic drum kit'`)
4. Push to the Branch (`git push origin feature/NewDrumKit`)
5. Open a Pull Request

### Contributing Ideas

- **New Drum Kits**: Add more sound libraries
- **Effects**: Reverb, delay, distortion
- **Pattern Sharing**: Import/export functionality
- **Recording**: Multi-track recording capabilities
- **Visualization**: Audio spectrum analyzer
- **MIDI Support**: External controller integration

## 🐛 Known Issues

- Some browsers may have audio latency issues
- Safari requires user interaction to start audio
- Mobile devices may have limited concurrent audio streams

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Hugo Adona**
- GitHub: [@HugoAdona](https://github.com/HugoAdona)
- Website: [Your Website]

## 🎵 Acknowledgments

- Web Audio API documentation and community
- Drum sample libraries and creators
- Beat makers and musicians who inspire creativity
- Open source audio projects

## 🔗 Related Projects

- [Quotely](https://github.com/HugoAdona/quotely) - Random quote generator
- [MarkdownMagic](https://github.com/HugoAdona/markdownmagic) - Markdown editor

## 🎼 Musical Inspiration

*"Music is the universal language of mankind."* - Henry Wadsworth Longfellow

Start creating your beats today with DrumLab! 🎵🥁