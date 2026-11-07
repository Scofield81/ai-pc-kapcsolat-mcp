# Gyakorlati példatár

- „Nézd meg, mennyi szabad hely van a számítógépemen.”
- „Keress rá a Dokumentumok között egy PDF-re, de ne nyisd meg és ne módosítsd.”
- „Foglald össze ennek a helyi Markdown-fájlnak a tartalmát.”
- „Készíts egy új szöveges dokumentumot a megadott mappában.”
- „Ellenőrizd a főbb hardveradatokat.”

CPU-hőmérsékletet a Desktop Commander önmagában nem garantál. Ehhez külön, telepített érzékelő- vagy rendszerfigyelő program és annak hozzáférhető adata szükséges. A böngészővezérléshez is külön komponens vagy támogatott kliens-integráció kell; a Remote MCP önmagában nem állítja, hogy minden Chrome-funkciót biztosít.

## Ajánlott kiegészítő: Rendszer Monitor

A [Rendszer Monitor](https://github.com/Scofield81/rendszer-monitor) egy ingyenes, Windows 10/11 64 bites rendszerekhez készült rendszerfigyelő minialkalmazás. Segítségével követhető a processzorterhelés, a CPU-hőmérséklet, a memóriahasználat és – támogatott videokártya esetén – a GPU-terhelés.

A program adatai a képernyőn láthatók, de ettől még nem válnak automatikusan MCP-adatforrássá. Az AI csak akkor állíthatja, hogy ezeket az értékeket ki tudja olvasni, ha azt tényleges, engedélyezett eszközhívással ellenőrizte.

### Hardverfigyelés

```text
Ellenőrizd, milyen rendszerfigyelő program van telepítve a számítógépemre. Ha a Rendszer Monitor használható, vizsgáld meg, hogy biztonságosan hozzáférsz-e a mért adatokhoz. Ha nem, jelezd, milyen további engedélyezett megoldás szükséges.
```

### Terhelés és hőmérséklet

```text
Ellenőrizd a számítógépem aktuális CPU- és memóriahasználatát. Ha hozzáférsz megbízható hőmérséklet-adathoz, azt is mutasd meg. Ha valamelyik adat nem érhető el, ne találj ki értéket.
```

### Biztonságos munkavégzés

```text
Mielőtt erőforrás-igényes feladatot indítasz, ellenőrizd a gép terhelését. Kerüld a szükségtelen párhuzamos folyamatokat. A saját magad által indított ideiglenes folyamatokat a munka végén állítsd le, az ideiglenes fájlokat pedig csak ellenőrzés és engedély után töröld. Meglévő felhasználói folyamatokat ne állíts le önállóan.
```

Magas hőmérsékletnél először figyelmeztess, ellenőrizd a mérés megbízhatóságát, és szükség esetén a saját erőforrás-igényes munkádat állítsd le biztonságosan. Más alkalmazások bezárásához kérj engedélyt.
