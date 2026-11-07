# AI-szolgáltatói teszteredmények

## Vizsgálati idő

Teljes felderítési időszak: **2026.11.06. kb. 22:15–23:15, körülbelül 60 perc**. Ez a felhasználó által megadott teljes vizsgálati idő, nem kizárólag MCP-eszközhívás.

## Eredmények

| Szolgáltató | Eredmény | Bizonyíték/korlát |
|---|---|---|
| ChatGPT Plus | Korábbi használatban működött | Normál ChatGPT-csevegés, nem Work mód; a jelen dokumentumkészítés külön felderítési tesztje nem ismételte meg. |
| ChatGPT Free | Nem sikerült | A vizsgált 2026.11.06-i ingyenes fiókban a csatlakozó nem volt telepíthető/használható. |
| Claude Free, Haiku 5.5 | Sikeres | Windows 11 számítógép elérése, ideiglenes tesztmappa, Markdown-fájl létrehozása, visszaolvasás, törlés és utólagos ellenőrzés. A gép neve és a felhasználói útvonal nem része a nyilvános dokumentációnak. |
| Gemini ingyenes web | Nem sikerült | A vizsgált magyarországi fiókban a csatlakozó és egyéni távoli MCP-hozzáadás nem volt elérhető. |

## Claude műveleti időpontok

| Időpont | Naplóban jelzett művelet |
|---|---|
| 22:44:03 | Desktop Commander indítása |
| 22:44:09 | Sikeres Remote MCP-csatlakozás |
| 22:55:59 | Tesztmappa létrehozása |
| 22:56:23 | Tesztfájl írása |
| 22:56:50 | Tesztfájl visszaolvasása |
| 22:59:14 | Első, szintaktikai hiba miatt sikertelen törlési próbálkozás |
| 22:59:18–22:59:23 | Sikeres törlési műveletek |
| 22:59:25–22:59:27 | Törlés ellenőrzése |

A teszt egy ideiglenes, nem érzékeny mappában és `teszt.md` fájllal történt. A pontos helyi útvonalat adatvédelmi okból nem közöljük. A helyi képernyőképek nem voltak elérhetők, ezért képi bizonyíték nincs ebben a kiadásban.

## Aktuális hivatalos keret

A [hivatalos árlista](https://desktopcommander.app/pricing/) a vizsgálatkor Free csomagnál havi 10 000 tool-hívást jelzett. Ez a Desktop Commander szolgáltatói kerete, nem az AI-szolgáltató saját ingyenes kerete.
