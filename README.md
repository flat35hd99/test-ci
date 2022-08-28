[![kibot](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/kibot.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/kibot.yml)
[![platformio](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/platformio.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/platformio.yml)
[![reuse](https://github.com/nerdyscout/KiCAD-CICD-Template/actions/workflows/reuse.yml/badge.svg)](https://github.com/nerdyscout/KiBot-CICD-Template/actions/workflows/reuse.yml)

---

# KiCAD-CICD-Template

This repository provides different CI/CD workflows used for projects using [KiCAD](https://www.kicad.org/) and [PlatformIO](https://www.platformio.org).

## workflows

### KiBot

[KiBot](https://github.com/INTI-CMNB/KiBot/) is used to generate all kind of documentation from a KiCAD6 project.

Whenever a file matching `pcb/*.kicad_*` changes this workflow will trigger.

The following documents are generated on every build:

```
- pcb/cad/
   - dxf/
      - AutoCAD - DXF
   - boardview - BRD
   - 3D render - STEP
- pcb/docs/
   - bom/
      - Interactive BOM - HTML
      - Octopart list - CSV
      - KiCost - XLSX (disabled)
   - schematic - PDF
- pcb/img/
   - pcb/$fab/$style/
      - PCB top - SVG
      - PCB bottom - SVG
   - render/ (disabled)
      - PCB render - PNG
   - schematic - SVG
- pcb/gerbers - ZIP
```

### PlatformIO

used to rebuild your source code whenever it changes.

### REUSE

used to insure every file got a propper license. 

## getting started

- [x] hit the "use this template" button and give your project a name
- [x] clone this new repository localy
- [x] replace content of README.md
- [x] Code
   - [x] put your code in the `src/` folder using platformio
- [x] PCB
   - [x] change the filenames in `pcb/*.kicad_*` matching your repository name
   - [x] create your PCB
- [x] run `reuse --lint`
   - [x] make sure the licenses of `pcb/*` fits your needs
   - [x] make sure the licenses of `src/*`, `include/*`, `lib/*`, `test/*` fits your needs
- [x] commit and push all those changes regulary to your project
