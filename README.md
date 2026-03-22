# Compose — A Modern Music Notation Engine (WIP)

Compose is a modern, modular music‑notation engine built to render, layout, and eventually edit musical scores.  
It aims to provide a clean, understandable foundation for engraving, MusicXML parsing, and interactive score editing.

---

## 🎯 Project Purpose

Compose exists to solve one problem:  
**make music‑notation software easier to build, extend, and understand.**

Most existing notation engines are large, legacy codebases. Compose starts fresh with:

- A clean data model  
- A predictable layout engine  
- A renderer designed for the modern web  
- A step‑by‑step roadmap toward full editing and playback  

---

## 🚀 Features (Current & Planned)

### ✔️ Implemented (v0.1)
- Core project structure  
- Basic score model (Score → Part → Measure → Voice → Note)  
- SMuFL font loading (Bravura recommended)  
- Staff + notehead rendering  
- Fixed‑spacing layout prototype  

### 🔧 In Progress
- MusicXML (read‑only) importer  
- Hit‑testing for selecting notes  
- Dynamic spacing engine  

### 🛠️ Planned
- Beams, ties, slurs  
- Multi‑voice alignment  
- Editing tools (note input, erase, articulation palette)  
- Playback engine (MIDI/WebAudio)  
- Export to MusicXML and PDF  

---

## 🧱 Architecture

Compose is divided into three clear layers:

### 1. **Model Layer**
Pure data structures for musical concepts:
- Notes, rests, durations  
- Measures, voices, parts  
- Clefs, key signatures, time signatures  

No rendering logic lives here.

### 2. **Layout / Engraving Layer**
Responsible for:
- Horizontal spacing  
- Vertical alignment  
- Collision avoidance  
- Glyph placement  
- Mapping musical time → page coordinates  

This is the core “engraving brain.”

### 3. **Rendering Layer**
Outputs the final score using:
- **SVG** (preferred for crisp vector output)  
- or **Canvas** (for interactive editing performance)

---

## 📁 Project Structure

compose/
│
├── src/
│   ├── model/          # Notes, measures, parts, score
│   ├── layout/         # Spacing, engraving rules
│   ├── render/         # SVG/Canvas drawing
│   ├── io/             # MusicXML import/export
│   └── ui/             # (Future) Editing tools + interactions
│
├── fonts/              # SMuFL music fonts (Bravura, Leland, etc.)
├── examples/           # Sample scores + demos
└── README.md

---

## 📝 Getting Started

### Requirements
- Node.js  
- A SMuFL music font (Bravura recommended)

### Install
```bash
npm install
```

### Run Dev Server
```bash
npm run dev
```

### Build
```bash
npm build
```
---
## 🤝 Contributing

Contributions are welcome. Areas that need help:
- Engraving algorithms
- MusicXML parsing
- UI/UX for editing
- Playback engine design

Open an issue or submit a PR.