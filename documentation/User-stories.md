# User Stories - Keyboard Rhythm Game

Dit document vertaalt de inhoud van `concept.md` naar concrete user stories. De stories zijn opgesplitst in `Must have` voor de eerste speelbare versie en `Nice to have` voor uitbreidingen.

## Must Have

### US-01 - Map of nummer kiezen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik voor de start een map of nummer kunnen kiezen, zodat ik bewust een level kan starten dat ik wil spelen.

**Acceptatiecriteria**
- De speler kan vanuit een startscherm minimaal een kleine set speelbare maps of nummers zien.
- Een selectie kan direct gestart worden zonder handmatige aanpassingen buiten de game.
- De gekozen map bepaalt welke noten, timing en muziek tijdens het level worden geladen.

### US-02 - Inkomende noten kunnen lezen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik inkomende noten duidelijk op het scherm zien aankomen, zodat ik mijn input op tijd kan voorbereiden.

**Acceptatiecriteria**
- Noten bewegen of verschijnen op een consistente manier richting een duidelijk hitmoment.
- Het is zichtbaar welke toets of inputzone bij een noot hoort.
- De interface blijft leesbaar tijdens snelle patronen.

### US-03 - Normale noten op timing spelen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik een normale noot kunnen raken door de juiste toets op het juiste moment in te drukken, zodat skill en timing centraal staan.

**Acceptatiecriteria**
- Elke normale noot is gekoppeld aan een specifieke toets.
- Input wordt beoordeeld op basis van timing ten opzichte van het hitmoment.
- Correcte input telt als hit en foute of gemiste input telt als fout.

### US-04 - Muziek en gameplay synchroon ervaren
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik dat muziek, noten en inputmomenten synchroon lopen, zodat het ritme eerlijk en speelbaar aanvoelt.

**Acceptatiecriteria**
- Noten verschijnen op basis van de timing van de gekozen map.
- Het hitmoment van noten sluit aan op de muziek.
- De speler kan op gehoor en zicht reageren zonder dat de timing structureel verkeerd aanvoelt.

### US-05 - Meerdere toetsen tegelijk indrukken
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik patronen met meerdere gelijktijdige toetsen kunnen spelen, zodat de gameplay gevarieerd en uitdagend wordt.

**Acceptatiecriteria**
- Een map kan noten bevatten die tegelijk geraakt moeten worden.
- De game controleert of alle vereiste toetsen binnen hetzelfde timingvenster zijn ingedrukt.
- Een onvolledige of foute gelijktijdige input wordt als fout geregistreerd.

### US-06 - Hold notes vasthouden
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik hold notes kunnen indrukken en vasthouden, zodat langere acties onderdeel worden van het ritme.

**Acceptatiecriteria**
- Een hold note heeft een startmoment en een duur.
- De speler moet de juiste toets op het startmoment indrukken en vasthouden.
- Te vroeg loslaten of niet correct starten telt als fout of gemiste actie.

### US-07 - Bomtoetsen vermijden
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik bomtoetsen kunnen herkennen en vermijden, zodat valstrikken extra spanning toevoegen aan de gameplay.

**Acceptatiecriteria**
- Bomtoetsen zijn visueel te onderscheiden van normale noten.
- Het indrukken van een bomtoets veroorzaakt straf.
- De straf heeft minimaal effect op HP en mag ook andere negatieve gevolgen hebben, zoals het verbreken van een combo.

### US-08 - Directe timingfeedback ontvangen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik direct feedback krijgen op mijn input, zodat ik tijdens het spelen begrijp of mijn timing goed of fout was.

**Acceptatiecriteria**
- Na een hit of fout krijgt de speler direct visuele feedback.
- Feedback maakt duidelijk of een input correct, fout of gemist was.
- De feedback belemmert de leesbaarheid van volgende noten niet.

### US-09 - Score opbouwen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik punten verdienen voor correcte inputs, zodat mijn prestatie meetbaar en motiverend is.

**Acceptatiecriteria**
- Correcte inputs verhogen de score.
- Fouten leveren geen positieve score op.
- De actuele score is zichtbaar tijdens of direct na het level.

### US-10 - Combo opbouwen en verliezen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik een combo kunnen opbouwen met opeenvolgende correcte inputs, zodat consistent goed spelen extra wordt beloond.

**Acceptatiecriteria**
- Een reeks correcte inputs verhoogt de combo.
- Een fout, gemiste noot of verkeerde input verbreekt de combo.
- De actuele combo is zichtbaar tijdens het spelen.

### US-11 - HP beheren tijdens een run
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik een zichtbare HP-balk hebben die reageert op mijn prestaties, zodat duidelijk is of ik het level overleef.

**Acceptatiecriteria**
- De speler heeft een percentage-gebaseerde HP-balk.
- Fouten, misses of bominputs verlagen de HP.
- Correcte inputs houden HP stabiel of herstellen deze beperkt.

### US-12 - Een level kunnen falen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik een run kunnen verliezen als mijn HP opraakt, zodat fouten echte consequenties hebben.

**Acceptatiecriteria**
- Wanneer HP tot nul daalt, eindigt het level voortijdig of telt de run als mislukt.
- De speler krijgt duidelijke feedback dat het level is gefaald.
- De game blijft stabiel functioneren wanneer een level vroegtijdig stopt.

### US-13 - Een level kunnen uitspelen
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik een nummer succesvol kunnen afronden als ik genoeg noten raak en HP behoud, zodat ik voortgang en voldoening ervaar.

**Acceptatiecriteria**
- Een run eindigt succesvol wanneer het nummer volledig is afgespeeld en de speler niet is uitgevallen.
- De game stopt of sluit de gameplay correct af aan het einde van het nummer.
- De overgang van gameplay naar resultaat verloopt zonder onduidelijke tussenstap.

### US-14 - Resultaat en samenvatting bekijken
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik na afloop een resultaat zien met mijn prestatie, zodat ik kan beoordelen hoe goed ik het heb gedaan.

**Acceptatiecriteria**
- Na elke run krijgt de speler een resultaat- of eindscherm.
- Het resultaat toont minimaal score en of het level gehaald of gefaald is.
- Het scherm sluit logisch aan op de gespeelde run.

### US-15 - Meerdere speelbare maps beschikbaar hebben
**Actor:** Speler  
**Prioriteit:** Must have  
**User story:** Als speler wil ik meerdere maps of nummers kunnen spelen, zodat de game meer biedt dan een enkele demo.

**Acceptatiecriteria**
- De game bevat minimaal een kleine set speelbare maps of nummers.
- Maps kunnen verschillen in patroon, tempo of uitdaging.
- De speler kan opnieuw kiezen tussen beschikbare content na een run.

## Nice To Have

### US-16 - Zelfgemaakte maps spelen
**Actor:** Contentmaker  
**Prioriteit:** Nice to have  
**User story:** Als contentmaker wil ik zelfgemaakte maps kunnen toevoegen en spelen, zodat de game uitbreidbaar wordt met eigen content.

**Acceptatiecriteria**
- Het systeem ondersteunt naast vooraf gemaakte maps ook custom maps.
- Een custom map kan noten- en timingdata bevatten die door de game gelezen wordt.
- Een toegevoegde map is selecteerbaar vanuit dezelfde flow als andere content.

### US-17 - Custom map editor gebruiken
**Actor:** Contentmaker  
**Prioriteit:** Nice to have  
**User story:** Als contentmaker wil ik een editor gebruiken om zelf maps te maken, zodat ik zonder handmatig programmeerwerk nieuwe levels kan bouwen.

**Acceptatiecriteria**
- Een gebruiker kan nootdata aanmaken of aanpassen via een editorworkflow.
- De gemaakte map kan opgeslagen en later gespeeld worden.
- De editor ondersteunt minimaal de kernnoottypes van de game.

### US-18 - Automatische mapgeneratie op basis van BPM
**Actor:** Speler / Contentmaker  
**Prioriteit:** Nice to have  
**User story:** Als speler of contentmaker wil ik automatisch maps kunnen genereren op basis van BPM, zodat nieuwe content sneller beschikbaar komt.

**Acceptatiecriteria**
- Het systeem kan op basis van BPM of muziekinformatie een basispatroon genereren.
- Een gegenereerde map is speelbaar binnen dezelfde gameplayregels als andere maps.
- De gegenereerde output is een startpunt dat eventueel later aangepast kan worden.

### US-19 - Modifiers of spelregels kiezen
**Actor:** Speler  
**Prioriteit:** Nice to have  
**User story:** Als speler wil ik voor de start modifiers of aangepaste spelregels kunnen kiezen, zodat ik de moeilijkheid en speelstijl kan aanpassen.

**Acceptatiecriteria**
- De speler kan voor de start een set actieve modifiers of regels selecteren.
- De gekozen regels hebben aantoonbaar invloed op de gameplay van de run.
- Het is duidelijk welke regels actief zijn voordat het level start.

### US-20 - Nieuwe rule sets of varianten toevoegen
**Actor:** Contentmaker / Ontwikkelaar  
**Prioriteit:** Nice to have  
**User story:** Als maker wil ik nieuwe spelvarianten of rule sets kunnen toevoegen, zodat de game flexibel uitbreidbaar blijft.

**Acceptatiecriteria**
- Het systeem ondersteunt een structuur waarin spelregels los van een map beheerd kunnen worden.
- Een nieuwe rule set kan zonder volledige herbouw van de basisgame worden toegevoegd.
- Maps kunnen gekoppeld worden aan standaardregels of alternatieve regels.

### US-21 - Extra moeilijkheidsgraden spelen
**Actor:** Speler  
**Prioriteit:** Nice to have  
**User story:** Als speler wil ik een nummer in meerdere moeilijkheidsgraden kunnen spelen, zodat beginners en gevorderden dezelfde content op hun niveau kunnen gebruiken.

**Acceptatiecriteria**
- Een nummer kan meerdere varianten of moeilijkheidsinstellingen hebben.
- De speler kan een moeilijkheid kiezen voordat de run start.
- Hogere moeilijkheden leveren zichtbaar complexere patronen of strengere uitdaging op.

### US-22 - Tegen andere spelers strijden in versus
**Actor:** Competitieve speler  
**Prioriteit:** Nice to have  
**User story:** Als competitieve speler wil ik een versusmodus spelen op basis van score, zodat ik mijn timing direct met anderen kan vergelijken.

**Acceptatiecriteria**
- Een versusmodus vergelijkt de prestaties van twee of meer spelers op dezelfde content.
- De winnaar wordt bepaald op basis van een duidelijk resultaat, zoals score.
- De modus gebruikt dezelfde kernmechanieken als de singleplayergame.

### US-23 - Samen overleven in co-op
**Actor:** Co-op speler  
**Prioriteit:** Nice to have  
**User story:** Als co-op speler wil ik samen met een andere speler een nummer kunnen voltooien, zodat samenwerking onderdeel wordt van de uitdaging.

**Acceptatiecriteria**
- Een co-opmodus laat meerdere spelers deelnemen aan dezelfde run.
- Timing en overleving zijn gezamenlijke of onderling afhankelijke factoren in het resultaat.
- De modus maakt duidelijk of het team het nummer heeft gehaald of niet.

### US-24 - Mijn score online vergelijken
**Actor:** Competitieve speler  
**Prioriteit:** Nice to have  
**User story:** Als competitieve speler wil ik een online scorebord kunnen bekijken, zodat ik mijn prestaties kan vergelijken met die van anderen.

**Acceptatiecriteria**
- Scores kunnen per map of nummer worden opgeslagen en weergegeven.
- De speler kan zien hoe een score zich verhoudt tot andere spelers.
- Het scorebord is gekoppeld aan echte gespeelde resultaten.

## Opmerking over scope

Voor een eerste versie ligt de focus op de `Must have` stories. Daarmee ontstaat een complete basisloop: map kiezen, noten spelen, score en HP beheren, en een resultaat ontvangen. De `Nice to have` stories zijn logisch als tweede fase zodra de kern stabiel en speelbaar is.
