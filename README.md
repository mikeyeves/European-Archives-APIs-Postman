# European Archives & Libraries APIs — Postman Collections

Postman (v2.1) collections for public APIs that help with **Central and Eastern European genealogy**: Austro-Hungarian, German, Banat/Danube Swabian, Serbian and Hungarian research. They cover historic newspapers, digitized archive and library material, and place-name resolution.

| Collection | Requests | Key needed? | Use it for | Import link |
|---|---|---|---|---|
| **Europeana API** | 18 | Free key (`api2demo` demo key works) | 50M+ items from European archives, libraries and museums, incl. Europeana Newspapers, IIIF and full text | `https://raw.githubusercontent.com/mikeyeves/European-Archives-APIs-Postman/main/Europeana_API.postman_collection.json` |
| **Deutsche Digitale Bibliothek (DDB) API** | 58 | Search: no key needed. User endpoints: key | German Digital Library plus the **German Newspaper Portal full-text index**, which includes German-language papers from Austria-Hungary | `https://raw.githubusercontent.com/mikeyeves/European-Archives-APIs-Postman/main/DDB_API.postman_collection.json` |
| **Wikidata (place-name toolkit)** | 7 | No | Resolving historic place names: Hungarian ↔ German ↔ Serbian/Romanian/Slovak. Also administrative history and nearby villages/parishes | `https://raw.githubusercontent.com/mikeyeves/European-Archives-APIs-Postman/main/Wikidata_Places.postman_collection.json` |
| **Austrian National Library (ÖNB) API** | 9 | No (IDs from ONB viewer) | IIIF manifests, images and OCR text from ÖNB digital collections | `https://raw.githubusercontent.com/mikeyeves/European-Archives-APIs-Postman/main/ONB_API.postman_collection.json` |

Import any collection with Postman → Import → Link. No environment file is needed; settings are collection variables.

## What was verified at build time
- **Europeana:** the search, record and entity APIs returned results with the `api2demo` key.
- **DDB:** the Solr search and newspaper full-text search returned results **without a key**. For example, `plainpagefulltext:Beodra` returned 64 newspaper issues.
- **Wikidata:** all 4 SPARQL queries and the entity search returned results. For example, Beodra resolves to Q793176 (Novo Miloševo, Serbia), with names in hu, de, ro and sr, and nearby villages within 15 km.
- **ÖNB:** the endpoints are copied from https://api.onb.ac.at/. They were **not** tested with live IDs. Note that ANNO (Austrian Newspapers Online) web pages sit behind a bot check and can't be used as an API.

## Sources considered but not included
| Source | Why it's not included |
|---|---|
| Archives Portal Europe | API keys are issued on request. The site blocks automated access, so the endpoints couldn't be verified |
| Matricula Online (parish registers) | No public API |
| Arcanum / Hungaricana | No public API |
| Serbian archives (Zrenjanin, Kikinda, Arhiv Vojvodine) | No API; requests by letter |
| Polish State Archives (szukajwarchiwach) and Czech regional archives | No public API |
| JewishGen, GenTeam, Geneteka, MyHeritage, Ancestry | No public API |

## Related collections
- [FamilySearch API](https://github.com/mikeyeves/FamilySearch-API-Postman)
- [Geni API](https://github.com/mikeyeves/Geni-API-Postman)
- [NYC Historical Vital Records](https://github.com/mikeyeves/NYC-Historical-Vital-Records-Postman)
- [NYC Open Data](https://github.com/mikeyeves/NYC-Open-Data-Postman)
- [Unified Census ED Finder](https://github.com/mikeyeves/Unified-Census-ED-Finder-Postman)
- [Federal Register + National Archives Catalog](https://github.com/mikeyeves/US-Federal-Register-National-Archives-Catalog-APIs)
- [Hebcal](https://github.com/mikeyeves/Hebcal-Jewish-Calendar-APIs)

*Unofficial. Not affiliated with Europeana, the DDB, Wikimedia or the ÖNB. Built from their public documentation.*
