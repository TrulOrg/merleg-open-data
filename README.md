# Mérleg nyílt adatok / Mérleg open data

Magyarországi közszolgáltatások és képzők hivatalos, nyilvános adatai géppel olvasható formában – ugyanaz az adat, amelyet a
Mérleg-oldalak mutatnak. Szabadon felhasználható a forrás megjelölésével.

*Machine-readable official public data about Hungarian schools, driving schools and nursing homes – the same data shown on the
Mérleg websites. Free to use with attribution.*

| Adatkészlet / Dataset | Sorok / Rows | Frissítve / Updated | Fájlok / Files | Weboldal / Website |
|---|---|---|---|---|
| **Autósiskolák vizsgamutatói** – Driving schools: exam pass rates, training hours, ranking | 1394 | 2026-10-26 | [autosiskolak.csv](autosiskolak.csv) · [autosiskolak.json](autosiskolak.json) | [JogsiMérleg](https://jogsimerleg.hu/) |
| **Középiskolák érettségi eredményei** – Secondary schools: school-leaving exam results, ranking | 1037 | 2026-09-27 | [kozepiskolak.csv](kozepiskolak.csv) · [kozepiskolak.json](kozepiskolak.json) | [SuliMérleg](https://sulimerleg.hu/) |
| **Idősotthonok és gondozóházak** – Nursing homes and temporary care homes: places, operator type | 965 | 2026-10-26 | [idosotthonok.csv](idosotthonok.csv) · [idosotthonok.json](idosotthonok.json) | [IdősotthonMérleg](https://idosotthonmerleg.hu/) |

## Oszlopok / Columns

### autosiskolak
`id`, `name`, `city`, `postcode`, `address`, `categories`, `score`, `rankNational`, `practicalB`, `theoryB`, `akoB`, `lat`, `lon`, `url`

score = JogsiMérleg-index (0–10, 5 = országos átlag); practicalB / theoryB = B kategóriás forgalmi / elméleti vizsgasikeresség (%); akoB = átlagos képzési óraszám (óra). Forrás: KAV (vizsgakozpont.hu), Közlekedési Hatóság. Minden sor `url` oszlopa az adott intézmény JogsiMérleg-adatlapjára mutat.

### kozepiskolak
`id`, `om`, `name`, `city`, `county`, `address`, `types`, `advancedPct`, `certificatePct`, `candidatesLatest`, `rankNational`, `competency`, `lat`, `lon`, `url`

advancedPct = sikeres emelt szintű érettségik aránya (%); certificatePct = érettségi bizonyítványt szerzők aránya (%); competency = 10. évfolyamos kompetenciamérés eltérése az országos átlagtól (pont). Forrás: KIR (Oktatási Hivatal). Minden sor `url` oszlopa az adott intézmény SuliMérleg-adatlapjára mutat.

### idosotthonok
`id`, `name`, `city`, `county`, `address`, `operatorType`, `places`, `premiumPlaces`, `types`, `nationalIntake`, `registerId`, `lat`, `lon`, `url`

places = nyilvántartott férőhelyek; premiumPlaces = emelt szintű (prémium) férőhelyek; nationalIntake = országos ellátási terület. Forrás: Szociális Ágazati Portál szolgáltatói nyilvántartása. Minden sor `url` oszlopa az adott intézmény IdősotthonMérleg-adatlapjára mutat.

## Élő elérés / Live access

A fájlok időnként frissülnek; a mindig friss adat a weboldalak nyílt API-ján érhető el. *These files are refreshed
periodically; the always-current data is on each site's open API.*

- **JogsiMérleg** – JSON API: https://jogsimerleg.hu/api/ · MCP szerver (AI-asszisztenseknek): `https://api.jogsimerleg.hu/mcp` · [llms.txt](https://jogsimerleg.hu/llms.txt)
- **SuliMérleg** – JSON API: https://sulimerleg.hu/api/ · MCP szerver (AI-asszisztenseknek): `https://api.sulimerleg.hu/mcp` · [llms.txt](https://sulimerleg.hu/llms.txt)
- **IdősotthonMérleg** – JSON API: https://idosotthonmerleg.hu/api/ · MCP szerver (AI-asszisztenseknek): `https://api.idosotthonmerleg.hu/mcp` · [llms.txt](https://idosotthonmerleg.hu/llms.txt)

Az MCP szerverek a hivatalos [MCP Registry](https://registry.modelcontextprotocol.io/)-ben is szerepelnek
(`hu.jogsimerleg/autosiskolak`, `hu.sulimerleg/iskolak`, `hu.idosotthonmerleg/idosotthonok`).

## Forrás és felhasználás / Source and licence

Az alapadatok hivatalos, nyilvános magyar állami forrásokból származnak (lásd az oszlopleírásoknál); a mutatók számítását
az egyes oldalak „Módszertan” lapja írja le. Az összeállítás [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
licenc alatt használható: hivatkozz az adott Mérleg-oldalra (pl. „Forrás: JogsiMérleg, jogsimerleg.hu”).
Hibát találtál? hello@jogsimerleg.hu, hello@sulimerleg.hu, hello@idosotthonmerleg.hu

*The underlying figures come from official Hungarian public sources; the compilation is licensed CC BY 4.0 – please cite the
relevant Mérleg site.*
