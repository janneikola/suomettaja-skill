# Suomettaja — Finnish Language Editing Skill for Claude Code, Codex and any other AI that supports skills

A skill that improves Finnish text quality. Removes AI-generated patterns, enforces grammar rules from Kielitoimiston ohjepankki, and naturalizes robotic-sounding content into authentic Finnish voice.

---

## Mitä se tekee

**Luonnollistaminen** — Tunnistaa ja poistaa AI-generoidun tekstin tunnusmerkit (26 patternia). Tekee tekstistä sellaista, jonka suomalainen ihminen olisi voinut kirjoittaa.

**Kielenhuolto** — Tarkistaa oikeinkirjoituksen, kieliopin ja pilkutuksen Kielitoimiston ohjepankin sääntöjen mukaisesti.

### Tunnistettavat AI-patternit (26 kpl)

Suomenkieliset patternit:
- Passiivin ylikäyttö
- Nominaalirakenteet ("suorittaa tarkistuksen" → "tarkistaa")
- Pronominien ylikäyttö englannin mallin mukaan
- Puuttuvat partikkelit (-han/-hän, -pa/-pä, kyllä, vaan)
- Käännösrakenteet (englannin sanajärjestys suomessa)
- Genetiiviketjut
- Adjektiivikasaumat
- Ylipitkät virkkeet
- Joka/jotka-kasautuminen
- Virkakielisyys väärässä kontekstissa

Universaalit patternit (suomeksi):
- Merkittävyyden liioittelu ("keskeinen", "ratkaiseva", "elintärkeä")
- Mainosmainen kieli
- Mielistelevä sävy ("Hyvä kysymys!")
- Täytesanat ("On syytä huomata, että...")
- Geneerinen lopetus ("Tulevaisuus näyttää valoisalta")
- Ja 11 muuta — ks. [references/patterns.md](references/patterns.md)

### Kielioppisäännöt

- Yhdyssanat (yleisin virhetyyppi: "verkko sivusto" → verkkosivusto)
- Pilkutus (sivulauseet, Oxford-pilkku, desimaalipilkku)
- Iso/pieni alkukirjain (kansallisuudet, viikonpäivät, kuukaudet pienellä)
- Numerot ja lyhenteet (tuhaterotin välilyönti, EU:n, 15 %)
- Viivat (yhdysmerkki `-` vs. ajatusviiva `–`)

---

## Asennus

### Claude Code

```bash
# Kloonaa suoraan skills-kansioon
git clone https://github.com/janneikola/suomettaja-skill ~/.claude/skills/suomettaja
```

Skill aktivoituu automaattisesti seuraavassa Claude Code -sessiossa.

### Manuaalinen asennus

1. Lataa tai kloonaa tämä repo
2. Kopioi kansio `~/.claude/skills/suomettaja/`
3. Varmista rakenne:
   ```
   ~/.claude/skills/suomettaja/
     SKILL.md
     references/
       kielioppi.md
       patterns.md
     custom_references/    # valinnainen: omat lisäreferenssit
     custom_rules/         # valinnainen: omat lisäsäännöt
   ```

---

## Käyttö

Skill triggeröityy automaattisesti kun:
- Kirjoitat tai muokkaat suomenkielistä tekstiä
- Pyydät "humanisoimaan", "oikolukemaan" tai "parantamaan" suomea
- Teksti kuulostaa robottimaaiselta tai käyttää anglismeja

Voit myös kutsua sitä suoraan:

```
Suometa tämä teksti: [teksti]
```

```
Oikolue ja luonnollista: [teksti]
```

### Esimerkki

**Ennen:**
> Tämä on erittäin merkittävä kehitysaskel, joka tulee vaikuttamaan laajasti alan tulevaisuuteen. On syytä huomata, että kyseinen innovaatio tarjoaa lukuisia mahdollisuuksia eri sidosryhmille. Haasteista huolimatta tulevaisuus näyttää valoisalta.

**Jälkeen:**
> Iso juttu alalle. En ole varma mihin tämä lopulta johtaa, mutta hyötyjiä on — varsinkin ne jotka ovat odottaneet tällaista jo vuosia.

---

## Tiedostorakenne

```
suomettaja/
  SKILL.md                  # Pääskilli: rooli, prosessi, säännöt
  references/
    patterns.md             # Kaikki 26 AI-patternia esimerkkeineen
    kielioppi.md            # Kielitoimiston ohjepankin säännöt
  custom_references/        # Omat lisäreferenssit (brändin ääni, sanastot)
    README.md
  custom_rules/             # Omat lisäsäännöt (kielletyt sanat, termit)
    README.md
  README.md
  LICENSE
```

---

## Mukautukset

Voit laajentaa Suomettajaa omilla tiedostoilla ilman että pohjaskilliä muokataan. Kaksi kansiota:

- **`custom_references/`** — kuvaileva taustamateriaali: brändin ääni, sanastot, hyvät esimerkit, kohdeyleisön kuvaus
- **`custom_rules/`** — käskevät direktiivit: kielletyt sanat, pakolliset termit, projektikohtaiset tyylivalinnat

Lisää vain `.md`-tiedostoja kansioihin. Suomettaja lukee ne automaattisesti seuraavassa käytössä.

**Esimerkki:**

```
custom_rules/
  brandin_termit.md    # "Acme Cloud" ei "acme cloud" tai "Acme-pilvi"
  kielletyt_sanat.md   # "ratkaisu", "innovatiivinen", "helppo"
```

**Sääntöhierarkia:** Kielioppi ja oikeinkirjoitus (`references/`) ovat aina voimassa. Omat säännöt (`custom_rules/`) voivat tiukentaa tyylivalintoja mutta eivät ohittaa kielioppisääntöjä.

Tarkemmat ohjeet ja esimerkit: [`custom_references/README.md`](custom_references/README.md) ja [`custom_rules/README.md`](custom_rules/README.md).

**Versionhallinta.** Omat tiedostot on ignoroitu `.gitignore`ssa, joten `git pull` ei riko mukautuksiasi.

---

## Lähteet

Skill yhdistää kaksi MIT-lisensoitua avoimen lähdekoodin projektia:

- **[Hakku/finnish-humanizer](https://github.com/Hakku/finnish-humanizer)** — 26 AI-patternia ja suomalaisen kirjoittajaäänen kuvaus
- **[akunikkola/suomi-finnish-skill](https://github.com/akunikkola/suomi-finnish-skill)** — Kielitoimiston ohjepankkiin perustuva kielioppiohjeistus

Kielioppisäännöt perustuvat:
- [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/)
- [Kielitoimiston sanakirja](https://www.kielitoimistonsanakirja.fi/)
- [Iso suomen kielioppi](https://kaino.kotus.fi/visk/etusivu.php)

---

## Lisenssi

MIT — ks. [LICENSE](LICENSE)
