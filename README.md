<div align="center">

# Hey, I'm Arghya 👋

### I build AI-powered products, 3D maps and slick web apps, usually against a deadline.

📍 Kolkata, India &nbsp;·&nbsp; 📧 arghyabhattacharjee3@gmail.com

</div>

---

## 👨💻 About me

I'm a builder who likes taking an idea from a blank folder to something people can click, drive and demo. Most of my work sits where **AI agents**, **maps and 3D** and **polished front-ends** meet. I learn fastest by shipping, so a lot of my projects started as hackathon builds (Smart India Hackathon, 24-hour sprints, vibe-coding events) and kept growing afterwards.

**What I care about:**
- **Real logic over demo smoke.** Finora does its money maths deterministically instead of letting an LLM guess numbers. FloodSafe routes with an actual graph algorithm.
- **Showing the work.** Gotham keeps a full provenance chain for every signal. Finora shows its agents planning and judging.
- **Math you can see.** I'm happiest when the geometry, the curves and the equations are visible in the final product, especially in 3D.
- **Taste.** Motion, typography and details matter, and I treat them as part of the product.

## 🔭 What I'm into right now

- Getting multiple AI models (Gemini, ChatGPT, Claude) to collaborate through shared memory
- Browser extensions and MCP tools that give chatbots "hands"
- Flood and terrain modelling for Indian cities
- 3D on the web: depth estimation, voxel engines, globes

---

## 🚀 Featured projects

### 📈 [Gotham India](https://github.com/arghya349/gotham): Signal Intelligence Terminal
> *"The Bloomberg Terminal for India's 90M retail investors."*

Turns raw Indian financial news from 40+ sources into actionable, accuracy-tracked stock signals in under 60 seconds.
- Medallion-style pipeline, from raw news to extracted signals to scored signals
- Full **provenance modal**: click a signal and see exactly which sources produced it
- **Paper-trading sandbox**, **WebSocket** live prices, webhooks and API-key auth (B2B API)
- **10-agent strategy optimizer** and a **5-agent AI trading assistant**
- Closed-loop accuracy tracking, so the system learns how right it was

`Python` `FastAPI` `WebSockets` `LLM agents`

### 🌊 [FloodSafe Kolkata](https://github.com/arghya349/floodsafe-kolkata): 3D flood navigation + AI disaster radio
Raise the simulated water level and watch Kolkata's low-lying neighbourhoods go under, then get a route that avoids them.
- Toggle between a 2D **Leaflet** map and a 3D **Three.js** terrain view
- **Dijkstra's algorithm** over an OpenStreetMap road graph, rerouting around flooded nodes
- A **Gemini-powered emergency radio anchor** that reads live flood state and broadcasts a BBC-style bulletin by speech synthesis
- Synthetic fallback graph so routing never breaks when the Overpass API is rate-limited
- Keyboard-navigable and ARIA-labelled, with a Lighthouse accessibility score above 80

`Three.js` `Leaflet` `OpenStreetMap` `Gemini API` `Vercel`

### 🤝 [Pip AI Room](https://github.com/arghya349/PIP-AGENT): Three chatbots, one team
A Chrome extension where **Gemini (Scout)**, **ChatGPT (Analyst)** and **Claude (Reviewer)** research one question together.
- Shared memory called the **brain**: evidence, hypotheses, stances, findings and tasks
- Five-phase missions: *scope → collect → hypothesise → challenge → conclude*
- Steer live with `@mentions` and export a Markdown report or JSON data
- **No server and no API keys.** It drives the chat tabs you're already signed in to.

`Chrome MV3` `JavaScript` `Service workers` `Multi-agent orchestration`

### 💰 Finora: Your money, finally with a brain
An AI **personal CFO**. Specialist agents plan, compute, get judged, and return an explainable recommendation with **real, deterministic math**. Ask a money question and watch the agents work.

`FastAPI` `Multi-agent LLM` `React` `Vercel`

### 🛰️ TerraSight: Edge-AI for planetary rovers (SIH)
Onboard perception for autonomous rovers. It turns stereo and RGB camera feeds into a live **3D terrain map**, classifies every patch into decision zones and scores it for construction, all without waiting on Earth.

`Python` `FastAPI` `Computer vision` `Robotics`

### 🔌 Toolbridge: A universal tool layer for chatbots
Lets the chatbot you already use in the browser (Gemini, ChatGPT, Claude) call any **MCP tool** on your computer, through an extension and a local bridge.

`Node.js` `Chrome extension` `MCP`

---

## 🧊 My strength: 3D and the math behind it

3D is where I'm strongest. I don't just place models in a scene. I work with the **geometry, linear algebra and calculus** underneath, and I build the pipelines that turn flat inputs (photos, depth maps, map data) into 3D that can be measured.

**Photos → 3D reconstruction** ([3D lab](https://github.com/arghya349/3d1))
- Rebuilds an object from 6 to 10 photos with no AI in the loop. I extract silhouettes, align the views and carve a 3D **signed-distance field**.
- Pulls the surface out with **marching cubes**, then turns it into a point cloud where every surface point has its own `(x, y, z)` coordinate.
- Describes complex shapes with a handful of primitives (ellipsoids, boxes, capsules, cylinders) and expands them into dense geometry by computation instead of typing out thousands of numbers.

**Differential geometry on meshes**
- Builds a wireframe **graph** of a mesh (24 cross-section rings with 16 nodes each) and measures **Gaussian curvature** (angle defect over area) and **mean curvature** (cotangent Laplacian) at every node.
- Computes **curvature and torsion** along every edge, plus the **Euler number** (V − E + F) and the **spectral fingerprint** (lowest eigenvalues of the graph Laplacian) for each shape.
- These measures don't change when a shape is moved or rotated, so two 3D objects can be compared on shape alone.

**Shape matching and refinement**
- Scores a bank of reference models against a reconstruction by how well their outlines overlap, using the share of points within 5 cm as a tiebreaker.
- Weights the closest models with an exponential falloff (a temperature-controlled softmax), then fits the winners onto the reconstruction.
- Reports every decision it made, so the result is explainable.

**Depth and terrain**
- Depth estimation, 360° depth and multi-view depth fusion into 3D scenes.
- **TerraSight** turns stereo and RGB camera feeds into a live 3D terrain map and scores each patch for construction.

**Geometry applied to real problems**
- **FloodSafe:** compares ground elevation to a rising water level and runs **Dijkstra's shortest path** on the road graph, avoiding flooded nodes.
- **Orbital globe:** a scale-accurate Earth (1 unit = 6,371 km) in **Three.js** with cargo routes and live data layers.
- **Moon voxel engine:** voxel terrain generated and rendered in the browser.

**Core toolkit:** vectors, matrices and coordinate transforms · projection and camera models · signed-distance fields · marching cubes · mesh curvature · graph theory and spectral methods · Three.js, WebGL and Blender

---

## 🎨 More things I've made

| Project | Description |
|---|---|
| [**Drip Nation**](https://github.com/arghya349/dripnation) | Streetwear storefront with catalogue, product pages, cart and an admin panel |
| **Annapurna** | QR-code table menu for guests plus a live service board for the kitchen, synced across tabs |
| [**MAAC**](https://github.com/arghya349/MAAC) | Department website with documentation |
| [**3D depth lab**](https://github.com/arghya349/3d1) | Photo-to-3D reconstruction, depth estimation, 360° depth and mesh-curvature analysis (see the 3D section above) |
| **Globe** | Interactive world map with cargo routes |
| **Moon voxel engine** | Voxel terrain engine built with Next.js |
| **AR / VR sandbox** | Immersive web experiments |
| **Kolkata Stem Relief** | Flood model driven from your own Gemini chat, with a relief chat that matches people who need help with people who can give it |

---

## 🛠️ Tech stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

**Frameworks and libraries**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**AI and tooling**
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=anthropic&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT-74AA9C?style=flat-square&logo=openai&logoColor=white)
![Chrome](https://img.shields.io/badge/Chrome_Extensions-4285F4?style=flat-square&logo=googlechrome&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

**Creative**
![Blender](https://img.shields.io/badge/Blender-E87D0D?style=flat-square&logo=blender&logoColor=white)
![DaVinci Resolve](https://img.shields.io/badge/DaVinci_Resolve-233A51?style=flat-square&logo=davinciresolve&logoColor=white)

---

## 📊 GitHub stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=arghya349&show_icons=true&theme=transparent" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=arghya349&layout=compact&theme=transparent" alt="Top languages" />
</p>

## 🤝 Let's connect

I'm open to hackathon teams, collaborations and interesting problems.

📧 [arghyabhattacharjee3@gmail.com](mailto:arghyabhattacharjee3@gmail.com)

---

<div align="center"><sub>Building in public, one sprint at a time. ⚡</sub></div>
