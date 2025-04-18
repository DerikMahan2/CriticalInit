# 🛠️ Critical Init – Dev Log  
[📋 View Task Checklist](dev-weekly-checklist.md)

---

<details>
<summary>📅 Week 1</summary>

### 🗓️ Day 1 – Initial Setup  
## Completed: April 16, 2025

✅ **What was accomplished:**
- Created Unity project using Universal 2D template  
- Set up folder structure under `Assets/`  
- Implemented `GameManager.cs` with Singleton pattern  
- Verified `InitializeGame()` logs in Console  
- Successfully committed and pushed initial version

🧠 **Reflection:**  
Solid foundation laid — resolved OneDrive conflicts, Git is clean, and Unity runs perfectly. A great launch day.

🔗 [View Task List](dev-weekly-checklist.md#📅-day-1--initial-setup)

---

### 🗓️ Day 2 – Player Setup & Input  
## Completed: April 18, 2025

🛠️ **In Progress:**  
- [X] Add placeholder Player GameObject  
- [X] Add Rigidbody2D + Collider components  
- [X] Create and attach movement script  
- [X] Test directional input (WASD or arrows)

🧠 **Reflection:**  
Today I completed the full player setup and movement input system. The player object moves smoothly using both WASD and arrow keys, and stops immediately when input is released. Setting gravity to zero for a top-down perspective was the right call and aligns perfectly with the vision of creating a tactical, grid-based D&D-inspired experience. The current system provides a strong foundation to expand into turn-based or tile-based movement later. Overall, very happy with how responsive and clean the input feels at this stage.

🔗 [View Task List](dev-weekly-checklist.md#📅-day-2--player-setup--input)

---

### 🗓️ Day 3 – Camera Follow & Scene Polish  
## Completed: April 18, 2025

✅ **What was accomplished:**
- Implemented `CameraFollow` script to track Player smoothly
- Assigned Main Camera to follow Player using `LateUpdate()` with Lerp
- Created a large background using a colored Sprite for visual grounding
- Adjusted sorting layer to layer visuals correctly
- Pressing play shows smooth camera tracking and movement responsiveness

🧠 **Reflection:**  
Very productive session! Movement and camera now feel polished and tight — it’s starting to resemble a real D&D-style top-down map. This puts us in a great place for layering in scene transitions or game state systems next.

🔗 [View Task List](dev-weekly-checklist.md#📅-day-3--camera-follow--scene-polish)

---
</details>