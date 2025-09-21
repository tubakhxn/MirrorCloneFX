# MirrorCloneFX

A real-time computer vision application that creates stylized clones of yourself using your webcam. Control different visual effects with simple hand gestures powered by MediaPipe and OpenCV.

## Features

- **Split-screen view**: Original webcam feed on the left, stylized clone on the right
- **Hand gesture controls**: Use MediaPipe hand tracking to switch between effects in real-time
- **Multiple visual styles**:
  - **Dots**: Stippled dot rendering with variable sizes
  - **Lines**: Edge outline rendering with enhanced colors
  - **ASCII**: Text character art using Unicode block characters
  - **Particles**: Dynamic swirling particles that follow your movement with physics

## Hand Gestures

| Gesture | Effect | Description |
|---------|--------|-------------|
| Two fingers (peace sign) | Dots | Creates a stippled dot version using original colors |
| One finger up | Lines | Shows edge outlines and contours with glow effect |
| Thumb + pinky out | ASCII | Renders you as ASCII art with color-coded intensity |
| Open palm (all fingers) | Particles | Generates physics-based particles following hand movement |

## Installation

### Prerequisites
- Python 3.7 or higher
- Webcam connected to your computer
- Good lighting conditions for optimal hand detection

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/tubakhxn/MirrorCloneFX.git
   cd MirrorCloneFX
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python main.py
   ```

## Usage

1. **Position yourself in front of your webcam** with good lighting
2. **Keep your hand visible** to the camera for gesture detection
3. **Use hand gestures** to switch between visual effects
4. **Press 'q'** to quit the application

The current mode is displayed in the top-left corner of the window.

## Technical Details

### Architecture
- **OpenCV**: Webcam capture and real-time image processing
- **MediaPipe**: Hand landmark detection and gesture recognition
- **NumPy**: Numerical computations for visual effects

### Visual Effects Implementation
- **Dots**: Intensity-based circle rendering with variable sizes
- **Lines**: Canny edge detection with enhanced color mapping
- **ASCII**: Unicode block character mapping with color-coded intensity levels
- **Particles**: Physics-based particle system with gravity and momentum

### Performance
- Runs at 30 FPS on most modern hardware
- Real-time hand tracking with 21 landmark points
- Optimized algorithms for smooth visual transitions

## Requirements

### System Requirements
- **OS**: Windows, macOS, or Linux
- **Python**: 3.7 or higher
- **RAM**: 4GB minimum (8GB recommended)
- **CPU**: Multi-core processor recommended
- **Webcam**: Any USB or built-in camera

### Dependencies
- `opencv-python>=4.5.0` - Computer vision and image processing
- `mediapipe>=0.8.9` - Hand tracking and gesture recognition  
- `numpy>=1.21.0` - Numerical computations for image effects

## Contributing

We welcome contributions to MirrorCloneFX! Here's how you can help:

### Ways to Contribute
- **Bug Reports**: Found a bug? Open an issue with detailed steps to reproduce
- **Feature Requests**: Have an idea for a new visual effect? Share it in the issues
- **Code Contributions**: Submit pull requests for bug fixes or new features
- **Documentation**: Help improve documentation and examples
- **Testing**: Test on different platforms and report compatibility issues

### Development Setup

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/MirrorCloneFX.git
   cd MirrorCloneFX
   ```
3. **Create a new branch** for your feature:
   ```bash
   git checkout -b feature-name
   ```
4. **Install development dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
5. **Make your changes** and test thoroughly
6. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add your descriptive commit message"
   ```
7. **Push to your fork**:
   ```bash
   git push origin feature-name
   ```
8. **Create a Pull Request** on GitHub

### Code Style Guidelines
- Follow PEP 8 Python style guide
- Add docstrings for new functions and classes
- Include comments for complex algorithms
- Test your changes before submitting
- Ensure compatibility with Python 3.7+

### Adding New Visual Effects

To add a new visual effect:

1. **Create a new method** in the `MirrorCloneFX` class:
   ```python
   def create_your_effect(self, frame):
       """Create your custom visual effect"""
       # Your implementation here
       return processed_frame
   ```

2. **Add the effect to the modes dictionary**:
   ```python
   self.modes = {
       0: "Dots",
       1: "Lines", 
       2: "ASCII",
       3: "Particles",
       4: "YourEffect"  # Add your effect
   }
   ```

3. **Update the gesture detection** to include your effect
4. **Test thoroughly** with different lighting conditions
5. **Update documentation** with the new gesture and effect

### Reporting Issues

When reporting issues, please include:
- **Operating System** and version
- **Python version**
- **Steps to reproduce** the issue
- **Expected vs actual behavior**
- **Screenshots or videos** if applicable
- **Error messages** (full traceback)

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- **MediaPipe** team for excellent hand tracking capabilities
- **OpenCV** community for comprehensive computer vision tools
- **Python** community for the amazing ecosystem

## Troubleshooting

### Common Issues

**Camera not detected**
- Ensure webcam is connected and not used by another application
- Try different USB ports
- Check camera permissions in system settings

**Hand gestures not working**
- Ensure good lighting conditions
- Keep hand clearly visible and within camera frame
- Try adjusting distance from camera (arm's length works best)
- Make sure gestures are held steady for 1-2 seconds

**Performance issues**
- Close other applications to free up CPU/memory
- Ensure adequate lighting to reduce processing overhead
- Try lower resolution if available in your camera settings

**Installation errors**
- Verify Python 3.7+ is installed: `python --version`
- Update pip: `pip install --upgrade pip`
- Install dependencies one by one if batch install fails

### Platform-Specific Notes

**Windows**
- May require Visual C++ redistributables for OpenCV
- Use Command Prompt or PowerShell for installation

**macOS**
- May need to grant camera permissions in System Preferences
- Use Terminal for installation commands

**Linux**
- May need additional packages: `sudo apt-get install python3-opencv`
- Ensure camera drivers are properly installed

## Customization

### Modifying Visual Effects

You can customize the visual effects by editing the corresponding methods:

**Dots Effect** (`create_dots_effect`)
- Adjust `dot_spacing` for density
- Modify `radius` calculation for dot sizes
- Change color enhancement factor

**Lines Effect** (`create_lines_effect`)
- Modify Canny edge detection parameters
- Adjust color enhancement multiplier
- Change glow effect intensity

**ASCII Effect** (`create_ascii_effect`)
- Change `self.ascii_chars` for different character sets
- Adjust `char_width` and `char_height` for spacing
- Modify color thresholds

**Particles Effect** (`create_particles_effect`)
- Adjust `max_particles` for density
- Modify physics parameters (gravity, velocity)
- Change particle lifetime and appearance

## Star History

If you find this project useful, please consider giving it a star on GitHub!

## Connect

- **GitHub**: [tubakhxn](https://github.com/tubakhxn)
- **Issues**: [Report bugs or request features](https://github.com/tubakhxn/MirrorCloneFX/issues)
- **Discussions**: [Community discussions](https://github.com/tubakhxn/MirrorCloneFX/discussions)