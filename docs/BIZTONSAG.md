# Biztonsági útmutató

## Kockázat

A kapcsolat fájlok olvasását/írását, terminálparancsot, folyamat- és programkezelést tehet lehetővé. Ezért ne add át automatikusan a teljes gépet, ne használd ismeretlen utasítással, és ne másold be jelszavaidat vagy kulcsaidat a chatbe.

## Biztonságos gyakorlat

- Elsőként csak olvass és listázz.
- A teszteléshez külön, nem érzékeny mappát használj.
- Törlésnél és parancsfuttatásnál egyszeri engedélyt válassz.
- Ellenőrizd az útvonalat és a célfájlt minden módosítás előtt.
- Ne engedélyezz rendszergazdai vagy állandó hozzáférést indokolatlanul.
- Leállítás után ellenőrizd az AI-felület eszközállapotát és a futó PowerShell-ablakot.
- A `Ctrl+C` megszakítja a futó helyi komponenst; az engedély visszavonását a szolgáltató aktuális kezelőfelületén végezd.

## Mit ne tölts fel nyilvánosan?

Jelszó, token, privát SSH-kulcs, személyes e-mail-cím, eszközazonosító, munkamenetadat, helyi szerverbeállítás és érzékeny napló nem kerülhet a repóba.
## Rendszerfigyelő adatok és magas hőmérséklet

A képernyőn megjelenő CPU-, memória-, GPU- vagy hőmérsékletértékek önmagukban nem MCP-adatok. Az AI csak tényleges, engedélyezett eszközhívással ellenőrzött értéket közölhet; ha az adat nem érhető el, ezt egyértelműen jeleznie kell.

A [Rendszer Monitor](https://github.com/Scofield81/rendszer-monitor) használható kiegészítőként a terhelés és a hőmérséklet figyelésére. Magas hőmérséklet esetén először a mérés megbízhatóságát kell ellenőrizni, majd az AI a saját erőforrás-igényes folyamatát állítsa le biztonságosan. Más alkalmazások vagy felhasználói folyamatok bezárásához mindig kérjen külön engedélyt.
