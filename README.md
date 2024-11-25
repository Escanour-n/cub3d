# 🕹️ Cub3D  

**Cub3D** is a 42 Network project that introduces the fundamentals of 3D game engines. Inspired by *Wolfenstein 3D*, this project challenges you to build a raycasting engine to render a 3D world on a 2D plane.  

---

## 🌟 Features  
- **3D rendering** using raycasting.  
- **Player mechanics**: walking, strafing, and rotation.  
- **Collision detection** to prevent walking through walls.  
- **Texture mapping** for walls, floors, and ceilings.  
- Configurable via `.cub` files to define the map and settings.  
- **MiniLibX** integration for graphics rendering.  

---

## 🚀 Getting Started  

### Prerequisites  
- **Operating System**: Linux or macOS.  
- **Libraries**:  
  - [MiniLibX](https://harm-smits.github.io/42docs/libs/minilibx/getting_started.html).  
  - Math library (`-lm`).  
- **Compiler**: GCC or Clang.  

### Installation  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/cub3d.git
   cd cub3d

2. Build the project:  
   ```bash
   make

3. Build the project:  
   ```bash
   ./cub3d path/to/map.cub

## 🎮 Controls  

| **Key**            | **Action**                 |
|---------------------|----------------------------|
| `W` / `A` / `S` / `D` | Move forward, backward, and strafe |
| `←` / `→`           | Rotate the camera          |
| `ESC`               | Exit the game             |


## 🗺️ Map Format (`.cub`)  

The `.cub` file is a configuration file that defines the game's map, textures, and colors.  

### **Format Requirements**  
1. **Map Structure**:  
   - The map must be rectangular and fully surrounded by walls (`1`).  
   - The player starting position (`N`, `S`, `E`, `W`) must be defined on the map.  

2. **Map Elements**:  
   - `0`: Empty space.  
   - `1`: Wall.  
   - `2`: Sprite (e.g., collectible or enemy).  
   - `N`, `S`, `E`, `W`: Player starting position and orientation.  

3. **Texture and Color Definitions**:  
   - `NO`, `SO`, `WE`, `EA`: File paths for wall textures.  
   - `F`: Floor color in RGB format (e.g., `220,100,0`).  
   - `C`: Ceiling color in RGB format (e.g., `225,30,0`).  

### Example `.cub` File  

```plaintext
NO ./textures/north_wall.xpm
SO ./textures/south_wall.xpm
WE ./textures/west_wall.xpm
EA ./textures/east_wall.xpm
F 220,100,0
C 225,30,0

111111
100001
1000N1
100001
111111
