<p align="center">
  <img src="banner.svg" alt="Sim Kah Yan: C++, OpenGL, Unity, real-time simulation" width="100%"/>
</p>

<p align="center">
  <a href="mailto:simkah222@gmail.com"><img src="https://img.shields.io/badge/Email-simkah222%40gmail.com-0d1630?style=for-the-badge&logo=gmail&logoColor=5eead4"/></a>
  <a href="https://www.linkedin.com/in/kah-yan-sim-3067141a3"><img src="https://img.shields.io/badge/LinkedIn-Kah%20Yan%20Sim-0d1630?style=for-the-badge&logo=linkedin&logoColor=60a5fa"/></a>
  <img src="https://img.shields.io/badge/Open%20to-IWSP%20May%202027-0d1630?style=for-the-badge&logoColor=f472b6"/>
</p>

## 👋 Hi, I'm Kah Yan

I build real-time rendering and simulation software in **C++, OpenGL and Unity (C#)**. I'm a Year 3 Computer Science student at the Singapore Institute of Technology (SIT), in the Real-Time Interactive Simulation (RTIS) degree run with DigiPen. Before that, I studied electronics and mechatronics and worked in a network operations centre, so I like knowing how things work from the hardware up.

- 🚐 **Now:** rendering and simulation developer on **Formula 9**, an autonomous-shuttle fleet training simulator
- 🎓 **Studying:** BSc Computer Science (RTIS), SIT-DigiPen, graduating April 2028
- 🌐 **Before:** Network Operations Center intern at Westcon Group (Cisco Meraki)
- 🔎 **Looking for:** a 1-year Integrated Work Study Programme (IWSP) placement from May 2027

## 🚗 Featured work

### Formula 9: Autonomous Shuttle Fleet Training Simulator
`C++` `Qt` `OpenGL` → `Unity` `C#` · team project · Sep 2026 to now · [repo](https://github.com/axewhy-xy/Formula9)

A training simulator where operators run a fleet of autonomous shuttles through a real Singapore neighbourhood. The team started with a native C++/Qt/OpenGL app and moved to Unity in late October. **I built the city's rendering and the life on its streets, one milestone at a time:**

- **Milestone 1: map renderer and camera** (C++, Qt, OpenGL). Wrote the OpenGL renderer that draws the road network from a road database, with roads coloured by type. Built a camera with pan, cursor-anchored zoom and fit-to-data, and level-of-detail rules that hide minor roads when zoomed out and re-query only when the view changes. Played back an ego vehicle's route from KITTI driving data on the map.
- **Milestone 2: vehicles and vehicle AI** (Unity, C#). Brought textured car, taxi, bus, truck and van models into the city. Drew them with GPU instancing and per-camera frustum culling, so only what a camera can see gets drawn. Traffic follows the backend's simulation when it sends frames. When it doesn't, my fallback driver takes over: it picks routes at junctions, avoids roads with hazards, keeps large vehicles off service roads, and smooths lane changes so cars steer instead of snapping.
- **Milestone 3: pedestrians and pedestrian AI** (Unity, C#). Built a walkable network of pavements beside every road and joined it at junction corners. People cross only at mapped crossings, and at signalled ones only while the traffic they cross has a red light. Each character model is baked into a few walk and idle poses and drawn as batched instances, with no per-person GameObjects, Animators or skinning, so a whole crowd stays cheap to draw.

### Struct Squad: Turn-Based Grid RPG on a Custom C++ Engine
`C++` `OpenGL` `GLSL` `ImGui` `CMake` · team of 9 · Sep 2025 to Apr 2026 · [repo](https://github.com/ethanngyl/Gam200Test)

A turn-based tactics RPG built on our own engine with no commercial game engine: grid movement, A* enemy pathfinding, a procedurally generated map, bosses, skill selection and controller support. **I worked on the graphics, the editor tools and the in-game UI** (113 commits):

- **Renderer:** wrote the OpenGL graphics system with GLSL shaders, textures, and mesh and material handles. Added multiple shaders, the camera system with camera clamping, and text rendering with TrueType fonts.
- **Optimisation:** batched draws by mesh, material and texture, and moved per-object transforms into instanced buffers (an SSBO), so each batch is drawn in one call instead of one call per object.
- **Editor:** built the prefab editor (create, save and place reusable objects) and the editor camera in the ImGui level editor.
- **UI and gameplay polish:** movement and attack range tints, health bars, the skills page, How to Play, win and lose screens, and audio settings.

### Seam Carving: Content-Aware Image Resizing
`Python` `NumPy` `OpenCV` `Streamlit` · team of 6 · Nov 2026 · [repo](https://github.com/R15hika/seam-carving)

An algorithms project that resizes images without squashing what matters, by removing the lowest-energy "seams" of pixels. Three seam finders (dynamic programming, greedy and graph cut) are compared in an interactive demo app. **I owned the dynamic programming seam finder:**

- Wrote the DP recurrence with backtracking, vectorised with NumPy so each row is computed in one step instead of pixel by pixel, plus horizontal seams by reusing the vertical finder on the transposed image
- Made the demo app safer to use: rejects images it can't decode, shows how many seams a resize will remove, warns before slow DP resizes, stops graph cut on images it can't handle, and reports how long each resize took

▶️ [Watch the demo](https://youtu.be/3gPar0sKfHI)

### Sudoku Rush: Networked Multiplayer Game
`C++` `Win32` `TCP/UDP` `SQLite` · team of 2 · Mar 2026

Multiplayer Sudoku over a client-server connection: TCP for logins, rooms and chat, and UDP for fast gameplay updates. **I led the client and networking code**, plus the Win32 interface and audio.
▶️ [Watch the demo](https://youtu.be/1zpRgxMpxo0)

### Network Operations Center Internship, Westcon Group
`Cisco Meraki` `Ekahau` · Mar to Aug 2023

Handled support tickets across Cisco Meraki, Palo Alto, Juniper and F5, alerted clients to outages longer than 5 minutes, moved a client's public Wi-Fi login from Facebook to SMS, and co-produced a router and server configuration guide that engineers use.
▶️ [Watch the config guide](https://youtu.be/ap5H1yltEnU)

## 🛠️ Tech stack

| Area | Tools | Where I used them |
|---|---|---|
| **Languages** | <img src="https://skillicons.dev/icons?i=cpp,c,cs,py,html,dart&theme=dark" height="36"/> | C++ engines and renderers, C# in Unity, Python for algorithms |
| **Graphics & engines** | <img src="https://skillicons.dev/icons?i=opengl,unity,qt&theme=dark" height="36"/> <img src="https://img.shields.io/badge/GLSL-0d1630?style=flat-square&logo=opengl&logoColor=5eead4"/> <img src="https://img.shields.io/badge/ImGui-0d1630?style=flat-square&logo=cplusplus&logoColor=5eead4"/> | OpenGL renderers in Formula 9 and Struct Squad, Unity vehicles and pedestrians |
| **Data & algorithms** | <img src="https://skillicons.dev/icons?i=sqlite&theme=dark" height="36"/> <img src="https://img.shields.io/badge/NumPy-0d1630?style=flat-square&logo=numpy&logoColor=60a5fa"/> <img src="https://img.shields.io/badge/OpenCV-0d1630?style=flat-square&logo=opencv&logoColor=60a5fa"/> <img src="https://img.shields.io/badge/Streamlit-0d1630?style=flat-square&logo=streamlit&logoColor=60a5fa"/> | Map road database, seam carving |
| **Networking & cloud** | <img src="https://skillicons.dev/icons?i=aws&theme=dark" height="36"/> <img src="https://img.shields.io/badge/Cisco%20Meraki-0d1630?style=flat-square&logo=cisco&logoColor=f472b6"/> <img src="https://img.shields.io/badge/TCP%2FUDP-0d1630?style=flat-square&logo=socketdotio&logoColor=f472b6"/> <img src="https://img.shields.io/badge/Ekahau-0d1630?style=flat-square&logo=wifi&logoColor=f472b6"/> | Westcon internship, Sudoku Rush |
| **Tools** | <img src="https://skillicons.dev/icons?i=git,github,cmake,visualstudio,linux,androidstudio&theme=dark" height="36"/> | Team repos with branches and pull requests, CMake builds |

<!-- SNAKE: uncomment after the snake workflow has run once
<p align="center">
  <img src="https://raw.githubusercontent.com/BluePiggyKaya/BluePiggyKaya/output/github-snake-dark.svg" alt="contribution snake"/>
</p>
-->

## 📫 Get in touch

Happy to talk about real-time rendering, simulation, or IWSP and internship roles. Email me at **simkah222@gmail.com**.
