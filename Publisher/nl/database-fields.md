# Databasevelden
De structuur van een databases bestaat uit velden, interesses en collecties.
In velden en interessevelden kan bijvoorbeeld een tekst, datum of getal
worden opgeslagen. In het geval van interesses wordt hier alleen "ja" of "nee"
als waarde geaccepteerd. Door een collectie aan een database toe te voegen
creëer je een extra laag in de database. Een collectie bestaat ook weer uit
enkelvoudige velden.

## Veldtypes
Er zijn verschillende veldtypes beschikbaar voor het opslaan van specifieke
gegevens, bijvoorbeeld voor tekst, getallen en datums.
Hieronder is een tabel weergegeven met alle beschikbare veldtypes.

| Veldtype           | Omschrijving                                                                                         |
|--------------------|------------------------------------------------------------------------------------------------------|
| Tekstveld          | Letters [A-Z], numerieke waardes [0-9] en/of underscores. Maximaal aantal karakters is 255.          |
| Numeriek veld      | Alleen numerieke waardes [0-9]. Kan geen leeg veld zijn. Geef bijvoorbeeld standaardwaarde 0 op.     |
| E-mail veld        | E-mailveld is een tekstveld, bedoeld voor het opslaan van e-mailadressen.                            |
| Telefoonveld       | Kan worden gespecificeerd voor fax, mobiele en andere telefoonnummers.                               |
| Datumveld          | Het datumveld bevat de datum (yyyy-mm-dd)                                                            |
| Datum + tijdveld   | Het datumveld bevat de datum (yyyy-mm-dd) en het tijdveld bevat de uren, minuten en seconden.        |
| Landcode veld      | Accepteert landcodes volgens de ISO 3166 standaard. NL, BE etc.                                      |
| Meerkeuzeveld      | Kan worden gebruikt om meerdere opties te tonen, optie gevolgd door een * is de standaardwaarde.     |
| Groot veld         | Tekstveld tot 16 mln. tekens. Wordt niet aangeraden, omdat je het niet kunt indexeren.               |
| Referentieveld     | Veld dat kan refereren naar een andere database door middel van een ID.                              |

## Extra veldopties
Als je velden aan het bewerken bent, kun je per veld een aantal extra opties
selecteren. Het is bijvoorbeeld mogelijk om aan te geven dat een veld standaard
gesorteerd is, of dat het verborgen moet blijven. Hieronder een korte uitleg
van al deze opties.

### Verborgen velden
Verborgen velden zijn niet zichtbaar in het dialoogvenster om een profiel te
bewerken. Gebruik deze optie voor velden die je niet meer wilt tonen of wilt
kunnen bewerken via de interface. De gegevens uit een verborgen veld kunnen wel
gewoon geïmporteerd en geëxporteerd worden, zoals alle andere velden.

### Veld tonen op overzichtspagina's
In een database staan vaak veel meer velden dan dat je wilt laten zien in een
profielenlijst. Deze optie stelt je in staat om zelf te bepalen wat de
belangrijke velden zijn, de andere velden worden in deze lijsten verborgen.

### Gesorteerde velden
Met deze optie kun je invoeren op welk veld een overzicht met profielen
standaard wordt gesorteerd. Deze optie kan slechts bij één veld tegelijkertijd
actief zijn.

### Geïndexeerde velden
Het indexeren van velden kan het zoeken van profielen en het maken van
selecties versnellen. Het is dus verstandig om velden die je vaak opzoekt in
selecties te indexeren. Je kan maximaal 64 velden indexeren, maar het is ook
niet nodig er veel te indexeren. Velden van het type "Groot veld" kunnen niet
worden geïndexeerd.

## Interesses
Interesses zijn velden die aan- of uitgezet kunnen worden. Een profiel kan
meerdere interesses hebben per groep. Denk hierbij bijvoorbeeld aan een groep
'Inschrijvingen' met drie interesses: Nieuwsbrief (op 'ja'), Aanbiedingen
(op 'nee') en Facturen (op 'ja'). Interesses kunnen aangemaakt worden in het
databaseveldenmenu door op 'interesse toevoegen' te klikken.

## Databasevelden aanpassen of aanmaken
Om de structuur van je databasevelden aan te passen klik je **Velden & interesses** binnen de gekozen database. 
Er zal een lijst worden getoond met alle velden uit de database, klik op
**bewerken** achter een veld om dit veld aan te passen. Klik op
**veld aanmaken** om een nieuw veld aan te maken. Er zal aan de rechterkant
een venster verschijnen waar het veld aangepast of aangemaakt kan
worden. Geef het veld een naam, één van de bovengenoemde types en zet eventueel
extra opties aan.

## Databaserestricties instellen

Databaserestricties zijn regels die je kunt toevoegen aan een database
of collectie. Wijzigingen en toevoegingen aan een database moeten dan
aan de vooropgestelde regels voldoen om te worden doorgevoerd.
Je kunt bijvoorbeeld de minimumleeftijd instellen of zorgen dat de
gebruikersnaam altijd uniek is. Er bestaat daarnaast een optie
"dubbele veldwaarden blokkeren" waarmee je vervuiling van de database
tegengaat.

**Let op:** deze restricties worden alleen toegepast op nieuwe profielen en
wijzigingen aan bestaande profielen. Om bestaande foutieve profielen te
verwijderen, zal je voor deze een selectie moeten aanmaken met dezelfde
voorwaarden als de databaserestricties en deze profielen te verwijderen met de
functionaliteit onder **Configuratie > Profielen verwijderen**.
