# TODO – Bachelorproef "De efficiëntie van gamification bij het aanleren van COBOL"

> Status: april 2026. Onderzoeksaanpak gewijzigd naar **Plan B3 (vergelijkende literatuurevaluatie)**: er is geen empirische gebruikersstudie meer voorzien binnen de scope van de bachelorproef. De PDF is 82 pagina's en compileert zonder fouten.

---

## ✅ Klaar

- **Voorwoord, samenvatting en conclusie** geschreven en herwerkt voor Plan B3.
- **Voorwoord** weerspiegelt de Mainframe-keuzerichting (eigen COBOL-kennis als startpunt + wens om de instap voor anderen te verlichten).
- **Hoofdstuk 4** volledig herschreven als *Vergelijkende literatuurevaluatie*:
  - Per ontwerpkeuze (PBL, Octalysis Core Drives, MDA, didactisch ontwerp) een literatuur-onderbouwde plausibiliteitscheck.
  - Tabel die alle 8 Octalysis Core Drives koppelt aan de PoC-implementatie + verwachte richting.
  - Synthese per deelvraag (DV1–DV5) met verwijzing naar de bron-hoofdstukken.
  - Sectie *Beperkingen* en concrete *Aanbevelingen voor empirische opvolging* (binnen-subject design met counterbalancing als follow-up).
- **Methodologie Fase 3** geherformuleerd voor literatuurevaluatie.
- **Inleiding hoofdstuk-overzicht** bijgewerkt.
- **Lijst van afkortingen** opgekuist (IRL/IQR/SD/UX verwijderd, niet meer gebruikt).
- **Bibliografie** opgekuist: `Sauro2018` en `Nielsen1994` weggehaald (waren enkel voor empirische opzet); `Bangor2009` blijft (gebruikt in aanbeveling voor SUS-interpretatie).
- **Standalone bijlagen** (PDF-pack blok A/B + SUS-vragenlijst) blijven op `bachproef/bijlagen/` staan voor wie ze later alsnog wil gebruiken in een empirische opvolgstudie. Ze worden **niet** in de huidige bachelorproef ingevoegd.
- Stand van zaken: OOP-paragraaf (gebruikt `IBM2025a`), Octalysis afgewerkt, Gamification-bij-junior-devs uitgebreid, gap-analyse rond ontbrekende COBOL-tools.
- PoC: leaderboard-sectie en viering-sectie toegelicht.
- `\template{...}`-macro verwijderd (geen TEMPLATE-blokken meer nodig).
- Terminologie geconsolideerd op *gamification* (titel + body consistent).
- Hoofdtitel: *De efficiëntie van gamification bij het aanleren van COBOL aan junior developers*.

---

## ⚠️ Nog te doen vóór indiening

### 1. Inhoudelijke review (door jezelf en/of promotor)

- [ ] Lees hoofdstuk 4 grondig na: zijn alle literatuur-claims correct geïnterpreteerd? Vooral de SMD-cijfers van Zhan2022 en de KevinWerbach-uitspraken over leaderboards.
- [ ] Lees voorwoord en samenvatting na op stijl en lengte (samenvatting nu ±1 pagina, voorwoord ±0,5 pagina).
- [ ] Controleer of de mainframe-jargon-strips in hoofdstuk 3 (PoC) consistent en accuraat zijn.

### 2. Eindcontrole bij finale compilatie

- [ ] Visueel doorbladeren van de gegenereerde PDF (`output/DeVuystSilasBP.pdf`):
  - Geen blanco pagina's.
  - Geen `??` in plaats van `\ref{...}`.
  - Tabel `tab:eval-octalysis` past op één pagina.
  - Alle figuren correct genummerd.
- [ ] Spellings- en grammaticacheck (NL).
- [ ] Citatie-stijl: punt-vóór of punt-ná `\autocite{}` consistent (er staat nu nog een mengeling).
- [ ] De `xdvipdfmx: Annotation out of page boundary` waarschuwing in de bibliografie: niet kritiek, maar als je perfectionistisch bent kan je de URL die over de marge loopt manueel splitsen.

### 3. Optioneel — extra polish

- [ ] Spellingscheck voor titelblad: `\title{De efficiëntie van gamification \ldots}` — controleer of dit nog overeenkomt met de officieel ingediende titel bij HOGENT (oorspronkelijk *gamificatie*).
- [ ] `bachproef/bijlagen/` map: als je zeker bent dat je de empirische opvolgstudie nooit gaat doen, kan deze map gewoon weg. Anders: laten staan, ze compileert je niets in de huidige thesis.
- [ ] Voorstel-bijlage (`voorstel/voorstel-inhoud.tex`): de tekst beschrijft nog de oorspronkelijke tweegroepenopzet. Dit is correct als historisch document; de noot in `DeVuystSilasBP.tex` legt al uit waarom de aanpak veranderde.

### 4. Git-opkuis (geen blocker)

- [ ] Beslissen of `bachproef/TODO.md` mee in repo blijft (handig als werkdocument) of in `.gitignore` komt.
- [ ] Commit alle wijzigingen met een nette message.

---

## Snelle navigatie

```bash
# Belangrijkste bestanden
bachproef/DeVuystSilasBP.tex            # hoofdfile
bachproef/voorwoord.tex                 # voorwoord
bachproef/samenvatting.tex              # abstract
bachproef/inleiding.tex                 # hoofdstuk 1
bachproef/standvanzaken.tex             # hoofdstuk 2
bachproef/methodologie.tex              # hoofdstuk 3 (Fase 1-4)
bachproef/proofofconcept.tex            # hoofdstuk 4 (PoC)
bachproef/evaluatieEnResultaten.tex     # hoofdstuk 5 (literatuurevaluatie)
bachproef/conclusie.tex                 # hoofdstuk 6
bachproef/afkortingen.tex               # lijst afkortingen
bachproef/bachproef.bib                 # bibliografie
bachproef/bijlagen/                     # standalone PDF's voor evt. opvolging (niet in BP)

# Bouwen
.\make_thesis.bat                       # PDF in output/DeVuystSilasBP.pdf
```
