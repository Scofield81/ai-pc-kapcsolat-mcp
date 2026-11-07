# Windows 10/11 telepítési útmutató kezdőknek

## Előfeltételek

Windows 10 vagy Windows 11, internet, böngésző, e-mailes fiók a választott AI-szolgáltatónál és Node.js szükséges. A Windows 10 és Windows 11 alapértelmezetten tartalmazza a Windows PowerShellt, ezért azt külön nem kell letölteni.

A Node.js LTS telepítőjét a hivatalos [Node.js letöltőoldalról](https://nodejs.org/en/download) töltsd le. Telepítés után nyiss új PowerShellt, hogy az új `node` és `npx` parancsok biztosan elérhetők legyenek.

## 1. A PowerShell megnyitása

1. Kattints a Windows tálcáján a nagyító ikonra, vagy nyisd meg a **Start** menüt.
2. A keresőmezőbe kezdd el beírni: `PowerShell`.
3. A találatok között válaszd a **Windows PowerShell** alkalmazást.
4. Kattints rá a normál megnyitáshoz. **Nem szükséges rendszergazdaként futtatni.**

Megjelenik egy parancsablak. A villogó kurzor vagy a `PS C:\...>` kezdetű sor normális: ez azt jelzi, hogy az ablak várja a parancsot, nem hibát.

## 2. A Node.js telepítése – 5 egyszerű lépésben

Ha a `node --version` parancs már verziószámot ír ki, a Node.js rendelkezésre áll: ne telepítsd újra. Ha a parancs nem működik, kövesd az alábbi lépéseket.

Az útmutató ellenőrzésekor a hivatalos Node.js-letöltőoldal aktuális LTS-változata a **v26.13.0 LTS** volt. A közvetlen telepítők a Node.js hivatalos szerveréről érkeznek:

- [Windows x64 MSI – Intel/AMD számítógépek](https://nodejs.org/dist/v26.13.0/node-v26.13.0-x64.msi)
- [Windows ARM64 MSI – ARM-alapú számítógépek](https://nodejs.org/dist/v26.13.0/node-v26.13.0-arm64.msi)
- [Hivatalos Node.js letöltőoldal](https://nodejs.org/en/download)

A letöltőoldalon a **Windows Installer (.msi)** gombot válaszd. Ez a kezdőknek való telepítő. A **Standalone Binary (.zip)** csak hordozható, kézi használatra szánt csomag; ehhez az útmutatóhoz ne azt töltsd le.

Az x64-változat való a legtöbb Intel- vagy AMD-processzoros géphez. Ha nem tudod, melyik kell, nyisd meg a **Gépház → Rendszer → Névjegy** oldalt, és keresd meg a **Rendszertípus** sort. Az „x64-alapú processzor” az x64 telepítőt, az „ARM64-alapú processzor” az ARM64 telepítőt jelenti.

1. Kattints a számítógépedhez megfelelő közvetlen letöltési hivatkozásra.
2. A letöltés után nyisd meg a letöltött `.msi` telepítőfájlt. Ha a böngésző rákérdez, válaszd a **Megnyitás** vagy a **Fájl megnyitása** lehetőséget.
3. A Node.js telepítőablakában kattints a **Next** (Tovább) gombra, jelöld be a licenc elfogadását, majd kattints ismét a **Next** (Tovább) gombra.
4. Hagyd meg az alapértelmezett telepítési beállításokat, majd kattints az **Install** (Telepítés) gombra. Ha a Windows engedélykérő ablaka megjelenik, válaszd az **Igen** lehetőséget.
5. A telepítés végén kattints a **Finish** (Befejezés) gombra.

A telepítő több képernyőn vezet végig. Kezdőként ne változtasd meg a telepítési mappát vagy a választható alapbeállításokat. A telepítés után zárd be a régi PowerShell-ablakot, majd nyiss újat az előző rész szerint, hogy a Windows betöltse az új parancsokat.

## 3. A telepítés ellenőrzése

Nyiss új Windows PowerShell-ablakot, majd másold be külön-külön az alábbi parancsokat. Mindegyik után nyomd meg az **Enter** billentyűt. PowerShellben az `.cmd` végződésű változatokat használjuk, mert egyes Windows-beállítások tiltják az `npm.ps1` és `npx.ps1` segédszkriptek futtatását.

```powershell
node --version
npm.cmd --version
npx.cmd --version
```

Sikeres telepítéskor mindhárom parancs egy verziószámot ír ki, például `v26.13.0`, `11.x` vagy `13.x` formában. Nem az a fontos, hogy minden szám azonos legyen, hanem az, hogy mindhárom parancs működjön és ne jelenjen meg „nem található” hiba.

Sikeres például, ha a három parancs ehhez hasonló verziószámot ír ki:

```text
v22.23.2
10.9.8
10.9.8
```

Ha a `npm --version` vagy `npx --version` parancs azt írja, hogy az `npm.ps1` vagy `npx.ps1` nem tölthető be, ez PowerShell-futtatásiházirend-probléma, nem feltétlenül Node.js-hiba. Használd helyettük az útmutatóban szereplő `npm.cmd` és `npx.cmd` parancsokat. Ne módosítsd önállóan a PowerShell biztonsági házirendjét.

Ha az `.cmd` végződésű parancsok sem működnek:

1. Zárd be a PowerShell-ablakot.
2. Nyiss új **Windows PowerShell** ablakot.
3. Futtasd le újra a három ellenőrző parancsot.
4. Ha továbbra sem működik, ellenőrizd, hogy a hivatalos Node.js MSI-telepítő telepítése befejeződött-e, majd szükség esetén telepítsd újra az alapértelmezett beállításokkal.

## 4. A Desktop Commander indítása

Jelöld ki és másold ki az alábbi egyetlen sort. A PowerShell-ablakban kattints a parancssorba, illeszd be, majd nyomd meg az **Enter** billentyűt.

```powershell
npx.cmd @wonderwhy-er/desktop-commander@latest remote
```

Az `npx` szükség esetén letöltheti a helyi komponenst, ezért az első indítás eltarthat egy ideig. Ne zárd be az ablakot közben.

Sikeres induláskor a naplóban ehhez hasonló üzenetek jelenhetnek meg:

```text
Connected to Desktop Commander MCP
Connected to Remote MCP
Device ready
Status: Online
```

Csak a ténylegesen megjelenő ablak vagy mentett napló tekinthető bizonyítéknak.

## 5. Az ablak nyitva tartása

A PowerShell-ablakot hagyd nyitva a kapcsolat használata közben. Minimalizálhatod, de bezárásakor a helyi komponens leállhat, és a távoli AI-kliens elveszítheti a kapcsolatot.

Ez nem egyszeri, állandó telepítésként működik: a PowerShellben futó indítóparancs csak addig tartja fenn a kapcsolatot, amíg a folyamat fut. Ha befejezted a munkát, bezárhatod a PowerShell-ablakot. Ha később újra használni szeretnéd a kapcsolatot, a parancsot ismét el kell indítani.

## 6. Opcionális asztali gyorsindító

Az indítóparancs nem fut tovább a PowerShell bezárása után. Ha később újra használni szeretnéd a kapcsolatot, a parancsot ismét el kell indítani. Ennek kényelmes módja egy asztali gyorsindító parancsikon.

Fontos: a Windows asztali mappája nem minden gépen ugyanott található. Lehet hagyományos profilban, OneDrive által szinkronizálva vagy más módon átirányítva. Az AI-ügynök soha ne találgassa az útvonalat, hanem a bejelentkezett Windows-felhasználó környezetében kérdezze le:

```powershell
[Environment]::GetFolderPath('Desktop')
```

Az így kapott útvonalon ellenőrizze, létezik-e már azonos nevű parancsikon. Meglévő parancsikont engedély nélkül ne írjon felül. A gyorsindító nem indul el automatikusan a Windows bekapcsolásakor; a felhasználó indítja el, és a PowerShell-ablak bezárásával állítja le.

Az első sikeres csatlakozás után másold be ezt a promptot az AI-csevegőbe:

```text
Szeretném egyetlen kattintással elindítani a Desktop Commander Remote MCP-kapcsolatot.

Ellenőrizd, hogy a Windows-fiókom tényleges asztali mappája hol található, figyelembe véve az esetleges OneDrive- vagy más felhőalapú átirányítást.

Hozz létre az asztalomon egy „Desktop Commander – AI kapcsolat” nevű parancsikont, amely elindítja a következő parancsot:

npx.cmd @wonderwhy-er/desktop-commander@latest remote

A parancsikon használjon egyértelmű ikont, és nyisson látható PowerShell-ablakot.

Ellenőrizd, hogy a parancsikon valóban létrejött, a megfelelő helyre mutat és a helyes indítóparancsot tartalmazza.

Meglévő parancsikont ne írj felül engedély nélkül, és más fájlt ne módosíts.
```

### Gyorsindító ellenőrzése

1. Várd meg, amíg az ügynök visszajelzi, hogy a parancsikon elkészült.
2. Ellenőrizd az asztalon a nevét és az ikonját.
3. A futó PowerShell-ablakot zárd be az **X** gombbal. Ezzel a kapcsolat várhatóan megszakad.
4. Kattints kétszer az új gyorsindítóra, és várd meg a kapcsolat indulását.
5. Várd meg a `Device ready` vagy `Status: Online` üzenetet, majd az AI-felületen ellenőrizd, hogy a gép újra elérhető.

Az első kiadásban a gyorsindító tényleges indítását nem jelöljük saját, végrehajtott tesztként. A prompt ajánlott kényelmi lépés; a felhasználó minden számítógépen külön ellenőrizze az útvonalat és a parancsikont.

## 7. Biztonságos leállítás

```text
Ctrl+C
```

Kattints a futó PowerShell-ablakra, majd nyomd meg egyszerre a **Ctrl** és **C** billentyűt. Ez jelzi a programnak, hogy álljon le. Ne a folyamat erőltetett kilövésével kezdd. A kapcsolat leállítása után az AI-felületen is ellenőrizd, hogy az eszköz offline vagy leválasztott állapotú.

## Képernyőképek állapota

Ebben az első kiadásban nem áll rendelkezésre ellenőrzött, személyes adatoktól megtisztított Windows 10/11 képernyőkép a keresés, a PowerShell-megnyitás, a parancsbeillesztés és a sikeres csatlakozás bemutatásához. Nem készült kitalált vagy manipulált kép. A valódi, anonimizált illusztrációk későbbi kiadásban pótolhatók.

## Más rendszerek

A hivatalos projektek más kliens- és operációs rendszereket is említhetnek, de ez a dokumentáció Windows 10/11-en végzett saját ellenőrzésre épül. Linux/macOS vagy más AI-kliens esetén külön ellenőrzés szükséges.
