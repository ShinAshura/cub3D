# cub3D

A simple 3D game engine inspired by Wolfenstein 3D, built using raycasting. This project is part of the 42 curriculum and introduces fundamental concepts of graphics programming, including rendering, textures, and player movement.

---

## 📌 Features

* Raycasting-based 3D rendering
* Real-time player movement (WASD controls)
* Camera rotation with keyboard or mouse
* Textured walls and sprites
* Minimap
* Basic collision detection
* Configurable maps via `.cub` files
* Dynamic wall placement during gameplay
* Real-time map modification (wall building mechanic)

---

## 🛠️ Installation

### Prerequisites

* GCC / Clang
* Make
* MiniLibX (provided by 42)

### Clone the repository

```bash
git clone https://github.com/ShinAshura/cub3D.git
cd cub3d
```

### Build the project

```bash
make
```

---

## ▶️ Usage

```bash
./cub3D maps/map.cub
```

### Controls

| Key           | Action                    |
| ------------- | ------------------------- |
| W / A / S / D | Move player               |
| ← / →         | Rotate camera             |
| E             | Place wall (build)        |
| ESC           | Exit game                 |

---

## 🗺️ Map Format (`.cub`)

A valid map file includes:

* Resolution
* Texture paths (NO, SO, WE, EA)
* Floor and ceiling colors
* Map layout (walls = `1`, empty space = `0`, player start = `N/S/E/W`)

Example:

```
NO ./textures/north.xpm
SO ./textures/south.xpm
WE ./textures/west.xpm
EA ./textures/east.xpm

F 220,100,0
C 225,30,0

111111
100001
1000N1
111111
```

---

## 🎥 Demo


![Demo](assets/demo_10fps.gif)


Tool used to convert part of the gameplay to GIF:

```bash
ffmpeg -i demo.mp4 -vf "fps=10,scale=800:-1:flags=lanczos" demo.gif
```

---

## 🧠 Concepts Learned

* Raycasting algorithms
* Graphics rendering basics
* Event handling
* Memory management in C
* Parsing and validation of configuration files

---

## 📜 License

This project is licensed under the MIT License — see the LICENSE file for details.

Originally developed as part of the 42 school curriculum.

---

## 🙌 Acknowledgments

* 42 Network
* MiniLibX library
* Wolfenstein 3D for inspiration
* Developed in collaboration with [Lisa]([https://github.com/username](https://github.com/ft-lisa)
