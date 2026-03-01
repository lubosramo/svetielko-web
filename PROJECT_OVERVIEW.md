## Prehľad projektu

Tento repozitár je založený na šablóne **Hugoplate** – Hugo + Tailwind CSS starter. Slúži ako základ pre tvoj vlastný web postavený na statickom generátore **Hugo**.

## Ako z toho spraviť vlastný web

### 1. Základné nastavenia webu

- **`hugo.toml`**  
  - nastav názov webu (`title`), `baseURL` (tvoja doména), jazyk a ďalšie globálne nastavenia
- **`config/_default/params.toml`**  
  - mení sa tu logo, favicon, SEO, vyhľadávanie, komentáre a ďalšie parametre témy

### 2. Obsah stránok (texty)

Obsah webu je v adresári `content/english/...`:

- **Domovská stránka**: `content/english/_index.md`
- **O nás**: `content/english/about/_index.md`
- **Kontakt**: `content/english/contact/_index.md`
- **Blog**: `content/english/blog/*.md` (jednotlivé články)
- **Ďalšie stránky**: `content/english/pages/*.md` (napr. privacy policy, elements)
- **Sekcie domovskej stránky**: `content/english/sections/*.md` (hero, call-to-action, testimonials a pod.)

V týchto `.md` súboroch môžeš priamo meniť nadpisy, texty, tlačidlá a ďalší obsah.

### 3. Dizajn (farby, fonty, rozloženie)

- **Farby a fonty**: `data/theme.json`  
  - primárna/sekundárna farba, font family, veľkosti
- **Sociálne siete**: `data/social.json`  
  - odkazy na sociálne siete zobrazované na webe
- **Vzhľad (CSS)**: `assets/css/custom.css` a ďalšie CSS súbory  
  - jemné úpravy vzhľadu, ktoré dopĺňajú Tailwind
- **HTML šablóny**: `layouts/**`  
  - šablóny stránok a partials, ak chceš meniť samotnú HTML štruktúru

### 4. Jazyk (napr. slovenčina)

- Jazyk môžeš nastaviť v **`hugo.toml`** a **`config/_default/languages.toml`**  
- Môžeš:
  - použiť existujúci priečinok `english` ako základ a neskôr ho premenovať (napr. na `sk`), alebo
  - pridať nový jazyk a mať viacjazyčný web
- Texty rozhrania (napr. „Next/Previous“, drobné UI texty) sú v `i18n/*.yaml`

---

Tento súbor slúži ako rýchle zhrnutie, kde čo v projekte nájdeš a čo treba upraviť, aby si z Hugoplate spravil svoj vlastný web.

