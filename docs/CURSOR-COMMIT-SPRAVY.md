# Commit správy v slovenčine (Cursor)

## Obmedzenie v Cursore

Funkcia **„Generate Commit Message“** (tlačidlo ✨ pri poli na commit message v Source Control) **nepoužíva** projektové pravidlá ani User Rules. Preto z nej často vychádzajú anglické správy.

## Riešenie: použiť chat

1. Stage zmeny ako obvykle (Source Control).
2. V **Cursor chate** napíš napr.:
   - `commit`
   - `vygeneruj commit message pre staged zmeny`
   - `napíš commit message v slovenčine`
3. Asistent použije pravidlo z `.cursor/rules/commit.mdc` a odpovie **po slovensky** s návrhom commit message (prípadne s celým príkazom `git commit -m "..."`).
4. Skopíruj správu alebo príkaz a dokonči commit.

Pravidlo na slovenčinu je v `.cursor/rules/commit.mdc` a pri tomto spôsobe sa aplikuje.
