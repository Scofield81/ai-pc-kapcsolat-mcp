# Linux telepítési útmutató

Ez az útmutató Linux asztali rendszerekhez készült. A pontos csomagkezelő az elosztástól függ; a példák Debian/Ubuntu rendszeren használható minták.

## 1. Terminál megnyitása

Nyisd meg a rendszer Terminál alkalmazását. A parancsablakban a saját felhasználói környezetedben dolgozz; ne használj rendszergazdai `sudo` módot, ha arra nincs szükség.

## 2. Node.js LTS telepítése

Telepítsd a hivatalos [Node.js LTS](https://nodejs.org/) változatot vagy a Linux-disztribúciód dokumentációjában ajánlott Node.js-csomagot. Ellenőrzés:

```bash
node --version
npm --version
npx --version
```

## 3. Remote MCP indítása

```bash
npx @wonderwhy-er/desktop-commander@latest remote
```

Indítás után várd meg a szolgáltatás által jelzett online vagy kész állapotot. A terminált hagyd nyitva a kapcsolat használatához.

## 4. Útvonalak és gyorsindító

Az AI ne találgassa a saját géped vagy felhasználód nevét. Kérd le az adott környezet adatait, például:

```bash
printf 'OS=%s\nUSER=%s\nHOME=%s\n' "$(uname -s)" "$USER" "$HOME"
xdg-user-dir DESKTOP 2>/dev/null || printf '%s\n' "$HOME/Desktop"
```

Gyorsindítót csak az aktuális felhasználó tényleges asztali mappájában hozz létre, meglévő fájl felülírása nélkül. Ez nem automatikus indítás; a terminálfolyamatot később újra el kell indítani.

## 5. Leállítás

```text
Ctrl+C
```

Linuxon, macOS-en és Windowson is külön kell ellenőrizni a szolgáltatói csatlakozó és az AI-kliens kompatibilitását. Ebben a projektben Linuxon saját fájlkezelési tesztet még nem végeztünk.
