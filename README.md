# 🚗 Automotive Signal Generator

Professional automotive signal generator for **Crank**, **Cam 1** & **Cam 2** signals with ESP32/Arduino support.

**Developed by: SALAH ALRAWI**  
**Mobile: +964 781 156 6375**

## 🌟 Features

### 📊 Signal Generation
- **Real-time signal visualization** with oscilloscope mode
- **Interactive pulse editing** - click to toggle individual pulses
- **Multiple signal types**: Square wave and Sine wave
- **Configurable RPM**: 100-8000 RPM range
- **Missing tooth patterns**: 36-1, 60-2, 24-1 support
- **Cam signal synchronization** with adjustable phase offset

### 🚀 Hardware Integration
- **ESP32 connectivity** via Web Serial API
- **Arduino code generation** for standalone operation
- **Real-time signal transmission** to hardware
- **SD card pattern storage** on ESP32
- **LCD display support** for hardware status

### 🎯 Vehicle Database
- **Comprehensive vehicle database** with 80+ brands
- **25,000+ vehicle models** from global manufacturers
- **Engine specifications** including displacement and type
- **Years coverage**: 2000-2026

### 📱 Progressive Web App (PWA)
- **Install on any device** - works like a native app
- **Offline functionality** - works without internet
- **Responsive design** - optimized for tablets and mobile
- **Touch-friendly controls** - perfect for workshop use

### 🔧 Advanced Tools
- **Signal plotter** with image import and annotation
- **Measurement tools** with ruler and frequency analysis
- **Pattern history** with save/load functionality
- **File export/import** in multiple formats
- **Zoom controls** for detailed signal analysis

## 🚀 Quick Start

### 📱 Install on Android Tablet
1. Open **Chrome** browser on your Android device
2. Visit: **[https://yourusername.github.io/automotive-signal-generator](https://yourusername.github.io/automotive-signal-generator)**
3. Tap **"Add to Home Screen"** when prompted
4. Launch from home screen like a native app

### 💻 Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/automotive-signal-generator.git
cd automotive-signal-generator

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 🔌 Hardware Setup

### ESP32 Connection
1. Connect ESP32 to your computer via USB
2. Click **"Connect ESP32"** in the app
3. Select the correct serial port
4. Configure baud rate (default: 115200)
5. Transmit signal patterns to ESP32

### Arduino Integration
1. Select your vehicle from the database
2. Configure signal parameters (RPM, teeth count)
3. Click **"Generate Arduino Code"**
4. Upload the generated code to your Arduino
5. Connect output pins to your test equipment

## 📊 Signal Patterns

### Supported Patterns
- **36-1 Crank Pattern** (most common)
- **60-2 Crank Pattern** (high resolution)
- **24-1 Crank Pattern** (older vehicles)
- **Custom patterns** via interactive editing

### Output Specifications
- **Voltage levels**: 0V (LOW) / 5V (HIGH)
- **Frequency range**: 1Hz - 1000Hz
- **Resolution**: 1600 samples per signal
- **Timing accuracy**: ±1ms

## 🛠️ Technical Specifications

### Browser Requirements
- **Chrome 89+** (recommended)
- **Edge 89+**
- **Firefox 85+**
- **Safari 14+**

### Hardware Requirements
- **ESP32** or **Arduino Uno/Nano**
- **16x2 LCD Display** (optional)
- **SD Card Module** (for ESP32 pattern storage)
- **Logic level outputs** (3.3V/5V compatible)

### Performance
- **Real-time generation** at up to 8000 RPM
- **Low latency** signal output (<1ms)
- **Memory efficient** pattern storage
- **Responsive UI** on mobile devices

## 📁 Project Structure

```
src/
├── main.ts              # Application entry point
├── signal-generator.ts  # Core signal generation logic
├── canvas-renderer.ts   # Real-time signal visualization
├── ui-controller.ts     # User interface management
├── vehicle-data.ts      # Vehicle database
├── signal-transmitter.ts # ESP32/Arduino communication
├── signal-plotter.ts    # Advanced analysis tools
└── style.css           # Responsive styling

public/
├── manifest.json       # PWA configuration
├── sw.js              # Service worker for offline support
└── index.html         # Main HTML template
```

## 🔧 Configuration

### Signal Parameters
```typescript
interface SignalConfig {
  rpm: number           // Engine RPM (100-8000)
  teethCount: number    // Crank teeth count (24, 36, 60)
  camRatio: number      // Cam to crank ratio (1, 2, 4)
  signalType: 'square' | 'sine'  // Waveform type
}
```

### Hardware Pins (ESP32)
```cpp
const int CRANK_PIN = 25;  // Crank signal output
const int CAM1_PIN = 26;   // Cam 1 signal output
const int CAM2_PIN = 27;   // Cam 2 signal output
```

## 🚀 Deployment

### GitHub Pages (Automatic)
1. Fork this repository
2. Enable GitHub Pages in repository settings
3. Push changes to `main` branch
4. Access at: `https://yourusername.github.io/automotive-signal-generator`

### Manual Deployment
```bash
# Build the application
npm run build

# Deploy to any static hosting service
# Upload the 'dist' folder contents
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Developer

**SALAH ALRAWI**  
Automotive Electronics Engineer  
📱 Mobile: +964 781 156 6375  
📧 Email: [contact@salahalrawi.com](mailto:contact@salahalrawi.com)

### Expertise
- Automotive diagnostics and signal analysis
- ESP32/Arduino embedded systems
- Real-time signal processing
- Progressive Web App development
- Mobile-first responsive design

## 🙏 Acknowledgments

- Vehicle database compiled from manufacturer specifications
- Signal patterns based on automotive industry standards
- PWA implementation following Google's best practices
- Responsive design optimized for workshop environments

## 📱 Screenshots

### Desktop Interface
![Desktop Interface](https://images.pexels.com/photos/3862132/pexels-photo-3862132.jpeg?auto=compress&cs=tinysrgb&w=1280&h=720&fit=crop)

### Mobile/Tablet View
![Mobile Interface](https://images.pexels.com/photos/190574/pexels-photo-190574.jpeg?auto=compress&cs=tinysrgb&w=512&h=512&fit=crop)

---

**⭐ Star this repository if you find it useful!**

**🔧 Perfect for automotive workshops, training centers, and diagnostic equipment testing.**
