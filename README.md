# Håkon Færgestad Trafikkopplæring – nettside (utkast)

High-end statisk nettside for **Håkon Færgestad Trafikkopplæring** (Ski), bygget ved å rebrande STEP-/Just Drive-malen til Håkons egen merkevare og innhold.

## Forhåndsvisning
Fra prosjektmappen:

```
node scripts/serve.mjs        # http://localhost:5500
node scripts/validate.mjs     # sjekker lenker + at ingen leftovers gjenstår
```

## Designgrunnlag
- **Mal:** samme komponentbibliotek som de andre trafikkskole-sidene (selvhostede fonter – Space Grotesk + Plus Jakarta Sans).
- **Profil:** mørk og premium, tilpasset HF-logoen (hvit monokrom) og hero-bildet (mørk Tesla i solnedgang ved fjord).
- **Aksentfarge:** varm **kobber/amber (`--accent #B4551E`)** + lys amber (`--accent-bright #E8994F`), plukket fra solnedgangen i heroen. Skiller seg fra Just Drive (magenta), Step og Elite.
- **Logo:** `img/logo-hvit.png` (hvit) brukes overalt. Over mørk hero vises den hvit; på lys, «solid» nav ved scroll gjøres den svart via CSS-filter (`brightness(0)`).
- **Hero/OG:** `img/hf-hero.jpg` (optimalisert fra kundens PNG). `img/og.jpg` er 1200×630 for delingskort. `img/favicon.png` er HF-monogrammet på mørk bakgrunn.
- **Ingen TABS-kobling:** denne skolen er *ikke* koblet til TABS. All booking/elevinnlogging er fjernet – «Meld deg på» går til kontaktskjemaet. Ingen kommende-kurs-import.
- Ingen falske Google-score, garantier eller anmeldelser.

## Sider
| Fil | Innhold |
|---|---|
| `index.html` | Hjem – hero, opplæring (B, trafikalt, trafikant i mørket), «Derfor Håkon», pris-utdrag, sted, om Håkon, FAQ |
| `klasse-b.html` | Klasse B – bil (automat og manuell), firetrinnsmodellen, aldersgrenser, pris-utdrag |
| `trafikalt-grunnkurs.html` | Trafikalt grunnkurs (inkl. trafikant i mørket + førstehjelp), priser, påmelding |
| `kommende-kurs.html` | Kommende kurs – datoliste for grunnkurs, trafikant i mørket og førstehjelp |
| `priser.html` | Prisliste med faner (Klasse B / Trafikalt grunnkurs) + gebyrer + «godt å vite» |
| `om-oss.html` | Om Håkon – én fast trafikklærer siden 1998 |
| `kontakt.html` | Kontakt – telefon, e-post, område, påmeldingsskjema, kart over Ski |
| `vilkar.html` | Vilkår (foreløpige, noindex) |

## Håkon Færgestad-info (verifisert mot Brønnøysund + skitrafikkskole.no)
- **Org.nr** 989 180 568 · HÅKON FÆRGESTAD TRAFIKKOPPLÆRING (enkeltpersonforetak) · næringskode 85.531 (trafikkskole) · registrert 2006.
- **Sted:** Ski (Nordre Follo, Akershus). Kjører i Ski og Follo. Oppmøtested etter avtale.
- **Telefon:** 901 60 065 (Håkons direktenummer som trafikklærer, hentet fra skitrafikkskole.no).
- **Bakgrunn:** utdannet trafikklærer ved Statens trafikklærerskole i 1998, sertifisert for bil (klasse B) og førstehjelp.
- **Klasser:** Klasse B (automat + manuell) og trafikalt grunnkurs (med trafikant i mørket + førstehjelp). **Ingen** MC eller BE (Håkon er ikke registrert for dette).

## Priser
Hentet fra **skitrafikkskole.no** per 2026-07-01 (Håkon jobber i dag der, og prøvesteder Drøbak/Mysen stemmer for Ski-området). Eksempler: kjøretime 45 min 950 kr, 60 min 1 270 kr; sikkerhetskurs på øvingsbane 7 300 kr; trafikalt grunnkurs 2 300 kr (sommer) / 4 500 kr (med mørkekjøring). Gebyrer hos Statens vegvesen 2026.

## MÅ GJØRES FØR LANSERING
1. **Bekreft prisene med Håkon.** Prisene er hentet fra Ski Trafikkskole. Kjører Håkon egne priser når han starter for seg selv, må de oppdateres (`priser.html`, pris-utdrag på `index.html` og `klasse-b.html`, `trafikalt-grunnkurs.html`).
2. **Kommende kurs – datoer.** Datoene i `kommende-kurs.html` (og teaseren på forsiden) er eksempler (aug–nov 2026). Sett inn Håkons faktiske kursdatoer før lansering.
3. **Domene.** Canonical/OG/sitemap bruker `hakonfergestad.no` (antatt). Bekreft endelig domene og oppdater ved behov.
4. **E-post.** `post@hakonfergestad.no` er antatt. Bekreft, eller bytt til Håkons faktiske e-post.
5. **Kontaktskjema:** bruker demo-handler (viser takk-melding). Koble til ekte endepunkt (f.eks. Web3Forms) – markert med TODO i `kontakt.html`.
6. **Telefon:** 901 60 065 er hentet fra Ski Trafikkskole. Bekreft at dette er nummeret Håkon vil bruke.
7. **Adresse:** Vi publiserer ikke gateadresse (den registrerte i Brreg er trolig hjemmeadresse). Siden bruker «Ski og omegn – oppmøtested etter avtale». Avklar om Håkon vil oppgi en fast adresse.
8. **Kurstilbud:** Bekreft at kurslinjen (Klasse B + trafikalt grunnkurs) stemmer. Vil han også tilby BE/oppfriskning, kan det legges til.
9. **Sosiale medier:** ingen lenker lagt inn (ingen bekreftede kontoer). Legg til Facebook/Instagram hvis han har.
10. **Vilkår:** foreløpige – gjennomgå før publisering.

## Kilde
Research mot Brønnøysund Enhetsregisteret og skitrafikkskole.no. Levert av Larsen Digital Solutions, 2026-07-01.
