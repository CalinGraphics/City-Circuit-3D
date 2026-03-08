# 🏙️ City Circuit 3D

> O scenă WebGL completă cu un circuit stradal nocturn, clădiri, mașini AI și iluminare dinamică — rulează direct în browser, fără instalare.

---

## 🎮 Demo

Deschide `index.html` direct în browser. Nu necesită server, nu necesită build.

---

## 🕹️ Controale

| Tastă | Acțiune |
|-------|---------|
| `W` | Accelerație |
| `S` | Frână / marșarier |
| `A` / `D` | Viraj stânga / dreapta |
| `Q` / `E` | Cameră sus / jos |
| `R` | Resetează mașina la poziția de start |
| `Mouse drag` | Orbită cameră liberă în jurul scenei |

---

## 🌆 Ce conține scena

- **Circuit oval nocturn** cu relief și pistă asfaltată texturată
- **4 mașini AI** care circulă autonom pe circuit cu culori distincte
- **Mașina jucătorului** (albastru) — controlabilă complet
- **Clădiri procedurale** dispuse în jurul circuitului cu textură de ferestre
- **Parc central** cu copaci generați procedural
- **14 stâlpi de iluminat** cu LED strip portocaliu și spotlight dinamic
- **Skybox panoramic** cu cer nocturn / Milky Way (equirectangular)
- **Sistem de coliziuni** cu clădiri, copaci și stâlpi — resetare automată cu banner
- **HUD** cu viteză în timp real (km/h) și lista controalelor

---

## 📁 Structură fișiere

```
/
├── index.html          # Toată logica jocului (Three.js, WebGL)
├── textures/
│   ├── sky.jpg         # Skybox panoramic (equirectangular)
│   ├── asphalt.jpg     # Textură pistă
│   ├── building.jpg    # Textură ferestre clădiri
│   └── tree_leaves.jpg # Textură frunze copaci
├── models/
│   ├── drone.glb       # Model 3D dronă
│   └── 25042_Perseverance.glb  # Model 3D rover
└── README.md
```

> ⚠️ Texturile și modelele trebuie să fie în folderele `textures/` și `models/` relative la `index.html`. Fără ele, scena folosește fallback-uri procedurale generate din canvas.

---

## 🛠️ Tehnologii folosite

- [Three.js r128](https://threejs.org/) — rendering WebGL 3D
- `OrbitControls` — control cameră cu mouse
- Canvas API — generare procedurală de texturi fallback
- Vanilla JS / HTML5 — zero dependențe de build

---

## 🚀 Cum rulezi local

```bash
# Clonează repo-ul
git clone https://github.com/USERNAME/city-circuit-3d.git
cd city-circuit-3d

# Deschide direct în browser
open index.html

# SAU pornește un server local (recomandat pentru texturi)
npx serve .
# sau
python -m http.server 8080
```

---

## 📸 Features tehnice

- **Shadow mapping** (PCFSoft) pe toate obiectele
- **SpotLight** dinamic per stâlp de iluminat
- **Box3 hitbox collision** pentru clădiri, copaci și stâlpi
- **Procedural terrain** cu funcție de înălțime customizată
- **Equirectangular skybox** mapping
- **requestAnimationFrame** loop cu delta-time fix

---

## 📝 Licență

Proiect realizat în cadrul cursului **Sisteme de Grafică pe Calculator (SPG)**.  
Liber de utilizat în scop educațional.
