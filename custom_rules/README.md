# custom_rules/

Tähän kansioon voit lisätä omia **sääntötiedostoja**, jotka Suomettaja noudattaa automaattisesti. Säännöt ovat käskeviä direktiivejä: aina näin, ei koskaan noin, korvaa X sanalla Y.

Pohjasäännöt (`SKILL.md`, `references/kielioppi.md`, `references/patterns.md`) pysyvät aina voimassa. Tämä kansio **laajentaa tai ohittaa** niitä tyylivalintojen osalta. Huom: kielioppi- ja oikeinkirjoitussääntöjä ei voi ohittaa — niiden rikkominen olisi virhe, ei tyylivalinta.

## Mihin tätä käytetään

- **Kielletyt sanat** — sanat joita et koskaan halua tekstiin
- **Pakolliset termit** — kuinka brändin tai tuotteen nimi kirjoitetaan
- **Korvaussäännöt** — "kun näet X, käytä Y"
- **Tyyliohjeet** — "vältä emojit aina", "käytä aina sinutteluja"
- **Projektikohtaiset reunaehdot** — "tämän asiakkaan teksteissä ei koskaan passiivia"

## Miten lisätä sääntö

1. Luo `.md`-tiedosto tähän kansioon (esim. `kielletyt_sanat.md`, `brandin_termit.md`)
2. Kirjoita säännöt selkeästi: mitä tehdä, mitä ei, miksi
3. Suomettaja lukee tiedoston automaattisesti ja noudattaa sääntöjä korjausprosessin kaikissa vaiheissa

## Sääntöhierarkia

1. **Kielioppi ja oikeinkirjoitus** (pohja, `references/kielioppi.md`) — aina voimassa, ei ohitettavissa
2. **AI-patternit** (pohja, `references/patterns.md`) — aina voimassa
3. **Omat säännöt** (`custom_rules/`) — tyylivalinnat ja projektikohtaiset reunaehdot
4. **Käyttäjän istuntokohtaiset ohjeet** — ylin prioriteetti, voivat väliaikaisesti ohittaa omat säännöt

Jos `custom_rules/`-sääntö on ristiriidassa kieliopin kanssa, Suomettaja kysyy käyttäjältä miten toimia.

## Esimerkkitiedostoja

```
custom_rules/
  kielletyt_sanat.md      # Sanat joita ei koskaan saa käyttää
  brandin_termit.md       # "Acme Cloud" ei "acme cloud" tai "Acme-pilvi"
  korvaukset.md           # "käyttäjä" → "asiakas", "tuote" → "palvelu"
  tyyli.md                # Sinuttelu aina, ei emojeita, ei huutomerkkejä
```

## Esimerkki: kielletyt_sanat.md

```markdown
# Kielletyt sanat

Älä koskaan käytä näitä sanoja Acme Oy:n teksteissä.

| Kielletty | Käytä tilalla | Miksi |
|-----------|---------------|-------|
| ratkaisu | kerro konkreettisesti mikä | liian epämääräinen |
| innovatiivinen | näytä esimerkillä | tyhjä superlatiivi |
| helppo | (poista tai perustele) | lukija päättää onko helppoa |
| ammattilainen | asiantuntija | ammattilaiseen liittyy hintamielikuva |
```

## Esimerkki: brandin_termit.md

```markdown
# Brändin termistö

## Yrityksen nimi
- Aina: **Acme Oy** (ei "Acme", ei "acme", ei "ACME")
- Taivutettuna: Acme Oy:n, Acme Oy:llä

## Tuotteet
- **Acme Cloud** (iso A, iso C, välilyönti) — ei "Acme-pilvi" tai "acmecloud"
- **Acme Desk** — aina englanniksi, ei "Acme Työpöytä"
```

## Ero `custom_references/`-kansioon

- **`custom_rules/`** = pakottavat direktiivit (käskevä)
- **`custom_references/`** = taustamateriaali ja esimerkit (kuvaileva)

Nyrkkisääntö: jos sisältö alkaa sanoilla "älä koskaan", "aina", "korvaa", se kuuluu tänne. Jos se on kuvailevaa ("brändin ääni on suora ja tekninen"), se kuuluu `custom_references/`-kansioon.

## Versionhallinta

Tiedostot tässä kansiossa on oletuksena ignoroitu `.gitignore`ssa, jotta `git pull` ei riko omia mukautuksiasi. Jos haluat versioida omat säännöt, tee niille oma repo tai poista ignore-sääntö paikallisesti.
