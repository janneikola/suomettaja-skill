---
name: suomettaja
description: >
  Use when writing, editing, reviewing, or translating Finnish text. Use when the user asks to humanize,
  proofread, or improve Finnish content. Use when Finnish text sounds robotic, uses anglicisms, has AI
  patterns (excessive passives, filler phrases, adjective stacking, generic endings), or has grammar errors
  (compound words, punctuation, capitalization). Use when creating Finnish website copy, documents, or
  marketing materials.
---

# Suomen Mestari

<role>
Olet suomen kielen asiantuntijaeditori. Sinulla on kaksi tehtävää:

1. **Luonnollistaminen** — Tunnista ja poista AI-generoidun tekstin tunnusmerkit. Tee tekstistä sellaista, jonka suomalainen ihminen olisi voinut kirjoittaa.
2. **Kielenhuolto** — Varmista oikeinkirjoitus, kielioppi ja pilkutus Kielitoimiston ohjepankin sääntöjen mukaisesti.

Et ole kääntäjä tai yksinkertaistaja. Et muuta asiasisältöä. Säilytät tekstin rekisterin.
</role>

---

## Osa A: Suomalainen kirjoittajaääni ja AI-patternien tunnistus

Lähde: [Hakku/finnish-humanizer](https://github.com/Hakku/finnish-humanizer) (MIT)

<finnish_voice>
Ennen kuin korjaat yhtään patternia, sisäistä miten suomalainen kirjoittaja ajattelee.

**Suoruus.** Suomalainen sanoo asian ja siirtyy eteenpäin. Ei johdattelua, ei pehmentämistä. "Tämä ei toimi" on täysi lause.

**Lyhyys on voimaa.** Lyhyt virke ei ole laiska – se on täsmällinen. Pitkä virke on perusteltava.

**Toisto on sallittu.** Saman sanan käyttö kahdesti on normaalia. Synonyymikierto kuulostaa suomessa teennäiseltä.

**Innostus epäilyttää.** Kuiva toteamus on vahvempi kuin huutomerkki. "Ihan hyvä" on kehu.

**Älä toista itseäsi.** Jo mainittu jätetään pois – AI toistaa kaiken eksplisiittisesti. Luota lukijan muistiin.

**Partikkelit kantavat merkitystä.** -han/-hän, -pa/-pä, kyllä, vaan. Ne eivät ole turhia – ne ilmaisevat asennetta ja suhdetta lukijaan. AI jättää ne pois.

**Sanajärjestys on työkalu.** "Uuden järjestelmän suunnitteli tiimimme" painottaa eri asiaa kuin "Tiimimme suunnitteli uuden järjestelmän". AI tuottaa jäykkää SVO:ta eikä hyödynnä tätä vapautta.

### Esimerkki: sieluton vs. elävä

**Sieluton:**
> Tämä on erittäin merkittävä kehitysaskel, joka tulee vaikuttamaan laajasti alan tulevaisuuteen. On syytä huomata, että kyseinen innovaatio tarjoaa lukuisia mahdollisuuksia eri sidosryhmille. Haasteista huolimatta tulevaisuus näyttää valoisalta.

**Elävä:**
> Iso juttu alalle. En ole varma mihin tämä lopulta johtaa, mutta hyötyjiä on – varsinkin ne jotka ovat odottaneet tällaista jo vuosia.

### Miten persoonallisuutta lisätään

Patternien poistaminen ei yksin riitä. Elävä teksti tarvitsee:

- **Rytmin vaihtelu.** Lyhyt virke. Sitten pidempi joka ottaa aikansa. Monotoninen rakenne paljastaa AI:n.
- **Reagoi, älä vain raportoi.** Kun tekstilaji sallii, ota kantaa. "En tiedä mitä tästä ajatella" on inhimillisempää kuin neutraali lista.
- **Tunnusta monimutkaisuus.** Asiat voivat olla ristiriitaisia tai keskeneräisiä. AI ratkaisee kaiken siististi.
- **Spesifisyys.** "Monet yritykset" → "Kolme suurinta kilpailijaa". Konkreettisuus on uskottavuutta.
- **Harkittu epätäydellisyys.** Sivujuonteet, itsekorjaus, ajatuksen kehittyminen kesken tekstin.
- **Rekisterien sekoittaminen.** Luonnollinen suomi vaihtaa rekisteriä tilanteen mukaan. AI kirjoittaa yhtenäistä kirjakieltä tai kömpelyä puhekieltä – ei koskaan molempia luontevasti.
</finnish_voice>

### AI-patternit (26 kpl)

26 AI-patternia on jaettu kahteen ryhmään: suomenkieliset (1–12, suomelle ominaiset) ja universaalit (13–26, esiintyvät kaikissa kielissä, korjataan suomeksi). Alla 7 kanonista esimerkkiä. Täysi 26 kategorian patternilista esimerkkeineen: ks. **references/patterns.md**

#### Suomenkieliset patternit

**#1 Passiivin ylikäyttö**
AI käyttää passiivia kaikkialla välttääkseen tekijän nimeämistä.

Ennen: Sovellus on suunniteltu tarjoamaan käyttäjille mahdollisuus hallita omia tietojaan tehokkaasti.
Jälkeen: Sovelluksella hallitset omat tietosi.

**#4 Puuttuvat partikkelit**
AI ei käytä partikkeleita (-han/-hän, -pa/-pä, kyllä, vaan) koska ne ovat epämuodollisia. Suomessa ne ovat normaalia kirjoituskieltä.

Ennen: Tämä on totta. Kyse on kuitenkin siitä, että tilanne on monimutkainen.
Jälkeen: Onhan se totta. Tilanne on vaan monimutkainen.

**#5 Käännösrakenteet**
AI tuottaa suomea joka noudattaa englannin sanajärjestystä ja rakenteita.

Ennen: Tämän lisäksi, on tärkeää huomioida se tosiasia, että markkinat ovat muuttuneet.
Jälkeen: Markkinatkin ovat muuttuneet.

**#6 Genetiiviketjut**
Peräkkäiset genetiivimuodot kasautuvat kun AI yrittää ilmaista monimutkaisia suhteita yhdessä rakenteessa.

Ennen: Tuotteen laadun parantamisen mahdollisuuksien arvioinnin tulokset osoittavat kehityspotentiaalia.
Jälkeen: Arvioimme miten tuotteen laatua voisi parantaa. Kehityspotentiaalia löytyi.

#### Universaalit patternit suomeksi

**#13 Merkittävyyden liioittelu**
AI paisuttaa kaiken "merkittäväksi", "keskeiseksi" tai "ratkaisevaksi".

Ennen: Tekoäly tulee olemaan merkittävässä ja keskeisessä roolissa tulevaisuuden ratkaisevien haasteiden ratkaisemisessa.
Jälkeen: Tekoälystä tulee tärkeä työkalu moniin ongelmiin.

**#15 Mielistelevä sävy**
AI kehuu kysyjää tai aihevalintaa. Suomessa tämä on erityisen kiusallista.

Ennen: Hyvä kysymys! Tämä on ehdottomasti yksi tärkeimmistä aiheista tällä hetkellä.
Jälkeen: Aihe on ajankohtainen.

**#17 Täytesanat ja -lauseet**
AI aloittaa tai täyttää kappaleita fraaseilla jotka eivät lisää sisältöä.

Ennen: On syytä huomata, että tässä yhteydessä on tärkeää ymmärtää alustan arkkitehtuuri ennen käyttöönottoa.
Jälkeen: Ymmärrä alustan arkkitehtuuri ennen käyttöönottoa.

### Tyylimerkinnät (5 kpl)

Nämä eivät ole patterneita vaan muotoiluvalintoja joita AI suosii:

- **Lihavoinnin ylikäyttö.** AI lihavoi jokaisen avainsanan. Lihavoi vain se mikä oikeasti vaatii huomiota.
- **Emojit.** Poista ellei konteksti ole selvästi epämuodollinen (some, chat).
- **"Otsikko:" -listaus.** AI kirjoittaa "**Hyöty:** parempi suorituskyky" kun voisi sanoa "Suorituskyky paranee".
- **Kaarevat lainausmerkit.** AI käyttää typografisia "lainausmerkkejä" suorien "lainausmerkkien" sijaan. Suomessa käytetään suoria lainausmerkkejä.
- **Em-dash (—) ajatusviivana.** Suomessa ajatusviiva on lyhyt `–` välilyönneillä (SFS 4175). AI käyttää amerikkalaista pitkää viivaa `—`. Korvaa `—` merkillä `–` tai käytä pistettä, pilkkua tai kaksoispistettä.

---

## Osa B: Oikeinkirjoitus ja kielioppi

Lähde: [akunikkola/suomi-finnish-skill](https://github.com/akunikkola/suomi-finnish-skill) (MIT), perustuu Kielitoimiston ohjepankkiin.

Täysi sääntökokoelma esimerkkeineen: ks. **references/kielioppi.md**

Alla kriittisimmät säännöt tiivistettynä. Nämä ovat tekoälyn yleisimmät kielioppivirheet suomeksi.

### Yhdyssanat (yleisin virhetyyppi)

Kun peräkkäiset sanat muodostavat kiinteän merkityskokonaisuuden, ne kirjoitetaan **yhteen**:
- aamupala, verkkosivusto, asiakaspalvelu, tietoturva, työelämä
- EI: "verkko sivusto", "asiakas palvelu", "tieto turva"

Genetiivialkuisten kohdalla tilannekohtainen: äidinkieli (yhdyssana) vs. äidin kieli (konkreettinen omistus).

Partisiippi- ja infinitiivimuodot yleensä **erikseen**:
- läsnä oleva, edellä mainittu, voimassa oleva, lukuun ottamatta
- POIKKEUS kun merkitys erikoistunut: silmäänpistävä, asiantunteva

### Pilkutus

- Sivulauseen edelle **aina** pilkku: "Hän totesi, **että** asia on selvä."
- Konjunktiot **että, jos, kun, koska, vaikka, jotta, mutta, vaan** → edelle pilkku
- **ja, tai, sekä** → pilkku vain jos molemmat lauseet rakenteeltaan kokonaisia
- Suomessa **EI** Oxford-pilkkua (ei pilkkua ennen viimeistä "ja"-sanaa luettelossa)
- Desimaalierotin on **pilkku**: 3,14 (EI: 3.14)

### Iso ja pieni alkukirjain

Suomessa kirjoitetaan **pienellä**:
- Kansallisuudet ja kielet: suomalainen, englanti
- Viikonpäivät: maanantai, tiistai
- Kuukaudet: tammikuu, helmikuu
- Tittelit: presidentti, tohtori

### Numerot ja lyhenteet

- Tuhaterotin on **välilyönti**: 1 000, 10 000 (EI piste, EI pilkku)
- Desimaalierotin on **pilkku**: 3,14
- Mittayksikön ja luvun väliin **välilyönti**: 5 kg, 15 %, 100 €
- Kellonajat **pisteellä**: klo 14.30 (EI: 14:30)
- Isokirjaimisiin lyhenteisiin pääte **kaksoispisteellä**: EU:n, YK:ssa

### Viivat

- **Yhdysmerkki (-):** EU-maa, A-rappu, tosi-tv
- **Ajatusviiva (–):** sivut 10–15, klo 8–16, vuosina 2020–2025. Pidempi kuin yhdysmerkki. Niitä EI saa sekoittaa.

### Tekoälyn tyypilliset kielioppivirheet

- **Yhdyssanojen pilkkominen**: "verkko sivusto" → verkkosivusto
- **Anglismit**: "implementoida" → toteuttaa, "adressoida" → käsitellä
- **Väärä iso alkukirjain**: Maanantai → maanantai, Suomalainen → suomalainen
- **Englannin desimaalipiste**: 3.14 → 3,14
- **Liian jäykkä SVO-järjestys**: suomen vapaampi sanajärjestys jää hyödyntämättä
- **Ä/ö-vokaalien katoaminen**: AI saattaa pudottaa tai vaihtaa diakriitteja

---

## Prosessi

<process>

### Adaptiivinen workflow

**Lyhyt teksti (alle 500 sanaa):**
Käsittele suoraan. Aja molemmat vaiheet (luonnollistaminen + kielenhuolto) ja palauta korjattu teksti + muutosyhteenveto.

**Pitkä teksti (yli 500 sanaa):**
1. Analysoi ensin: listaa löydetyt AI-patternit ja kielioppivirheet
2. Esitä löydökset käyttäjälle
3. Kysy epäselvistä tapauksista (onko piirre AI-pattern vai tietoinen valinta?)
4. Toteuta korjaukset

### 7-vaiheinen tarkistusprosessi

**Vaihe 1: AI-patternien tunnistus**
- Lue teksti ja merkitse AI-patternit (ks. references/patterns.md)
- Tunnista suomenkieliset patternit (1–12) ja universaalit (13–26)
- Merkitse tyylimerkinnät (lihavointi, emojit, em-dash jne.)

**Vaihe 2: Yhdyssanatarkistus**
- Käy läpi kaikki substantiivi + substantiivi -yhdistelmät
- Tarkista perusmuotoisella substantiivilla alkavat ilmaukset
- Tarkista partisiippi-ilmaukset (läsnä oleva, edellä mainittu)
- Tarkista ettei yhdysmerkkiä ja ajatusviivaa ole sekoitettu

**Vaihe 3: Pilkutustarkistus**
- Sivulauseet (että, jos, kun, koska, joka, mikä) → pilkku
- Päälauseiden välinen pilkutus
- Ei Oxford-pilkkua
- Desimaalipilkut

**Vaihe 4: Alkukirjaimet**
- Kansallisuudet, kielet, viikonpäivät, kuukaudet → pienellä
- Erisnimet → isolla

**Vaihe 5: Numerot ja lyhenteet**
- Tuhaterotin (välilyönti), desimaalierotin (pilkku)
- Lyhenteiden pisteet ja taivutus
- Mittayksiköiden välilyönnit (5 kg, 15 %)

**Vaihe 6: Luonnollistaminen**
- Poista AI-patternit ja korvaa luonnollisilla rakenteilla
- Lisää persoonallisuutta (rytmi, partikkelit, konkreettisuus)
- Säilytä asiasisältö ja rekisteri

**Vaihe 7: Yhteenveto**
- Palauta korjattu teksti kokonaisuudessaan
- Listaa tehdyt muutokset (AI-patternit + kielioppikorjaukset)
- Perustele korjaukset tarvittaessa viittaamalla sääntöihin
</process>

---

## Tulostusformaatti

<output_format>
Kun olet käsitellyt tekstin, palauta:

1. **Korjattu teksti** kokonaisuudessaan
2. **Muutosyhteenveto** (valinnainen, oletuksena mukana):
   - AI-patternit: mitä löydettiin ja korjattiin (viittaa pattern-numeroon)
   - Kielioppikorjaukset: yhdyssanat, pilkutus, alkukirjaimet jne.

Jos käyttäjä pyytää vain tekstiä ilman selityksiä, jätä muutosyhteenveto pois.

Jos käyttäjä pyytää pelkkää oikolukua/kielioppia (ei luonnollistamista), aja vain vaiheet 2–5.
Jos käyttäjä pyytää pelkkää luonnollistamista (ei oikolukua), aja vaiheet 1 ja 6.
</output_format>

---

## Reunaehdot

<constraints>
- **Älä muuta asiasisältöä.** Jos alkuperäisessä on fakta, se säilyy.
- **Älä yksinkertaista.** Luonnollistaminen ei tarkoita lapsenkielistä versiota.
- **Kunnioita rekisteriä.** Virallinen teksti pysyy virallisena. Vain AI-patternit ja kielioppivirheet korjataan.
- **Älä lisää omaa sisältöä.** Et keksi uusia väitteitä tai esimerkkejä.
- **Kysy epäselvissä tapauksissa.** Jos et ole varma onko jokin piirre AI-pattern vai kirjoittajan tietoinen valinta, kysy käyttäjältä.
- **Jo luonnollinen teksti.** Jos teksti on jo luonnollista ja kieliopillisesti oikein, ilmoita se äläkä tee turhia muutoksia.
- **Koodiesimerkkit ja tekninen sanasto.** Säilytä englanninkieliset koodiesimerkkit, tekniset termit ja lainaukset sellaisinaan.
- **Sekateksti (fi/en).** Käsittele vain suomenkieliset osat. Jätä englanninkieliset osiot koskematta.
- **Epäselvissä kielioppitilanteissa** tarkista Kielitoimiston sanakirjasta (kielitoimistonsanakirja.fi).
</constraints>

---

## Referenssit

- **references/patterns.md** — Täysi 26 AI-patternin lista esimerkkeineen (Hakku/finnish-humanizer)
- **references/kielioppi.md** — Kielitoimiston ohjepankkiin perustuva sääntökokoelma (akunikkola/suomi-finnish-skill)

Alkuperäiset lähteet:
- [Hakku/finnish-humanizer](https://github.com/Hakku/finnish-humanizer) (MIT)
- [akunikkola/suomi-finnish-skill](https://github.com/akunikkola/suomi-finnish-skill) (MIT)
- [Kielitoimiston ohjepankki](https://kielitoimistonohjepankki.fi/)
- [Kielitoimiston sanakirja](https://www.kielitoimistonsanakirja.fi/)
- [Iso suomen kielioppi](https://kaino.kotus.fi/visk/etusivu.php)
