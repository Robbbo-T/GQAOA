# 📐 Primary_Topological_OPTOUT

## 🧩 Descripción General

Este módulo contiene los **resultados exportables** de la optimización topológica aplicada a la **estructura primaria** del fuselaje del AMPEL360-BWB-Q100. Incluye:
- Longuerones (stringers)
- Cuadernas (frames)
- Refuerzos estructurales
- Paneles internos rígidos

Estos resultados se derivan de simulaciones iterativas que maximizan la **relación rigidez/peso**, considerando cargas operativas, condiciones límite, y geometría BWB específica.

---

## 🧠 Objetivo

Reducir la masa estructural sin comprometer la integridad estructural ni el cumplimiento con los requisitos de certificación (CS-25, FAR 25, DO-160G).

---

## 🧪 Origen de Datos

- Algoritmos de optimización topológica 3D: SIMP / BESO
- Herramientas: Altair OptiStruct, Ansys Topology Optimization, COMSOL
- Entradas:
  - Condiciones de carga: empuje, presión, aterrizaje
  - Restricciones: geometría BWB, volumen interno, sistemas empotrados
  - Objetivo: masa mínima, rigidez máxima, cumplimiento con modos de pandeo

---

## 📂 Contenido del Módulo

| Archivo / Subcarpeta                     | Descripción                                                                 |
|------------------------------------------|------------------------------------------------------------------------------|
| `raw_outputs/`                           | Archivos de malla 3D exportados (`.obj`, `.stl`, `.bdf`)                    |
| `processed_results/`                     | Modelos limpiados y convertidos en `STEP`, `IGES`, y mapas de densidad      |
| `load_cases/`                            | Cargas de entrada aplicadas durante la simulación                           |
| `design_constraints.json`                | Restricciones geométricas y de manufactura                                  |
| `mass_distribution_map.svg`              | Mapa visual de densidad y masa                                              |
| `README.md`                              | Este documento                                                              |

---

## 🛰️ Estado Cuántico y Ciclo de Vida

- `Estado`: ψ (Ψ) — Resultado simulado, listo para integración digital twin
- `Fase del ciclo`: `2_Design`, `3_Testing`, parcialmente `4_Certification`
- `División Q responsable`: `Q-STRUCTURES`, en colaboración con `Q-HPC`

---

## 🔐 Trazabilidad y Conformidad

| Estándar              | Aplicación específica                                               |
|-----------------------|---------------------------------------------------------------------|
| CS-25 Subpart C       | Resistencia estructural y carga límite                             |
| DO-160G               | Condiciones ambientales simuladas para testing                     |
| ISO 10303-242 (STEP)  | Exportación para CAD y digital twin                                |
| GQOIS Identifier      | `GQOIS-BWBQ100-STRUCT-TOPO-ψ001`                                   |

---

## 🧬 Integración con BOB-DT

Los modelos en esta carpeta alimentan directamente el gemelo digital `BOB-DT` como:
- Datos CAD-ificados para simulación estructural
- Entradas para el submódulo `Skin_Fuselage/`
- Referencia para interfaces `Landing_Gear`, `Cabin_Pax`, y `Hydrogen_Pneumatics_SAF`

---

## 🗂️ Documentos Relacionados

- `Mechanics/Flight_Surfaces_Requirements/README.md`
- `Skin_Fuselage/README.md`
- `Digital_Twin/Docs/2_Design/Structural_Paths_TopOpt.md`
- `Certification/Structural_Loads_TopOpt_Traceability.xlsx`

---

## ✍️ Responsable

- Autor técnico: **Amedeo Pelliccia**
- Unidad de diseño: **Q-STRUCTURES**
- Trazabilidad: GQAOA Tree ↔ `ALI-ATA-53` ↔ `BOB-DT-53-DES-003` (ψ-state)


