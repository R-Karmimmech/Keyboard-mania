# Game Design Document

## Titel
**Keyboard Rhythm Game**

## High Concept
Keyboard Rhythm Game is een ritmegame waarin de speler toetsen op het toetsenbord indrukt op het juiste moment, synchroon met de muziek. Het doel is om notenreeksen correct uit te voeren, combo's op te bouwen en een level uit te spelen zonder alle HP te verliezen.

## Genre
- Rhythm game
- Skill-based
- Mogelijk uitbreidbaar met multiplayer en custom content

## Doel van de game
De speler moet reageren op visuele prompts die gekoppeld zijn aan muziek. Door op tijd de juiste toetsen in te drukken, scoort de speler punten en blijft de HP-balk gevuld. Fouten, gemiste noten of het raken van verboden toetsen zorgen voor straf.

## Hoe het spelen eruitziet
De speler start op een selectiescherm en kiest daar een nummer of map. Daarna verschijnt een speelscherm dat qua opzet lijkt op de lane-logica van `osu!taiko`: er is een duidelijke hoofdlane waarin alle noten van rechts naar links, of richting een vast hitpunt, bewegen. De speler hoeft dus niet meerdere banen tegelijk te volgen, maar focust op een centrale stroom van noten die op een vast moment geraakt moeten worden.

Het verschil met `osu!taiko` is dat de game niet werkt met kleurcodes of vrije toetskeuze. In plaats daarvan staat op iedere noot duidelijk aangegeven welke toets de speler moet indrukken. Als er bijvoorbeeld een noot met de letter `F` aankomt, moet de speler precies op het hitmoment de `F`-toets indrukken. Daardoor leest de speler niet alleen het ritme, maar ook direct welke input verwacht wordt.

Om gelijktijdige input duidelijk te maken, kunnen twee noten met een zichtbare streep aan elkaar verbonden zijn. Die verbinding laat zien dat beide toetsen exact tegelijk moeten worden ingedrukt zodra het gekoppelde nootpaar het hitpunt bereikt. Zo kan de speler in een oogopslag herkennen of het om een enkele input gaat of om een gecombineerde aanslag.

Niet alle noten werken hetzelfde. Normale noten vragen om een enkele toetsaanslag. Gekoppelde noten vragen om twee toetsen tegelijk. Hold notes verschijnen als langere vormen of balken in dezelfde lane: de speler drukt de juiste toets in zodra de noot het hitpunt bereikt en houdt die vast tot het einde van de vorm. Bomtoetsen zijn juist gevaren; die zien er afwijkend uit en moeten vermeden worden, omdat een verkeerde input hier HP kost.

Onderaan of aan de zijkant van het scherm blijft steeds belangrijke informatie zichtbaar, zoals HP, score en combo. Daardoor kan de speler in een oogopslag zien hoe goed de run verloopt. Als de speler veel fouten maakt, daalt de HP-balk. Raakt die leeg, dan mislukt het level direct. Blijft de speler overeind tot het einde van het nummer, dan volgt een resultaatscherm met de eindscore en een samenvatting van de prestatie.

## Doelgroep
- Spelers die van rhythm games houden
- Spelers die uitdaging zoeken in timing en precisie
- Spelers die graag eigen content of spelregels willen maken

## Core Gameplay Loop
1. De speler kiest een map of nummer.
2. De speler heeft de mogelijkheid om aanpassing(en) te kiezen om de map lastiger of makkelijker te maken.
3. De game start een liedje en toont inkomende noten in een centrale lane met een vast hitpunt.
4. De speler leest per noot welke toets gevraagd wordt en drukt die toets op het juiste moment in wanneer de noot het hitpunt bereikt.
5. Goede timing levert punten, combo's en behoud van HP op, terwijl directe feedback toont hoe goed de input was.
6. Fouten, gemiste noten, verkeerde toetsen of het raken van bomtoetsen kosten HP en kunnen de combo verbreken.
7. Aan het einde van het nummer krijgt de speler een score en resultaat.

## Belangrijkste Mechanics

### 1. Normale noten
De speler moet de toets indrukken die op de noot zelf staat aangegeven, precies op het juiste moment.

### 2. Meerdere toetsen tegelijk
Sommige noten zijn met een streep aan elkaar verbonden. Dat betekent dat beide weergegeven toetsen gelijktijdig moeten worden ingedrukt.

### 3. Hold notes
Bepaalde toetsen moeten voor een bepaalde tijd worden ingedrukt gehouden.

### 4. Bomtoetsen
Sommige toetsen zijn valstrikken. Als de speler deze indrukt, verliest die HP.

### 5. HP-systeem
De speler heeft een percentage-gebaseerde HP-balk. Fouten verlagen HP, correcte inputs houden HP stabiel of kunnen deze beperkt herstellen.

### 6. Score en combo
Correcte inputs verhogen de score. Opeenvolgende correcte inputs bouwen een combo op, wat extra punten kan opleveren.

## Progressie en Content

### Maps
- Vooraf gemaakte maps
- Zelfgemaakte maps
- Mogelijk automatisch gegenereerde maps op basis van BPM

### Spelregels
- Standaard spelregels per map
- Aanpasbare modifiers die de moeilijkheid of speelstijl veranderen
- Mogelijkheid om zelf nieuwe regels of varianten toe te voegen

### Multiplayer
Als uitbreiding kan multiplayer worden toegevoegd, bijvoorbeeld:
- Versus mode op score
- Co-op mode op timing en overleving

## Visuele Richting
De game moet duidelijk leesbaar zijn tijdens snelle gameplay. De focus ligt op:
- Een duidelijke centrale lane met vast hitpunt
- Toetslabels op noten zodat direct zichtbaar is welke input nodig is
- Geen kleurlogica zoals in `osu!taiko`, zodat de leesbaarheid en instapbaarheid hoger blijven
- Duidelijke timing feedback
- Goed zichtbare HP- en score-indicatoren
- Visuele waarschuwingen voor bomtoetsen, hold notes en gekoppelde noten

## Audio
Audio is de kern van de ervaring. Daarom moet de game:
- Muziek strak synchroniseren met inputmomenten
- Directe feedback geven bij correcte en foute inputs
- Verschillende nummers en BPM-structuren ondersteunen

## Technische Richting
De game kan goed opgebouwd worden met een objectgeorienteerde structuur. Denk aan:
- `Game`: beheert de algemene game state
- `Song`: bevat muziekinformatie en BPM
- `Map`: bevat nootdata en timing
- `Note`: basisobject voor een noot
- `HoldNote`: speciale noot die langer actief blijft
- `BombNote`: noot die schade veroorzaakt bij input
- `Player`: houdt score, combo en HP bij
- `RuleSet`: bepaalt actieve spelregels en modifiers

## Must Have
- Een speelbare rhythm game met toetsenbordinput
- Noten die op timing gespeeld kunnen worden
- Score- en combosysteem
- HP-systeem op basis van fouten
- Ondersteuning voor normale noten
- Ondersteuning voor meerdere toetsen tegelijk
- Ondersteuning voor hold notes
- Ondersteuning voor bomtoetsen
- Minimaal een kleine set speelbare maps of nummers

## Nice to Have
- Custom map editor
- BPM-gebaseerde mapgeneratie
- Aanpasbare spelregels
- Multiplayer
- Extra moeilijkheidsgraden
- Online scorebord

## Samenvatting
Keyboard Rhythm Game is een ritmegame waarin timing, precisie en patroonherkenning centraal staan. De presentatie gebruikt een `osu!taiko`-achtige lane-opzet, maar vervangt kleurcodes door expliciete toetsen op de noten zelf. Daardoor moet de speler niet alleen het ritme volgen, maar ook exact de toetsen indrukken die verschijnen. Extra mechanics zoals gekoppelde noten, hold notes en bomtoetsen zorgen voor variatie en uitdaging.
