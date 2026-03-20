Projekt-Ziel – Erweitert mit Vektor + Hybrid-Features gespeichert:
PROJEKT-ZIEL (Final) – Alle Rahmenbedingungen
Ziel: GCode-Generierung für Marlin Polargraph in Rhino/Grasshopper/GHPython.
INPUTS & FEATURES
•	Pixelbasiert: Makelangelo-Filter (Threshold/Blur/Edge/Quadtree) als externe Python-Module → Stippling/Hatch.
•	Vektorbasiert: GH-native Geometrie (Linien/Kurven) → Technische Zeichnungen/Logos.
•	HYBRID: Pixel + Vektor kombinieren (z.B. Stipples + saubere Linien + Logo) – ein GCode, ein Nullpunkt.
STIFTWEchsel (Multi-Pen)
•	Automatische Pausen: Nach Layer 1 → Park → `M0` (Pause für Stiftwechsel).
•	Layer-Reihenfolge: Stipples → Technik → Logo.
•	GCode-Beispiel:

; Layer 1: Stipples (schwarzer Stift)
[...stipple paths...]
M0 (Stiftwechsel zu blau)
; Layer 2: Technik 
[...vector paths...]
M0 (Stiftwechsel zu rot) 
; Layer 3: Logo
[...logo paths...]



STANDARD-STARTSEQUENZ

G90 G21 G92 X0 Y0 M280 P0 S90 G4 P500 G1 F2000
; Layer 1: [Name] ([Stiftfarbe])



ANSTEUERUNG
•	Pronterface → `M0` → Stiftwechsel → `Resume`.
Speicherbestätigung: Vektor/Hybrid/Multi-Pen integriert. Alles kompakt.