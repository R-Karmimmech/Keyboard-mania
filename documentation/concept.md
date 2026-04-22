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

## Doelgroep
- Spelers die van rhythm games houden
- Spelers die uitdaging zoeken in timing en precisie
- Spelers die graag eigen content of spelregels willen maken

## Core Gameplay Loop
1. De speler kiest een map of nummer.
2. De speler heeft de mogelijkheid om aanpassing(en) te kiezen om de map lastiger of makkelijker te maken.
3. De game start een liedje en toont inkomende noten op het scherm.
4. De speler drukt toetsen in op het juiste ritme.
5. Goede timing levert punten, combo's en behoud van HP op.
6. Fouten kosten HP of verbreken de combo.
7. Aan het einde van het nummer krijgt de speler een score en resultaat.

## Belangrijkste Mechanics

### 1. Normale noten
De speler moet een specifieke toets indrukken op het juiste moment.

### 2. Meerdere toetsen tegelijk
Sommige patronen vereisen dat meerdere toetsen gelijktijdig worden ingedrukt.

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
- Heldere lanes of inputzones
- Duidelijke timing feedback
- Goed zichtbare HP- en score-indicatoren
- Visuele waarschuwingen voor bomtoetsen en hold notes

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
Keyboard Rhythm Game is een ritmegame waarin timing, precisie en patroonherkenning centraal staan. De basis van de game draait om het correct indrukken van toetsen op het ritme van muziek, terwijl extra mechanics zoals hold notes, gelijktijdige inputs en bomtoetsen voor variatie en uitdaging zorgen.
