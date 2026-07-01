# Keyboard Mania

# Alphabet Mania(versie 1)

Een 2D ritmegame gebouwd in Unity waarbij letters van rechts naar links over het scherm bewegen. Raak op het juiste moment de bijbehorende toets op je toetsenbord om punten te scoren en je combo op te bouwen.

## Gameplay

- Letters (A t/m Z) spawnen aan de rechterkant van het scherm en bewegen naar links richting de hit-zone.
- Druk de toets in die overeenkomt met de letter zodra deze de hit-zone bereikt.
- Elke hit wordt beoordeeld op timing:

| Judgement | Tijdsvenster |
|---|---|
| **PERFECT** | ≤ 100 ms |
| **GREAT** | ≤ 200 ms |
| **OK** | ≤ 350 ms |
| **MISS** | > 350 ms / verkeerde toets / letter gemist |

- Opeenvolgende hits bouwen een combo op (rechtsonder in beeld). Een MISS reset de combo naar 0.

## Besturing

Alle letters `A`–`Z` op het toetsenbord. Druk de toets die overeenkomt met de letter die de hit-zone bereikt.

## Projectstructuur

```
Assets/
├── Prefabs/
│   └── HitNote.prefab        # Prefab voor een vallende letter-note
├── Scenes/
│   └── SampleScene.unity     # Hoofdscene van de game
├── Scripts/
│   ├── Movement.cs           # Beweegt de letter-note naar links en kent de letter toe
│   ├── Hit.cs                # Verwerkt toetsenbordinput en controleert hits
│   ├── Judgement.cs          # Berekent timing en toont PERFECT/GREAT/OK/MISS
│   ├── ComboCounter.cs       # Houdt de combo bij en toont deze op het scherm
│   └── RespawnNote.cs        # Spawnt periodiek nieuwe notes
└── Settings/                 # URP-instellingen (2D render pipeline)
```

## Technische opzet

- **Engine:** Unity, Universal Render Pipeline (2D)
- **Input:** nieuwe Unity Input System (`InputSystem_Actions`)
- **UI/Tekst:** TextMesh Pro voor letters, combo en judgement-teksten
- **Note-spawning:** `RespawnNote` spawnt automatisch nieuwe notes op een vast interval (`spawnInterval`) op basis van een prefab of bestaande note in de scene.
- **Hit-detectie:** `Hit.cs` luistert naar toetsenbordinput en checkt via `Physics2D.OverlapBoxAll` welke note zich in de hit-zone bevindt.
- **Timing-berekening:** `Judgement.cs` berekent het tijdsverschil op basis van de afstand tot het midden van de hit-zone en de snelheid van de note.

## Vereisten

- Unity Editor (2D URP-project)
- Packages: TextMesh Pro, Input System, Universal RP (allemaal al inbegrepen in dit package)

## Installatie

1. Open een leeg Unity 2D-project (URP template aanbevolen).
2. Importeer `Alphabet-mania.unitypackage` via **Assets → Import Package → Custom Package**.
3. Open `Assets/Scenes/SampleScene.unity`.
4. Druk op Play.

## Mogelijke uitbreidingen

- Score-systeem gebaseerd op judgements (bijv. PERFECT = 100 pt, GREAT = 50 pt)
- Levensysteem / health bar bij te veel missers
- Ondersteuning voor woorden/zinnen in plaats van losse letters
- Custom noteprefabs of moeilijkheidsgraden met variabele snelheid
- Geluidseffecten en achtergrondmuziek gesynchroniseerd met de beat


# keyboard mania(versie 2)

Een 2D ritmegame in Unity waarbij letters van rechts naar links over het scherm bewegen. Druk op de juiste toets op het moment dat de letter de hit-zone bereikt om punten te scoren en je combo op te bouwen.

## Gameplay

- Letters (A-Z) verschijnen rechts in beeld en bewegen naar links richting de hit-zone.
- Druk op de bijbehorende letter op je toetsenbord zodra de note de hit-zone bereikt.
- Timing bepaalt je score: **PERFECT**, **GREAT**, **OK** of **MISS**.
- Elke geslaagde hit verhoogt je combo; een gemiste of foute hit reset hem naar 0.
- Hoe hoger je combo, hoe sneller de volgende notes bewegen.

## Besturing

| Actie | Toets |
|---|---|
| Note raken | A t/m Z (bijbehorende letter) |
| Spel starten | Play-knop op het startscherm |

## Projectstructuur

```
Assets/
├── Prefabs/
│   └── HitNote.prefab          # Prefab voor een note
├── Scenes/
│   └── SampleScene.unity       # Hoofdscene van de game
└── Scripts/
    ├── GameManager.cs          # Startscherm / pauzeert het spel tot op Play gedrukt wordt
    ├── Movement.cs             # Beweegt notes van rechts naar links, kent letters toe
    ├── Hit.cs                  # Verwerkt toetsenbordinput en detecteert hits
    ├── Judgement.cs            # Bepaalt en toont de timing (PERFECT/GREAT/OK/MISS)
    ├── ComboCounter.cs         # Houdt de combo bij en toont deze in de UI
    └── RespawnNote.cs          # Respawnt notes nadat ze geraakt of gemist zijn
```

## Scripts

- **GameManager** – bevriest het spel (`Time.timeScale = 0`) totdat de speler op de Play-knop drukt.
- **Movement** – verplaatst een note naar links, kent er een willekeurige letter aan toe en verhoogt de snelheid naarmate de combo stijgt.
- **Hit** – luistert naar toetsenbordinput (nieuwe Input System) en checkt of er een note in de hit-zone zit die bij de ingedrukte toets past.
- **Judgement** – berekent hoe dicht een hit bij perfecte timing zat en toont dit als tekst boven/onder de note.
- **ComboCounter** – telt opeenvolgende hits en toont dit rechtsonder in de UI (via een Canvas).
- **RespawnNote** – spawnt een nieuwe note zodra de vorige geraakt of gemist is.

## Setup in Unity

1. Open het project in Unity (gebruikt Universal Render Pipeline en TextMesh Pro).
2. Open `Assets/Scenes/SampleScene.unity`.
3. Druk op Play. Er verschijnt eerst een startscherm; klik op **Play** om de game te starten.

### Vereisten

- Unity met **Universal Render Pipeline (URP)**
- **TextMesh Pro** package
- Nieuwe **Input System** package

## Bekende aandachtspunten

- De combo-tekst moet als kind van een **Canvas** staan met een `TextMeshPro - Text (UI)`-component; de losse world-space variant wordt niet betrouwbaar gepositioneerd.
- `Assets/_Recovery/` bevat auto-recovery scenes van Unity en zijn geen onderdeel van de game zelf.

## Auteur

R


# keyboard mania(versie 2)

Een 2D ritmegame in Unity waarbij letters van rechts naar links over het scherm bewegen. Druk op de juiste toets op het moment dat de letter de hit-zone bereikt om punten te scoren en je combo op te bouwen.

## Gameplay

- Letters (A-Z) verschijnen rechts in beeld en bewegen naar links richting de hit-zone.
- Druk op de bijbehorende letter op je toetsenbord zodra de note de hit-zone bereikt.
- Timing bepaalt je score: **PERFECT**, **GREAT**, **OK** of **MISS**.
- Elke geslaagde hit verhoogt je combo; een gemiste of foute hit reset hem naar 0.
- Hoe hoger je combo, hoe sneller de volgende notes bewegen.

## Besturing

| Actie | Toets |
|---|---|
| Note raken | A t/m Z (bijbehorende letter) |
| Spel starten | Play-knop op het startscherm |

## Projectstructuur

```
Assets/
├── Prefabs/
│   └── HitNote.prefab          # Prefab voor een note
├── Scenes/
│   └── SampleScene.unity       # Hoofdscene van de game
└── Scripts/
    ├── GameManager.cs          # Startscherm / pauzeert het spel tot op Play gedrukt wordt
    ├── Movement.cs             # Beweegt notes van rechts naar links, kent letters toe
    ├── Hit.cs                  # Verwerkt toetsenbordinput en detecteert hits
    ├── Judgement.cs            # Bepaalt en toont de timing (PERFECT/GREAT/OK/MISS)
    ├── ComboCounter.cs         # Houdt de combo bij en toont deze in de UI
    └── RespawnNote.cs          # Respawnt notes nadat ze geraakt of gemist zijn
```

## Scripts

- **GameManager** – bevriest het spel (`Time.timeScale = 0`) totdat de speler op de Play-knop drukt.
- **Movement** – verplaatst een note naar links, kent er een willekeurige letter aan toe en verhoogt de snelheid naarmate de combo stijgt.
- **Hit** – luistert naar toetsenbordinput (nieuwe Input System) en checkt of er een note in de hit-zone zit die bij de ingedrukte toets past.
- **Judgement** – berekent hoe dicht een hit bij perfecte timing zat en toont dit als tekst boven/onder de note.
- **ComboCounter** – telt opeenvolgende hits en toont dit rechtsonder in de UI (via een Canvas).
- **RespawnNote** – spawnt een nieuwe note zodra de vorige geraakt of gemist is.

## Setup in Unity

1. Open het project in Unity (gebruikt Universal Render Pipeline en TextMesh Pro).
2. Open `Assets/Scenes/SampleScene.unity`.
3. Druk op Play. Er verschijnt eerst een startscherm; klik op **Play** om de game te starten.

### Vereisten

- Unity met **Universal Render Pipeline (URP)**
- **TextMesh Pro** package
- Nieuwe **Input System** package

## Bekende aandachtspunten

- De combo-tekst moet als kind van een **Canvas** staan met een `TextMeshPro - Text (UI)`-component; de losse world-space variant wordt niet betrouwbaar gepositioneerd.
- `Assets/_Recovery/` bevat auto-recovery scenes van Unity en zijn geen onderdeel van de game zelf.

## Auteur

Arne
