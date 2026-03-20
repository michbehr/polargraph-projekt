PROJEKT-ZIEL – ABLAUFPLAN (neu gespeichert)
Befehl „Projekt-Ziel Ablauf“ ruft diesen Plan ab.
Phase 1: Vektor-only (GH-nativ, einfach)
1.	Preferences-Cluster bauen (Papier/Canvas/Offsets/Feeds/Limits).
2.	Vector-Formen erzeugen (Linien/Kurven).
3.	Branches für Werkzeug/Layer-Auswahl.
4.	GCode mit Startsequenz, PenUp-Logik, M0-Pausen.
5.	Pronterface einrichten (USB, Makros).
6.	Test: Kleiner Plot → Nullpunkt prüfen.
Phase 2: Pixel-only (GH-Standard)
1.	Image Sampler + Basis-Bearbeitung (Resize/Threshold).
2.	Plugins einführen (food4Rhino: ImageTools, Weaverbird?).
3.	Branches für Effekte/Werkzeug.
4.	GCode → Pronterface → Plot.
Phase 3: Hybrid Pixel+Vektor
1.	Kombi-Test (Stipples + Vektor + Logo, Multi-Pen).
2.	Performance messen/optimieren (Downsampling, Caching).
3.	GCode → Pronterface → Plot.
Phase 4: Makelangelo-Filter (fortgeschritten)
1.	Standard-Filter nachbauen (Threshold/Blur/Edge aus GitHub).
2.	Eigene Filter (basierend auf Makelangelo).
3.	Auslagern (externe .py-Module mit NumPy/OpenCV).
4.	GCode → Pronterface → Plot.
Ergänzte Lücken (nicht vergessen!)
•	Jeder Phase: Unit-Tests (GCode-Validierung, Limits-Check).
•	Phase 2: Plugins prüfen: ImageTools (ShapeDiver), Human (food4Rhino).[shapediver]
•	Phase 3: Layer-Management (DataTree pro Stift).
•	Global: Error-Handling (Out-of-Bounds), Versionskontrolle (.gh als Git).