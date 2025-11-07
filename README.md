# Chasm - Web MIDI Tracker

A browser-based MIDI tracker and sequencer inspired by Schism Tracker, featuring pattern-based sequencing, real-time MIDI output, and generative music tools.

**This is vibe coded... vibe along or vibe off** 🎵

## Overview

Chasm is a Web MIDI tracker that brings the classic tracker interface to the browser. Create music using pattern-based sequencing, connect to hardware MIDI devices, and experiment with generative ambient compositions.

## Features

### Tracker Features
- **Pattern Editor**: Multi-channel pattern editor with up to 256 channels
- **QWERTY Note Entry**: Schism Tracker-style keyboard note entry (Q=C, W=C#, etc.)
- **MIDI Output**: Connect to hardware synths, drum machines, and samplers via Web MIDI API
- **Web Audio Mode**: Built-in synthesizer with delay, reverb, and filtering
- **Pattern Sequencing**: Create and arrange patterns in a sequence
- **Effect Commands**: Hex-based effect commands (volume, panning, portamento, etc.)
- **Real-time Playback**: Step-based playback with tempo and speed control

### MIDI Synth Library
- Object-oriented abstractions for hardware MIDI devices
- Support for Roland, Behringer, Korg, and Boss devices
- Easy integration with generative MIDI projects

## Getting Started

### Requirements
- Modern web browser with Web MIDI API support (Chrome, Edge, Opera)
- MIDI device (optional, for hardware output)

### Usage

1. Open `index.html` in your browser to see all available tools
2. For tracker: Open `tracker.html` or `tracker3.html` (recommended)
3. Connect your MIDI device:
   - Click "Connect" after selecting your MIDI device from the dropdown
   - Or use Web Audio mode for built-in synthesis
4. Start creating patterns:
   - Use QWERTY keys to enter notes (Q=C, W=C#, E=D, etc.)
   - Use number keys (0-9) to set octave
   - Navigate with arrow keys
   - Press Space to play/stop

## Keyboard Shortcuts

### Note Entry (Schism Tracker Style)
- **Q, W, E, R, T, Y, U, I, O, P, [, ]**: Note entry (C through B)
- **0-9**: Set octave
- **Enter**: Step down to next row
- **Tab**: Move to next channel

### Navigation
- **Arrow Keys**: Navigate cells and fields
- **Space**: Play/Stop playback
- **Delete/Backspace**: Clear cell
- **Ctrl+C/V**: Copy/Paste cell

## Files

### Tracker Versions
- **tracker.html** - Main tracker implementation with MIDI output
- **tracker0.html** - Early version with basic features
- **tracker2.html** - Enhanced version with improved UI
- **tracker3.html** - Advanced version with MIDI + Web Audio dual output modes

### Ambient Generators
- **ambient1.html** - Ambient MIDI Generator v1
- **ambient2.html** - Ambient MIDI Generator v2
- **ambient3.html** - Ambient MIDI Generator v3
- **ambient4.html** - Ambient MIDI Generator v4
- **ambient5.html** - Ambient MIDI Generator v5 (latest)

### Libraries
- **midi-synths.js** - MIDI synth abstraction library with support for:
  - Roland SH-4d, TR-8S, TT-303, SP-404 MK2
  - Behringer TD-3, RD-6, RD-8, RD-9
  - Korg Minilogue XD
  - Boss RC-600

## Pattern Format

Each pattern consists of:
- **64 rows** per pattern
- **Multiple channels** (default 8, expandable to 256)
- **5 fields per cell**:
  - **Note**: Note name (e.g., "C-4", "C#3")
  - **Inst**: Instrument number (hex)
  - **Vol**: Volume (hex, 0x00-0xFF)
  - **Effect**: Effect command (hex)
  - **Param**: Effect parameter (hex)

## Effect Commands

- **0x0C**: Set volume
- **0x0B**: Set panning
- **0x01**: Portamento up
- **0x02**: Portamento down

## Browser Compatibility

- **Chrome/Edge**: Full support
- **Opera**: Full support
- **Firefox**: Limited (no Web MIDI API)
- **Safari**: Limited (no Web MIDI API)

## Technology

- **Vanilla JavaScript** - No frameworks
- **Web MIDI API** - Hardware MIDI communication
- **Web Audio API** - Built-in synthesis and effects
- **HTML5/CSS3** - Modern web standards

## Inspiration

Inspired by [Schism Tracker](https://github.com/schismtracker/schismtracker), a free and open-source reimplementation of Impulse Tracker.

## Fork This!

**Do fork this stuff!** Everything is packed in one HTML file that includes CSS and JS, so it's super easy to vibe with. It's unlicensed (public domain), so do whatever you want with it. And let me know if you make something cool! 🎵

## License

This project is released into the public domain under the [Unlicense](LICENSE). Do whatever you want with it.

## Contributing

Feel free to experiment, modify, and extend the codebase. This is a playground project for exploring Web MIDI and tracker interfaces.

## Notes

- Web MIDI API requires user permission on first use
- Some browsers may require HTTPS for Web MIDI API
- Pattern data is stored in browser memory (not persisted)
- Default pattern size: 64 rows
- Default channels: 8 (expandable to 256)

