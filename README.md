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

### Sudoku Rush: Networked Multiplayer Game
`C++` `Win32` `TCP/UDP` `SQLite` · team of 2 · Mar 2026

Multiplayer Sudoku over a client-server connection: TCP for logins, rooms and chat, and UDP for fast gameplay updates. **I led the client and networking code**, plus the Win32 interface and audio.
▶️ [Watch the demo](https://youtu.be/1zpRgxMpxo0)

### Network Operations Center Internship, Westcon Group
`Cisco Meraki` `Ekahau` · Mar to Aug 2023

Handled support tickets across Cisco Meraki, Palo Alto, Juniper and F5, alerted clients to outages longer than 5 minutes, moved a client's public Wi-Fi login from Facebook to SMS, and co-produced a router and server configuration guide that engineers use.
▶️ [Watch the config guide](https://youtu.be/ap5H1yltEnU)

## 🛠️ Tech stack

<p>
  <img src="https://skillicons.dev/icons?i=cpp,c,cs,opengl,unity,qt,cmake,visualstudio,linux,aws,dart,androidstudio,sqlite,html,git&theme=dark"/>
</p>

<!-- SNAKE: uncomment after the snake workflow has run once
<p align="center">
  <img src="https://raw.githubusercontent.com/BluePiggyKaya/BluePiggyKaya/output/github-snake-dark.svg" alt="contribution snake"/>
</p>
-->

## 📫 Get in touch

Happy to talk about real-time rendering, simulation, or IWSP and internship roles. Email me at **simkah222@gmail.com**.
