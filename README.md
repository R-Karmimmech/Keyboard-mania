# Keyboard Mania


#keyboard mania(versie 2)

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
