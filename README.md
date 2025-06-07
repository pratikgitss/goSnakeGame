# Snake Game 🐍

A classic Snake game implementation built with Go and the Ebiten game engine.

## Features

- Classic Snake gameplay mechanics
- Smooth movement with configurable game speed
- Food spawning and score system
- Simple, clean graphics
- Cross-platform compatibility

## Prerequisites

- Go 1.19 or higher
- A graphics-capable display (X11/Wayland/Windows/macOS)

## Installation

1. Clone this repository:

```bash
git clone https://github.com/pratikgitss/goSnakeGame.git
cd snake-game
```

2. Install dependencies:

```bash
go mod tidy
```

3. Run the game:

```bash
go run main.go
```

Or build and run:

```bash
go build -o snake main.go
./snake
```

## How to Play

### Controls

- **W** - Move Up
- **S** - Move Down
- **A** - Move Left
- **D** - Move Right

### Objective

- Control the snake to eat red food squares
- Each food eaten makes the snake grow longer
- Avoid colliding with walls or the snake's own body
- Try to achieve the highest score possible!

## Game Mechanics

- **Grid Size**: 20x20 pixels per cell
- **Screen Resolution**: 640x480 pixels
- **Game Speed**: 6 moves per second
- **Growth**: Snake grows by one segment per food eaten
- **Food**: Randomly spawns after each consumption

## Technical Details

### Built With

- **Language**: Go
- **Game Engine**: [Ebiten](https://ebiten.org/) v2.8.8
- **Graphics**: Vector-based rendering
- **Text Rendering**: Go text/v2 with M+ fonts

### Architecture

- `Game` struct implements Ebiten's `Game` interface
- Game loop handles input, updates, and rendering
- Simple collision detection and food spawning system

## Platform Compatibility

### Tested On

- Linux (X11/Wayland/Hyprland)
- Should work on Windows and macOS

### Display Systems

- **X11**: Full native support
- **Wayland**: Works via XWayland compatibility layer
- **Windows**: Native DirectX support
- **macOS**: Native Metal support

## Known Issues

- On Wayland systems, you may see XGB authority warnings - these are harmless and don't affect gameplay
- Game starts in "game over" state by default (intentional for this version)

## Development

### Project Structure

```
.
├── main.go           # Main game implementation
├── go.mod           # Go module definition
├── go.sum           # Dependency checksums
├── .gitignore       # Git ignore rules
└── README.md        # This file
```

### Key Components

- `Point` struct for 2D coordinates
- `Game` struct containing game state
- Movement direction constants
- Update/Draw game loop methods

## Contributing

Feel free to fork this project and submit pull requests for improvements such as:

- High score system
- Sound effects
- Different difficulty levels
- Improved graphics
- Game over/restart functionality

## License

This project is open source. Feel free to use and modify as needed.

## Acknowledgments

- Built with the excellent [Ebiten](https://ebiten.org/) 2D game library
- Uses M+ fonts for text rendering
- Inspired by the classic Nokia Snake game
