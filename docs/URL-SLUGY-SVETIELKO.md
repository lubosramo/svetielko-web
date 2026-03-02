# URL a slugy – Svetielko (1:1 z Buxus)

Mapovanie stránok na Hugo content súbory a výsledné URL. Statické súbory (.html, .mp3, .pdf) ostávajú v `static/`, odkazy na ne sa nemenia.

## Hlavné menu (vrchná lišta)

| Menu / stránka | Hugo content súbor | URL (relatívna) |
|----------------|--------------------|-----------------|
| Úvod | `content/sk/_index.md` | `/` |
| Hudba | `content/sk/hudba/_index.md` | `/hudba/` |
| Aktivity | `content/sk/aktivity/_index.md` | `/aktivity/` |
| Svetielko | `content/sk/svetielko/_index.md` | `/svetielko/` |
| Kontakt | `content/sk/kontakt/_index.md` | `/kontakt/` |

## Podstránky – Hudba

| Názov | Content súbor | URL |
|-------|----------------|-----|
| Vianoce na celom svete (detail + objednávka) | `content/sk/hudba/vianoce-na-celom-svete.md` | `/hudba/vianoce-na-celom-svete/` |
| Ferdo Mravec Všeumelec (detail + objednávka) | `content/sk/hudba/ferdo-mravec-vseumelec.md` | `/hudba/ferdo-mravec-vseumelec/` |

## Podstránky – Aktivity

| Názov | Content súbor | URL |
|-------|----------------|-----|
| Ukončené aktivity (archív) | `content/sk/aktivity/ukoncene-aktivity.md` | `/aktivity/ukoncene-aktivity/` |
| Hudobné kurzy v Bratislave | `content/sk/aktivity/hudobne-kurzy-v-bratislave.md` | `/aktivity/hudobne-kurzy-v-bratislave/` |
| Pôvodný detský muzikál Ferdo Mravec Všeumelec (opis) | `content/sk/aktivity/ferdo-mravec-vseumelec.md` | `/aktivity/ferdo-mravec-vseumelec/` |
| Muzikál Vianoce na celom svete (opis) | `content/sk/aktivity/vianoce-na-celom-svete.md` | `/aktivity/vianoce-na-celom-svete/` |

Poznámka: „Detský muzikál Anjeli“ a „Detské koncerty“ sú len text na stránke Aktivity, nemajú vlastnú podstránku.

**Zoznam na stránke Aktivity:** Podstránky sa na `/aktivity/` zobrazujú automaticky. V front matter každej podstránky môžete nastaviť:
- **list_title** – názov odkazu v zozname (ak chcete iný ako `title`)
- **description** – krátka anotácia pod odkazom (ak chýba, použije sa výňatok z úvodu stránky)

## Podstránky – Svetielko

| Názov | Content súbor | URL |
|-------|----------------|-----|
| Stanovy OZ Svetielko | `content/sk/svetielko/stanovy-oz-svetielko.md` | `/svetielko/stanovy-oz-svetielko/` |

## Mapovanie Buxus page_id → Hugo slug

| page_id | Stránka | Hugo URL |
|---------|---------|----------|
| 1 | Úvod | `/` |
| 118 | Kontakt | `/kontakt/` |
| 119 | Svetielko | `/svetielko/` |
| 120 | Aktivity | `/aktivity/` |
| 121 | Hudba | `/hudba/` |
| 122 | Vianoce na celom svete (Hudba) | `/hudba/vianoce-na-celom-svete/` |
| 123 | Ferdo Mravec Všeumelec (Hudba) | `/hudba/ferdo-mravec-vseumelec/` |
| 126 | Ferdo Mravec Všeumelec (Aktivity – opis) | `/aktivity/ferdo-mravec-vseumelec/` |
| 129 | Hudobné kurzy v Bratislave | `/aktivity/hudobne-kurzy-v-bratislave/` |
| 134 | Vianoce na celom svete (Aktivity – opis) | `/aktivity/vianoce-na-celom-svete/` |
| 140 | Ukončené aktivity | `/aktivity/ukoncene-aktivity/` |
| 143 | Stanovy OZ Svetielko | `/svetielko/stanovy-oz-svetielko/` |

## Statické súbory (odkazy ostávajú ako doteraz)

- Haleluja: `haleluja96.htm`, `haleluja97.htm`, `haleluja98.htm`, `haleluja99.htm`, `haleluja.htm` → v `static/` alebo na pôvodnej ceste
- MP3 ukážky: napr. `buxus/docs/ukazky/...` → skopírovať do `static/` a zachovať cesty v obsahu
- PDF stanovy: napr. `buxus/docs/OZ-Svetielko-stanovy.pdf` → `static/docs/` alebo ekvivalent

---

## Napojenie na Hugoplate

- **Jazyk:** `config/_default/languages.toml` – jediný jazyk `[sk]`, `contentDir = "content/sk"`.
- **Default jazyk:** `hugo.toml` – `defaultContentLanguage = "sk"`.
- **Menu:** `config/_default/menus.sk.toml` – hlavné menu (Úvod, Hudba, Aktivity, Svetielko, Kontakt) + podmenu pod Hudba, Aktivity, Svetielko; footer menu.
- **Obsah:** Všetky stub stránky sú v `content/sk/`. Po dokončení migrácie môžeš odstrániť `content/english/`.
