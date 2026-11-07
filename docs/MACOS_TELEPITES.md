# macOS telepítési útmutató

Ez az útmutató macOS rendszerekhez készült. A parancsokat a bejelentkezett felhasználó saját Terminal alkalmazásában futtasd.

## 1. Terminal megnyitása

Nyisd meg az **Applications > Utilities > Terminal** alkalmazást, vagy keresd meg a Spotlight segítségével.

## 2. Node.js LTS telepítése

Telepítsd a hivatalos [Node.js LTS](https://nodejs.org/) változatot. Ellenőrzés:

```bash
node --version
npm --version
npx --version
```

## 3. Remote MCP indítása

```bash
npx @wonderwhy-er/desktop-commander@latest remote
```

Várd meg a szolgáltatás online vagy kész állapotjelzését. A Terminal ablakát hagyd nyitva a kapcsolat használatához.

## 4. Útvonalak és gyorsindító

Az AI mindig kérdezze le az aktuális macOS-környezetet, és ne használjon előre beégetett számítógépnevet vagy felhasználói útvonalat:

```bash
printf 'OS=%s\nUSER=%s\nHOME=%s\nDESKTOP=%s\n' "$(uname -s)" "$USER" "$HOME" "$HOME/Desktop"
```

A gyorsindító csak a tényleges, aktuális felhasználói asztali mappába kerüljön, meglévő fájl felülírása nélkül. Nem indul el automatikusan a Mac bekapcsolásakor.

## 5. Leállítás

```text
Ctrl+C
```

Ebben a projektben macOS-en saját fájlkezelési tesztet még nem végeztünk; a támogatás és a saját validáció külön kezelendő.
