# Axiometa Binary Clock - ESPHome Edition

A ESPHome configuration for the [Axiometa Binary Clock](https://www.axiometa.io/products/binary-clock). This project transforms the hardware into a fully integrated smart home device, allowing for deep customization of animations, colors, and Home Assistant automation.

---

## ✨ Features

- **Binary Time Display**: 18-LED layout (Hours, Minutes, Seconds).
- **Multiple Modes**:
  - `Rainbow Binary Clock`: Active bits cycle through a vibrant rainbow.
  - `Inverse Rainbow`: Background cycles rainbow while time bits stay dark.
  - `Solid Binary Clock`: Fully customizable colors for Hours, Minutes, and Seconds.
- **Home Assistant Integration**:
  - Real-time brightness control.
  - 12-hour / 24-hour format toggle.
  - Status monitoring and OTA updates.
- **Hardware Feedback**: Dedicated WiFi status LED (Green = Connected, Red = Disconnected).
- **Reliability**: Automatic NTP time synchronization with local timezone support.

---

## 🚀 Getting Started

### 1. Prerequisites
- **Hardware**: Axiometa Binary Clock (or any ESP32-S3 with 18 WS2812B LEDs).
- **Software**: [ESPHome](https://esphome.io/) installed locally or via Home Assistant.

### 2. Configuration
1. Clone this repository.
2. Copy `secrets.yaml.example` to `secrets.yaml`.
3. Fill in your WiFi credentials and preferred passwords in `secrets.yaml`.

### 3. Flashing
Connect your device and run:
```bash
esphome run Binary-Clock.yaml
```

---

## 🛠️ Hardware Specification
- **Microcontroller**: ESP32-S3
- **LEDs**: 18x WS2812B (RGB)
- **Pins**:
  - Display LEDs: `GPIO1`
  - WiFi Status LED: `GPIO21`

---

## 🗺️ Roadmap / Future Features

- [ ] **Smooth Transitions**: Implement fade-in/fade-out animations when switching between clock modes.
- [ ] **Enhanced Animations**: Add "Matrix" style drops, pulse effects, and particle-based time transitions.
- [ ] **Native Color Pickers**: Replace global RGB variables with native ESPHome `color` components (or similar) for intuitive adjustment in Home Assistant.
- [ ] **Custom Themes**: Preset color palettes?

---

## 🤝 Contributing
Feel free to fork this project and submit Pull Requests! Whether it's a new animation or an optimized lambda, all contributions are welcome.

## 📄 License
This project is open-source. Please refer to the original hardware manufacturer [Axiometa](https://www.axiometa.io/) for hardware-specific inquiries.
