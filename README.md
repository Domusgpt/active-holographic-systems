# 🌌 Active Holographic Systems

**30-Variation Multilateral Polytonal Geometry Visualizer**

Advanced WebGL-based holographic visualization system featuring real-time audio reactivity, 4D mathematics, and VIB3 geometry library.

## 🚀 [**LIVE DEMO →**](https://domusgpt.github.io/active-holographic-systems/)

## 🎯 Features

### **30 Holographic Variations**
- **8 Base Geometries**: Tetrahedron, Hypercube, Sphere, Torus, Klein Bottle, Fractal, Wave, Crystal
- **Multiple Variants**: Field, Matrix, Lattice, Resonance variations of each geometry
- **Real-time Switching**: Manual controls + auto-cycling

### **Audio Reactivity**
- **Mobile-Optimized**: Fixed Chrome Android microphone permissions
- **3-Band Analysis**: Bass, Mid, High frequency separation
- **Visual Mapping**: Frequencies control density, rotation, colors, effects
- **Smooth Processing**: Anti-jitter algorithms for stable visuals

### **5-Layer Rendering**
- **Background Layer**: Subtle foundation patterns (20% opacity)
- **Shadow Layer**: Depth illusion with offset blur (60% opacity)
- **Content Layer**: Primary geometry visualization (80% opacity)
- **Highlight Layer**: Screen blend mode highlights (40% opacity)
- **Accent Layer**: Color-dodge accents for holographic effect (30% opacity)

### **Interactive Systems**
- **Mouse Reactivity**: Parallax tracking and click effects
- **Touch Support**: Multi-touch gestures on mobile
- **Scroll Physics**: Parallax depth control
- **Grid Overlay**: Dynamic visibility based on interaction

## 🎨 Geometry Library

### VIB3 8-Geometry Mathematical System

#### **1. TETRAHEDRON LATTICE**
```glsl
// 4-vertex tetrahedral grid with edge connections
float tetrahedronLattice(vec3 p, float gridSize) {
    vec3 q = fract(p * gridSize) - 0.5;
    float d1 = length(q);
    float d2 = length(q - vec3(0.4, 0.0, 0.0));
    float d3 = length(q - vec3(0.0, 0.4, 0.0));
    float d4 = length(q - vec3(0.0, 0.0, 0.4));
    return smoothstep(vertices, edges);
}
```

#### **2. HYPERCUBE LATTICE**
```glsl
// 4D cube projection with grid-based edges
float hypercubeLattice(vec3 p, float gridSize) {
    vec3 grid = fract(p * gridSize);
    vec3 edges = 1.0 - smoothstep(0.0, 0.03, abs(grid - 0.5));
    return max(max(edges.x, edges.y), edges.z);
}
```

#### **3. SPHERE LATTICE**
```glsl
// Radial distance field spheres
float sphereLattice(vec3 p, float gridSize) {
    vec3 q = fract(p * gridSize) - 0.5;
    float r = length(q);
    return 1.0 - smoothstep(0.2, 0.5, r);
}
```

#### **4. TORUS LATTICE**
```glsl
// Double-radius torus mathematics
float torusLattice(vec3 p, float gridSize) {
    vec3 q = fract(p * gridSize) - 0.5;
    float r1 = sqrt(q.x*q.x + q.y*q.y);
    float r2 = sqrt((r1 - 0.3)*(r1 - 0.3) + q.z*q.z);
    return 1.0 - smoothstep(0.0, 0.1, r2);
}
```

## 🔧 Technical Architecture

### **WebGL Shaders**
- **4D Rotation Matrices**: XW, YW, ZW rotational transforms
- **4D to 3D Projection**: Perspective projection from 4D space
- **Dynamic Geometry Selection**: Runtime switching between lattice types
- **HSV Color Space**: Smooth hue transitions and saturation control

### **Audio Processing**
```javascript
// Enhanced frequency analysis
const bassEnd = Math.floor(frequencyData.length * 0.1);    // 20-250 Hz
const midEnd = Math.floor(frequencyData.length * 0.4);     // 250-4000 Hz
// High frequencies: 4000+ Hz

// Audio influence mapping
bassInfluence: { density: 2.0, rotation: 0.05, intensity: 0.8 }
midInfluence: { morph: 1.5, chaos: 1.2, colorShift: 180.0 }
highInfluence: { speed: 3.0, glitch: 0.8, zoom: 0.5 }
```

### **Role-Based Reactivity**
Each layer responds differently to audio:
- **Background**: 30% reactivity, gentle movement
- **Shadow**: 50% reactivity, depth effects  
- **Content**: 100% reactivity, primary visualization
- **Highlight**: 120% reactivity, enhanced brightness
- **Accent**: 150% reactivity, maximum intensity

## 🎮 Controls

### **Manual Controls**
- **◀ PREV / NEXT ▶**: Switch between 30 variations
- **🎲 RANDOM**: Jump to random variation
- **▶ AUTO**: Auto-cycle every 3 seconds
- **🎵 AUDIO**: Toggle audio reactivity

### **Keyboard Shortcuts**
- **←/→**: Previous/Next variation
- **Space**: Random variation
- **Enter**: Toggle auto-cycle
- **A**: Toggle audio

### **Mouse/Touch Interactions**
- **Mouse Movement**: Parallax tracking
- **Click/Tap**: Pulse effects with ripples
- **Scroll**: Parallax depth control (desktop)
- **Touch Gestures**: Morph and chaos control (mobile)

## 🛠️ Development Roadmap

### **Phase 1: Enhanced Variations** 🚧
- [ ] Expand to 50+ geometric variations
- [ ] Add custom shader effects per geometry
- [ ] Implement preset save/load system
- [ ] Create variation gallery interface

### **Phase 2: Advanced Audio** 🔮
- [ ] Beat detection algorithms
- [ ] Spectral analysis visualization
- [ ] MIDI input support
- [ ] Audio file upload/analysis

### **Phase 3: VR/AR Integration** 🥽
- [ ] WebXR implementation
- [ ] Spatial audio mapping
- [ ] Hand tracking integration
- [ ] Holographic projection modes

### **Phase 4: Performance & Mobile** 📱
- [ ] WebGL 2.0 optimization
- [ ] Adaptive quality system
- [ ] Progressive Web App (PWA)
- [ ] Offline mode capability

## 🌐 Browser Compatibility

### **Desktop**
- ✅ Chrome 80+ (Recommended)
- ✅ Firefox 75+
- ✅ Safari 13.1+
- ✅ Edge 80+

### **Mobile**
- ✅ Chrome Android 80+
- ✅ Safari iOS 13.4+
- ✅ Samsung Internet 11+
- ⚠️ Firefox Mobile (limited audio support)

## 🎨 Visual Effects System

### **Holographic Effects**
- **RGB Glitch**: Channel separation with time-based oscillation
- **Moiré Patterns**: Interference patterns with audio reactivity
- **Grid Overlay**: Dynamic opacity based on interaction intensity
- **Blend Modes**: Screen, multiply, overlay, color-dodge layering

### **4D Mathematics**
```glsl
// 4D rotation matrices
mat4 rotateXW(float theta) {
    float c = cos(theta), s = sin(theta);
    return mat4(c,0,0,-s, 0,1,0,0, 0,0,1,0, s,0,0,c);
}

// 4D to 3D projection
vec3 project4Dto3D(vec4 p) {
    float w = 2.5 / (2.5 + p.w);
    return vec3(p.x * w, p.y * w, p.z * w);
}
```

## 📊 Performance Metrics

### **Target Performance**
- **Desktop**: 60 FPS @ 1080p
- **Mobile**: 30-60 FPS adaptive
- **Memory**: <100MB typical usage
- **CPU**: <20% on modern devices

### **Optimization Features**
- Adaptive quality based on device capabilities
- Automatic resolution scaling
- Frame rate monitoring and adjustment
- Memory management for long sessions

## 🔬 Scientific Applications

### **Educational Use**
- 4D geometry visualization
- Audio frequency analysis demonstration
- Real-time mathematics exploration
- Interactive physics concepts

### **Research Applications**
- Multidimensional data visualization
- Audio pattern analysis
- Geometric algorithm testing
- Shader development platform

## 🎪 Creative Applications

### **Live Performance**
- Music visualization for concerts
- DJ visual effects system
- Interactive art installations
- Immersive experience design

### **Content Creation**
- Screen recording for video content
- Social media visual loops
- Digital art creation tool
- Meditation/relaxation visuals

## 🔧 Setup & Installation

### **Quick Start**
1. Clone repository: `git clone https://github.com/domusgpt/active-holographic-systems.git`
2. Open `index.html` in a modern browser
3. Click "🎵 AUDIO" to enable audio reactivity
4. Use controls to explore 30 variations

### **Development Setup**
```bash
# Clone repository
git clone https://github.com/domusgpt/active-holographic-systems.git
cd active-holographic-systems

# Start local server (optional)
python -m http.server 8080
# or
npx serve

# Open browser
open http://localhost:8080
```

### **Mobile Testing**
For microphone permissions on mobile:
1. Serve over HTTPS (required for getUserMedia)
2. Use `ngrok` for quick HTTPS tunneling
3. Accept security warnings for self-signed certificates

## 📜 License

**Private/Proprietary** - Paul Phillips (domusgpt)

## 🤝 Contributing

This is an experimental research project. Contributions welcome:

1. **Geometry Additions**: New mathematical lattice functions
2. **Audio Enhancements**: Improved frequency analysis
3. **Performance Optimizations**: Mobile and low-end device support
4. **Visual Effects**: New shader techniques and blend modes

## 📧 Contact

**Paul Phillips** - phillips.paul.email@gmail.com

---

**🌌 Experience the intersection of mathematics, audio, and visual art through Active Holographic Systems.**