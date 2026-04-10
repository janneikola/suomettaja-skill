# custom_references/

Tähän kansioon voit lisätä omia **referenssitiedostoja**, jotka Suomettaja lukee automaattisesti osaksi kontekstiaan. Referenssit ovat kuvailevaa taustamateriaalia: brändin ääni, sanasto, esimerkkejä hyvästä tekstistä, toimialasanakirjat.

Pohjareferenssit (`references/patterns.md`, `references/kielioppi.md`) pysyvät aina voimassa. Tämä kansio **laajentaa** niitä.

## Mihin tätä käytetään

- **Brändin ääni** — miten yrityksesi tai tuotteesi "kuulostaa" suomeksi
- **Sanastot ja glossarit** — toimialan termistö, kielletyt tai suositellut sanat
- **Esimerkkitekstit** — hyviä ja huonoja esimerkkejä omasta tuotannostasi
- **Kohdeyleisö** — kenelle kirjoitat (asiantuntijat, kuluttajat, B2B)
- **Tyylioppaat** — omat tai asiakkaan tyyliohjeet

## Miten lisätä referenssi

1. Luo `.md`-tiedosto tähän kansioon (esim. `brandi_aani.md`, `sanasto.md`)
2. Kirjoita sisältö luettavaan muotoon: otsikot, listat, esimerkit ennen/jälkeen
3. Suomettaja lukee tiedoston automaattisesti seuraavassa käytössä

## Esimerkkitiedostoja

```
custom_references/
  brandi_aani.md         # Acme Oy:n ääni: suora, tekninen, ei hypeä
  sanasto.md             # Toimialan termit ja niiden suomennokset
  hyvat_esimerkit.md     # Aiempia tekstejä joita pidettiin onnistuneina
  kohdeyleisö.md         # Kirjoitamme IT-päättäjille, ei loppukäyttäjille
```

## Esimerkki: brandi_aani.md

```markdown
# Acme Oy:n kirjoittajaääni

## Periaatteet
- Suora ja tekninen. Ei hypeä.
- Käytämme me-muotoa, emme passiivia.
- "Asiakas" ei "loppukäyttäjä".

## Ei näitä sanoja
- "ratkaisu" (liian epämääräinen) → kerro mikä se on
- "innovatiivinen" → näytä, älä kerro
```

## Ero `custom_rules/`-kansioon

- **`custom_references/`** = taustamateriaali, jota Suomettaja konsultoi (kuvaileva)
- **`custom_rules/`** = pakottavat säännöt, joita Suomettaja noudattaa (käskevä)

Jos epäröit kumpaan laittaa: jos sisältö on "älä koskaan / aina käytä" -muotoista, se kuuluu `custom_rules/`-kansioon. Jos se on "tässä on taustaa ja esimerkkejä", se kuuluu tänne.

## Versionhallinta

Tiedostot tässä kansiossa on oletuksena ignoroitu `.gitignore`ssa, jotta `git pull` ei riko omia mukautuksiasi. Jos haluat versioida omat referenssisi, tee niille oma repo tai poista ignore-sääntö paikallisesti.
