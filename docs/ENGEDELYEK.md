# Engedélykérések magyarázata

A Claude-teszt során például ezekre érkezett engedélykérés: `List Devices`, `Get File Information`, `Create Directory`, `Write File`, `Read File or URL`, `Start Terminal Process`.

| Választás | Jelentés |
|---|---|
| **Deny** | A művelet elutasítása. |
| **Allow once** | Csak az adott hívás egyszeri engedélyezése. |
| **Always allow** | Az adott eszköz ismételt hívásainak engedélyezése a felület szabályai szerint. |

Az **Always allow** nem jelent automatikusan minden MCP-eszközre korlátlan hozzáférést. Kezdőként fájltörlésnél, parancsfuttatásnál és módosításnál az **Allow once** a biztonságosabb alapértelmezés.
