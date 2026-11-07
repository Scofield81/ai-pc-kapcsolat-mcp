# AI–PC kapcsolat MCP – többplatformos útmutató

Magyar, kezdőknek szóló útmutató a [Desktop Commander Remote MCP](https://desktopcommander.app/) használatához. A helyi komponens a támogatott számítógépen fut, az AI-kliens pedig engedélyezett fájl-, terminál- és folyamatműveleteket kérhet tőle.

> **Fontos:** Az AI a megadott engedélyektől függően hozzáférhet a számítógéped fájljaihoz, és parancsokat futtathat. Csak megbízható szolgáltatást használj, az engedélykéréseket mindig ellenőrizd, és ne ossz meg jelszavakat, hozzáférési kulcsokat vagy más bizalmas adatokat.

## Mire használható?

- Windows, Linux és macOS számítógép helyi fájl- és terminálműveleteire.
- AI-csevegőből indított, jóváhagyható feladatokra.
- Másik számítógépről, Androidról vagy iPhone/iPadről elérhető távoli munkamenetre, ha az adott AI-kliens és szolgáltatás támogatja.
- Kezdőknek is követhető, másolható parancsokra és biztonságos próbakérésekre.

A mobiltelefon vagy táblagép csak AI-kliens lehet: nem az MCP-kiszolgáló. A kiszolgáló komponens a távoli számítógépen fut.

## Támogatás és saját teszteredmény

A Desktop Commander Remote hivatalosan Windows, Linux és macOS rendszeren használható. A támogatás nem jelenti azt, hogy minden AI-kliens, modell, régió vagy fiók ugyanazokat a funkciókat kínálja.

Ebben a projektben jelenleg a Windows 11 + Claude Free fájlkezelési folyamatot ellenőriztük. Linuxon, macOS-en és mobilkliensből még nem végeztünk saját tesztet. A részletes, időponttal jelölt eredmények a [teszteredményekben](docs/TESZTEREDMENYEK.md) olvashatók.

## Gyors áttekintés

1. Válaszd ki a számítógép operációs rendszeréhez tartozó útmutatót.
2. Telepítsd az adott rendszerhez szükséges Node.js LTS-változatot.
3. Indítsd el a Remote MCP-komponenst a terminálban.
4. Az AI-kliensben add hozzá a támogatott csatlakozót, majd minden műveletet ellenőrizz.
5. Ha befejezted a munkát, állítsd le a terminálfolyamatot. Később újra kell indítani, hacsak nem használsz külön gyorsindítót.

## Operációs rendszerenkénti telepítés

- [Windows 10/11 telepítés](docs/WINDOWS_TELEPITES.md) – Windows PowerShell, Node.js LTS és opcionális asztali gyorsindító.
- [Linux telepítés](docs/LINUX_TELEPITES.md) – terminál, Node.js LTS és rendszerfüggetlen útvonal-ellenőrzés.
- [macOS telepítés](docs/MACOS_TELEPITES.md) – Terminal, Node.js LTS és rendszerfüggetlen útvonal-ellenőrzés.

## Első, biztonságos próbakérések

```text
Listázd az alapértelmezett Dokumentumok mappát, de ne módosíts semmit.
```

```text
Kérdezd le az aktuális operációs rendszert, a bejelentkezett felhasználó nevét és a tényleges asztali mappát. Ne írj és ne törölj semmit.
```

```text
Hozz létre egy ideiglenes tesztmappát az aktuális felhasználó dokumentummappájában, írj bele egy rövid Markdown-fájlt, olvasd vissza, majd kérj külön engedélyt a törléshez.
```

További minták: [kezdő tesztek](docs/KEZDO_TESZTEK.md) és [gyakorlati példák](docs/PELDATARBAN.md).

## Mobil- és táblagépes használat

Androidról, iPhone-ról vagy iPadről a támogatott AI-klienssel lehet elérni egy másik, Remote MCP-t futtató számítógépet. A mobilkliens nem helyettesíti a számítógépen futó MCP-komponenst, és saját mobiltesztünk még nincs.

Részletek: [távoli, mobil- és táblagépes használat](docs/TAvoli_MOBILIS.md).

## Dokumentáció

- [Claude Free csatlakoztatása](docs/CLAUDE_FREE.md)
- [Engedélykérések](docs/ENGEDELYEK.md)
- [Biztonsági útmutató](docs/BIZTONSAG.md)
- [Hibaelhárítás](docs/HIBAELHARITAS.md)
- [AI-szolgáltatói teszteredmények](docs/TESZTEREDMENYEK.md)

A belső munkanaplók, tanulságok és fejlesztési jelentések nem részei a nyilvános felhasználói kiadásnak.

## Ingyenes használat és források

A Desktop Commander szolgáltatásánál és az AI-szolgáltatóknál különböző ingyenes keretek lehetnek. Ezek változhatnak, és egy felhasználói üzenet több eszközhívást is eredményezhet. Mindig ellenőrizd az aktuális feltételeket.

- [Desktop Commander](https://desktopcommander.app/)
- [Hivatalos Remote Desktop Commander repó](https://github.com/desktop-commander/remote-desktop-commander)
- [Hivatalos helyi Desktop Commander MCP repó](https://github.com/wonderwhy-er/DesktopCommanderMCP)

## Licenc és eredet

Ez a repó magyar nyelvű, felhasználói dokumentáció. A Desktop Commander szoftver és szolgáltatás nem a repó szerzőjének fejlesztése; az eredeti szerzők és a hivatalos források a fenti hivatkozásokon találhatók.

## Ajánlott kiegészítő: Rendszer Monitor

A [Rendszer Monitor](https://github.com/Scofield81/rendszer-monitor) ingyenes Windows 10/11 x64-es rendszerfigyelő minialkalmazás. CPU-terhelést, CPU-hőmérsékletet, RAM-használatot és támogatott videokártyán GPU-terhelést jelenít meg.

A képernyőn látható értékek nem jelentenek automatikusan MCP-adatforrást. Az AI csak tényleges, engedélyezett eszközhívással igazolt adatokra támaszkodhat. Gyakorlati minták: [Rendszer Monitor és hardverfigyelés](docs/PELDATARBAN.md).
