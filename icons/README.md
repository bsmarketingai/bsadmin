# BSADMIN – ikony

Zdroj: Tabler Icons (MIT), github.com/tabler/tabler-icons, grid 24 px, tah 2 px (v UI 1,75).

- `outline/` – 158 ikon, `filled/` – 45 ikon (solid varianta, kde existuje; jinak fallback na outline).
- `../icons.js` – všechny ikony + web komponenta `<bs-icon name size level color stroke variant>`.
  - `level="2"` = hlavní CTA (viditelné v I2 a I3), `level="3"` = doplňkové (jen I3), `level="1"` = vždy.
  - Globální přepínač: `bsSetIcons(level, "outline" | "filled")`.

Kategorie výběru: navigace a akce, stavy a notifikace, data a čas, e-commerce a doprava, finance, produkty a katalog, systém a infrastruktura, komunikace, značky.
