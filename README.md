Here is a polished, professional, and visually appealing version of the `README.md` that combines your original project reflections with the detailed technical design document you provided. The video link has been removed, and the formatting has been significantly upgraded.

---

```markdown
# 🚀 2D Battle Tank Game

<p align="center">
  <img src="https://user-images.githubusercontent.com/33335169/57844679-66c43080-7785-11e9-9806-1d28ee0a95c0.png" alt="Tanks Logo" width="80%"/>
</p>

> A local multiplayer 2D tank battle game focused on responsive movement, strategic shooting, and balanced gameplay. 

This project was developed following the [Unity's Tanks tutorial](https://unity3d.com/learn/tutorials/s/tanks-tutorial). It serves as a major milestone in my game development journey, allowing me to familiarize myself with the Unity engine, physics, and C# scripting.

---

## 🎮 Gameplay & Core Mechanics

The game is designed as a head-to-head arena battle where each player controls an individual tank using separate keyboard inputs. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/33335169/57844714-793e6a00-7785-11e9-9067-44036ca1d0bf.png" alt="Tanks Gameplay" width="80%"/>
</p>

### ✨ Features Implemented
* **Local Multiplayer:** Two-player combat with independent movement controls (forward/backward and rotation).
* **Physics-Based Movement:** Smooth motion and collisions powered by Unity's Rigidbody physics.
* **Strategic Shooting:** A charge-based firing system. Holding the fire button increases the projectile launch force, forcing players to balance charge time and accuracy.
* **Dynamic Camera:** An orthographic camera that automatically centers between active players and adjusts the zoom level to keep all tanks visible.
* **Damage System:** Area-of-effect (AoE) explosions where damage decreases based on the tank's distance from the explosion's center.
* **Round Management:** Automatic round winner detection, health management, and game restart functionality.
* **Audiovisual Polish:** Custom engine sounds (varying pitch for idle/moving), dynamic UI text that matches the player's tank color, and explosive particle effects.

---

## 🧠 Development Journey

### What Went Well
Months ago, I attempted to create a tower defense game but gave up when I couldn’t get my enemy spawner to work correctly (and since I didn't use GitHub for version control back then, I couldn't easily revert my project! 👀). 

This Tanks game uses a Game Manager to spawn the tanks in their predefined arena locations every round. Successfully getting the spawner and Game Manager to work this time around was a huge win and shows my growth. It makes me excited to return to previous tutorials now that I have more knowledge.

### What Went Wrong
When testing the game halfway through development, my tank was getting instantly demolished when I dropped a projectile on it. The game is designed so that shooting a projectile from further away deals less damage, but no matter the distance, the whole tank would just explode and disappear. After debugging the tank health and shooting scripts, I eventually found and fixed the bug inside the shell explosion script.

### What I Learned
* **Asset Management:** As my second successful game tutorial, I got to use professional assets provided by Unity, stepping up from the basic 3D primitives I used in previous projects like [Cube Run](https://github.com/xixi743/Cube-Run).
* **Audio Mixing:** Audio mixing was entirely new to me. I learned how to make the background music "duck" so that important sound effects come through clearly.
* **Dynamic Feedback:** It was fascinating to learn how to tie visual/audio feedback to specific objects. For example, each tank has a different pitched driving sound, and the UI dynamically updates to match the color of the winning player's tank.

---

## 🏗️ Technical Details & Future Roadmap

While the game is fully playable and demonstrates a solid foundation, I have identified several areas for potential expansion and optimization.

### 🛠️ Known Issues (Technical Debt)
* **Input System:** The project currently uses Unity's legacy Input Manager instead of the newer Input System.
* **Performance:** Shells and explosion effects are instantiated and destroyed repeatedly. During extended gameplay, this could impact performance compared to using Object Pooling.
* **Static Environment:** Environmental objects and obstacles are static and cannot be destroyed.
* **Code Architecture:** Some scripts assume all required components are assigned (desirable to add null checking), and some duplicate scripts could be refactored for better maintainability.

### 🚀 Future Improvements
* **Gameplay Additions:** Add multiple tank classes (varying speed, health, damage), power-ups (health recovery, speed boosts), and AI-controlled opponents for a single-player mode.
* **User Experience:** Implement a tank selection menu, add multiple maps with different layouts, and upgrade the UI with health bars and a mini-map.
* **Technical Upgrades:** Migrate to Unity's New Input System, implement Object Pooling for projectiles/particles, and replace deprecated Unity APIs with modern alternatives.

---

*I'm currently very happy with the complete feel of this game and plan to leave it as-is to serve as a benchmark of my early Unity learning, though I may return to squash bugs as needed!*

```