# TODO – Review bachelorproef (Plan B3-versie)

> Volledige doorloop van alle hoofdstukken op zoek naar inconsistenties, ontbrekende details, onduidelijkheden, irrelevante content en bib-issues. Sorteer per prioriteit (kritiek → polish).

---

## 🔴 KRITIEK – Inconsistenties met Plan B3

Deze items spreken elkaar tegen of zijn niet meer waar sinds de overstap naar literatuurevaluatie. Zij **moeten** weg vóór indiening, anders straft de promotor je af op tegenstrijdigheid.

- [ ] **`inleiding.tex` regel 73 — Onderzoeksdoelstelling vermeldt nog "proefpersonen".**
  > *"Het succes van dit onderzoek wordt gemeten aan de hand van de gebruikservaring en de snelheid waarmee **proefpersonen** de basisconcepten van COBOL succesvol weten toe te passen in vergelijking met klassieke methoden."*
  - Plan B3 heeft géén proefpersonen. Herschrijf naar iets als: *"Het succes wordt afgemeten aan de mate waarin de gemaakte ontwerpkeuzes door bestaand empirisch onderzoek worden ondersteund, en aan de bruikbaarheid van de PoC als startpunt voor een toekomstige empirische opvolgstudie."*

- [ ] **`proofofconcept.tex` regel 11 — PoC zegt nog "gebruikersevaluatie".**
  > *"De PoC ... dient als basis voor de **gebruikersevaluatie (interviews, observaties)**."*
  - Wijzigen naar: *"... dient als concreet artefact dat in hoofdstuk~\ref{ch:evaluatie} via een vergelijkende literatuurevaluatie tegen bestaand onderzoek wordt afgezet."*

- [ ] **`standvanzaken.tex` laatste zin (regel 503) — Voorspelt nog een SUS-meting.**
  > *"Hoe de effectiviteit van die toepassing concreet wordt gemeten (via **SUS, leeruitkomsten, tijd-tot-succes, iteraties en een kwalitatieve thematische analyse**) wordt verder uitgewerkt in hoofdstuk~\ref{ch:evaluatie}."*
  - Wijzigen naar: *"Hoe de plausibiliteit van die toepassing wordt geëvalueerd via een vergelijkende literatuurstudie wordt verder uitgewerkt in hoofdstuk~\ref{ch:evaluatie}."*

- [ ] **`methodologie.tex` Fase 4 (regel 61–62) — Spreekt over "verzamelde data".**
  > *"In de finale fase worden alle **verzamelde data geanalyseerd en gesynthetiseerd**."*
  - Plan B3 verzamelt geen data. Herschrijven naar: *"In de finale fase worden de bevindingen uit de literatuurevaluatie gesynthetiseerd ..."* of vergelijkbaar.

- [ ] **`proofofconcept.tex` tabel `tab:schema-app-events` caption (regel 222) — Telemetrie voor onderzoek.**
  > *"Structuur van de tabel app\_events (telemetrie / **onderzoeksondersteuning**)"*
  - Bij Plan B3 wordt `app_events` niet meer voor onderzoek gebruikt. Wijzig caption naar: *"telemetrie (klaar voor empirische opvolging, niet gebruikt in deze BP)"* of laat "/onderzoeksondersteuning" weg.

- [ ] **`proofofconcept.tex` regel 235 — Vercel Analytics als "gebruiksstatistieken".**
  > *"Vercel Analytics en Speed Insights zijn ingeschakeld voor aggregated performance- en **gebruiksstatistieken**."*
  - Suggereert dat je ze gebruikt voor het onderzoek. Voeg toe: *"...; deze worden niet als onderzoeksdata gebruikt in deze BP."*

---

## 🟠 HOOG – Ontbrekende details / onduidelijke passages

- [ ] **`proofofconcept.tex` regel 334 — Typo / mismatched parenthesis in opsomming "Tips / documentatie):"**
  > Letterlijk staat er: `\textbf{Tips / documentatie):}` (haakje sluit zonder open). Zou moeten zijn: `\textbf{Tips / documentatie:}` of `\textbf{Tips (en documentatie):}`.

- [ ] **`proofofconcept.tex` regels 298–306 — COBOL-functie listing heeft TWEE `STOP RUN.`**
  > De `ADD-NUMBERS.` paragraaf eindigt met `STOP RUN.` *en* `MAIN.` ook. Het programma stopt dus ná `ADD-NUMBERS` en de `MAIN`-paragraaf wordt nooit bereikt — semantisch fout en verwarrend voor lezers die zelf COBOL leren. Verwijder de `STOP RUN.` uit `ADD-NUMBERS` of zet `MAIN` boven `ADD-NUMBERS`.

- [ ] **`proofofconcept.tex` tabel `tab:schema-badge-definitions` (regel 168) — `tier` vs `difficulty` ondefinieerd.**
  > Beide kolommen worden in één regel beschreven als "Presentatie (zeldzaamheid, moeilijkheidsgraad)". Splits in twee regels of leg uit hoe ze van elkaar verschillen (anders waarom twee kolommen?).

- [ ] **`proofofconcept.tex` `tab:schema-level-attempts` (regel 152) — `syntax_error_count` zonder context.**
  > Wordt deze kolom ergens in de tekst gebruikt? Zo niet, schrap hem of geef voorbeeld van wat de PoC ermee doet.

- [ ] **`proofofconcept.tex` §3.4 Authenticatie (regel 238–248) — te summier.**
  > 1 zin over registratie + 1 over redirect. Vul aan: e-mailverificatie ja/nee, sessieduur, of `auth.uid()` gebruikt wordt voor RLS, wat er gebeurt bij accountverwijdering.

- [ ] **`methodologie.tex` Fase 1 (regel 35–42) — Mist methodische verantwoording van literatuurselectie.**
  > Welke databases? Welke zoektermen? Inclusiecriteria voor bronnen? Een korte alinea over zoekstrategie maakt de literatuurstudie verifieerbaar en past beter bij wat een promotor verwacht in een methodologie-hoofdstuk.

- [ ] **`methodologie.tex` Fase 2 (regel 44–49) — "Iteratief proces" zonder detail.**
  > Hoeveel iteraties? Reviewmomenten? Beslissingsmomenten? Eén tot twee zinnen extra zou de Fase 2 een echte methodische beschrijving maken.

- [ ] **`evaluatieEnResultaten.tex` §5.4 tabel `tab:eval-octalysis` — schaal "zwak/matig/sterk/polariserend/risicovol" niet gedefinieerd.**
  > De rechterkolom gebruikt termen als "Positief, sterk", "Polariserend", "Risicovol bij overgebruik" zonder ergens uit te leggen waarop die kwalificatie steunt. Voeg vóór de tabel een korte legenda toe: bv. *"Positief sterk = meta-analyse rapporteert medium-tot-grote effectgrootte; positief matig = case-studies zonder meta-analyse; polariserend = literatuur rapporteert zowel positieve als negatieve effecten; ..."*

- [ ] **`conclusie.tex` aanbeveling 1 (regel 25) — "Combineer interactiviteit en diepgang" niet onderbouwd.**
  > De claim *"een hybride aanpak ... wordt door de literatuur het sterkst ondersteund"* heeft geen citaat. Ofwel concrete bron toevoegen (bv. teruglinken naar §5.6 *Interactiviteit versus statische COBOL-leermiddelen*), ofwel claim verzachten ("lijkt aannemelijk op basis van ...").

- [ ] **`inleiding.tex` regel 28 — "AI-gestuurde feedback-loops" is een buzzword zonder context.**
  > Geen citaat, geen voorbeeld. Ofwel concretiseren (Copilot, Cursor, AI tutor) en bron geven, ofwel schrappen.

- [ ] **`inleiding.tex` regel 42 + 72 — Octalysis genoemd zonder citaat.**
  > Het eerste vermelden van Octalysis (regel 42) en de naam Yu-kai Chou (regel 72) hebben geen `\autocite{Chou2015}`. In een inleiding wordt minimaal geciteerd, maar de eerste vermelding van een eigenaam-framework hoort wel een cite te krijgen.

- [ ] **`standvanzaken.tex` regel 38 — "ongeëvenaarde verwerkingskracht" zonder bron.**
  > Het bullet over Retail/Logistiek heeft geen `\autocite{}` terwijl de andere twee bullets in dezelfde lijst er wel een hebben. Bron toevoegen of het bullet verzachten/schrappen.

- [ ] **`standvanzaken.tex` §2.1.3 — Kyndryl-cijfers zonder context over de survey.**
  > "80% van de bedrijven heeft in 2025 hun mainframe-strategie aangepast" — voeg in 1 zin toe wat de scope van de Kyndryl-survey is (aantal respondenten, doelgroep) zodat de lezer weet hoe representatief die 80% is.

---

## 🟡 MEDIUM – Layout, typografie en bib

### Bibliografie

- [ ] `bachproef.bib` `Hunicke2004` — entry-type `@Article` is fout (het is een conferentie-paper). Wijzig naar `@InProceedings` of `@Misc` met `howpublished` en voeg een URL toe (bv. de officiële PDF op http://www.cs.northwestern.edu/~hunicke/MDA.pdf).
- [ ] `bachproef.bib` `KevinWerbach2020` — `publisher` ontbreekt (zou *Wharton School Press* moeten zijn).
- [ ] `bachproef.bib` `Chou2015` — `publisher` ontbreekt (zou *Octalysis Media* moeten zijn).
- [ ] `bachproef.bib` `TutorialsPoint` — geen `date` veld; biblatex toont dan "n.d." of laat het weg, wat onnetjes oogt. Vul aan of vervang door een academische bron.
- [ ] `bachproef.bib` `IBM2010` en `Ebbers2011` — bevatten zowel `date` als `year` (redundant). Verwijder `year`.
- [ ] `bachproef.bib` `Allied2022` — gebruikt `year` in plaats van `date`. Standaardiseren op `date`.
- [ ] `TutorialsPoint` en `IBMMainframer2021` zijn niet-academische tutorial-websites. Een promotor kan vragen om deze te vervangen door:
  - Officiële IBM-documentatie (`IBM2023` *Enterprise COBOL Language Reference*) — die heb je al in de bib, dus zou je ze grotendeels kunnen vervangen door extra `\autocite{IBM2023}`'s op de plekken waar nu TutorialsPoint of IBMMainframer staan.

### Typografie / layout

- [ ] **`standvanzaken.tex` regels 390 + 396 — `\\ \\` als witregel-hack in §2.3.2.3.**
  > LaTeX gebruikt lege regels (paragraph breaks), niet `\\ \\`. Vervang door echte alinea-breuken voor cleaner output.
- [ ] **`proofofconcept.tex` regels 449–451, 473–475, 481–483, 489–491, 497–499, 505–507, 513–515 — `\\` aan einde van elke regel in level-beschrijvingen.**
  > Per level worden vier feiten gescheiden met `\\` (linebreaks). Dit produceert smalle blokken zonder echte paragraaf-structuur en breekt de leesbaarheid in een gepubliceerde PDF. Overweeg om elk level als korte `description`-lijst te schrijven of als doorlopende alinea met komma's.
- [ ] **`proofofconcept.tex` regel 569 `\section{Samenvatting}` — naamconflict met de hoofdstuk-Samenvatting vooraan de paper.**
  > Hernoem naar *"Samenvatting van de PoC"* of *"Tussenconclusie"* om dubbele "Samenvatting" in TOC te vermijden.
- [ ] **`inleiding.tex` regel 45 — sectie-marker bevat nog `% DONE` van vorige iteratie.** Cosmetic, mag weg.
- [ ] **`methodologie.tex` regels 8–27 + 29–31 — Sjabloon-commentblokken en dubbele `Methodologie`-comment header.** Ook: regel 30–31 herhaalt de banner. Mag weggekuist worden.
- [ ] **`inleiding.tex` regel 22–25, 49, 67, 78–80 — Sjabloon `% Uit je probleemstelling moet duidelijk zijn ...`-comments.** Niet schadelijk, maar geven de source-tree een rommelig gevoel; mag weg.
- [ ] **`standvanzaken.tex` regel 209–210 — Leftover comment over OOP-locatie.**
  > `%% Object-georiënteerd programmeren wordt apart behandeld in sectie~\ref{subsec:cobol-oop}` was tijdelijk navigatiecommentaar. De OOP-sectie staat er nu (regel 326), dus deze comment is overbodig.
- [ ] **`bijlagen/bijlage-materialen.tex` ongebruikt** — Plan B3 voegt deze niet meer in. Mag in source blijven (klaar voor evt. opvolgstudie) maar voeg een bovenaan-comment toe dat dit niet in de huidige BP wordt opgenomen.

### Citatie-stijl

- [ ] Mengeling van `tekst.\autocite{X}` (punt vóór cite) en `tekst \autocite{X}.` (punt ná cite) doorheen de paper. Pollefliet-conventie wisselt; kies één en pas overal toe. Voorbeelden van inconsistentie:
  - `standvanzaken.tex:32`: *"...250 miljard regels \autocite{IBM2025}."* (punt ná cite ✓)
  - `standvanzaken.tex:14`: *"...productie zijn. \autocite{IBM2025}"* (punt vóór cite)
  - `standvanzaken.tex:69`: *"...gedefinieerde structuur. \autocite{TutorialsPoint}"* (punt vóór cite)
  - `standvanzaken.tex:91`: *"...4 \textit{Divisions}: \autocite{IBMMainframer2021}"* (cite na dubbele punt)
  > Conform Pollefliet hoort de cite vóór het einde van de zin (dus `tekst \autocite{X}.`). Doorlopend nakijken aan te raden.

---

## 🟢 POLISH / NICE-TO-HAVE

- [ ] **`voorwoord.tex`** — Een persoonlijke reflectie op wat ik zelf heb geleerd door deze BP zou hier nog stevig in passen (1 zin volstaat). Optioneel.
- [ ] **`conclusie.tex`** — Geen reflectie over het persoonlijk leerproces of de onverwachte inzichten; sommige promotoren waarderen dat. Optioneel.
- [ ] **`proofofconcept.tex` §3.5.1 (regel 250–261)** — De `\section{Gebruikersinterface}` heeft géén korte intro vóór de subsecties beginnen. Eén zin "In deze sectie worden de zeven hoofdschermen besproken in volgorde van doorklikken." zou helpen.
- [ ] **`proofofconcept.tex` §3.3.4 Code-editor (regel 229)** — *"Voor het bewerken van COBOL- en referentiecode"*: het woord "referentiecode" is vaag. Bedoel je de Python-referentiekolom? Zo ja, dat is read-only (de gebruiker bewerkt geen Python). Verduidelijk.
- [ ] **`proofofconcept.tex` §3.3.4 (regel 229)** — Voeg eventueel een footnote met URL naar `https://github.com/microsoft/monaco-editor` of `https://www.npmjs.com/package/@monaco-editor/react`.
- [ ] **`proofofconcept.tex` §3.3.5 Vercel** — Geen URL/footnote. Overweeg footnote naar `https://vercel.com/`.
- [ ] **`standvanzaken.tex` §2.2.4 functies (regel 282–315)** — Het Python-voorbeeld gebruikt `add_numbers` met underscore, het COBOL-voorbeeld gebruikt `ADD-NUMBERS` met hyphen (correct), maar de naamgeving is niet consequent uitgelegd: COBOL gebruikt hyphens, Python underscores. Eén zin extra zou dit verschil expliciet maken.
- [ ] **`standvanzaken.tex` §2.2.2 PIC table (regel 144)** — Het Python-equivalent voor `Decimal` toont `price = -123.45` (een float). Bij `S9(5)V99` is `Decimal('-123.45')` correcter (float ≠ exacte decimaal). Detail dat een COBOL-promotor zou kunnen aanwijzen.
- [ ] **`standvanzaken.tex` §2.3.2 PBL (regel 376–377)** — De bullets voor *Points* en *Badges* herhalen "in een gamified proces ...". Compacter zou zijn: één algemene zin + telkens één korte definitie.
- [ ] **`voorstel/voorstel-inhoud.tex` (loaded as bijlage)** — Bevat de oorspronkelijke aanpak met SUS-cijfers en focusgroepen. De disclaimer in `DeVuystSilasBP.tex` regel 173 legt uit dat dit historisch is, dus inhoudelijk OK. Optioneel: kort zelfstandig kadertje toevoegen aan het begin van de bijlage met dezelfde disclaimer voor wie alleen de bijlage leest.
- [ ] **Terminologie** — Op één plek wordt "binnen-subject" gebruikt en op andere "within-subject". Kies één:
  - `methodologie.tex:58`: "binnen-subject vergelijking"
  - `samenvatting.tex:33`: "binnen-subject vergelijking"
  - `evaluatieEnResultaten.tex:30`: "binnen-subject design"
  - `evaluatieEnResultaten.tex:218`: "binnen-subject"
  - `conclusie.tex:31`: "binnen-subject"
  > Allemaal NL-vorm "binnen-subject" → consistent. ✓ (Geen actie nodig, just verified.)
- [ ] **Hyphenation `\hyphenation{...}` in `DeVuystSilasBP.tex`** — Werkt enkel als de exact-vermelde woorden in de tekst voorkomen. Verifieer in een visuele scan van de PDF dat geen vreemde afbrekingen voorkomen die nog niet zijn toegevoegd.

---

## 📋 EINDCHECKLIST VOOR INDIENING

- [ ] Build draait zonder fouten via `make_thesis.bat`.
- [ ] In de gegenereerde PDF: alle `\ref{...}` resolven (geen `??`).
- [ ] Geen blanco pagina's, geen overflow-warnings die in de PDF zichtbaar zijn.
- [ ] Spellings- en grammaticacheck (NL).
- [ ] Pagina-aantal binnen de HOGENT-richtlijnen (typisch 40–60 p. exclusief bijlagen).
- [ ] `git status` schoon: `TODO.md` evt. naar `.gitignore` of mee in repo.
- [ ] PDF in `output/DeVuystSilasBP.pdf` is de definitieve versie die je indient.

---

## Snelle navigatie

```bash
# Alle plekken met "proefpersonen", "gebruikersevaluatie", oude SUS-context
rg -n "proefpersonen|gebruikersevaluatie|gebruikersonderzoek" bachproef/

# Alle TODO-comments in source (zou leeg moeten zijn)
rg -n "TODO" bachproef/*.tex

# Alle \\\\ als witregel-hack
rg -n "\\\\\\\\ ?\\\\\\\\" bachproef/

# Compileren
.\make_thesis.bat
```
