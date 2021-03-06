# Verjaardagscampagne
![](https://mk0exponealcw6ltqqx5.kinstacdn.com/wp-content/uploads/2017/04/automatic-emails-for-birthdays-name-days.png)

In deze tutorial gaan we een verjaardagscampagne aanmaken. Deze campagne
zal dagelijks de contacten selecteren die op die dag jarig zijn. Je hoeft
hiervoor alleen een aantal simpele stappen te volgen:

1. Maak een nieuwe [selectie](./database-selections-introduction) aan en geef
deze een nieuwe [conditie](./database-selections-introduction#regels-en-
condities). Selecteer bij **Type conditie** de optie **Check op datum**.
2. Selecteer het [veld](./database-fields) waar je verjaardagen opslaat om mee
te vergelijken.
3. Als je nu de optie **Ligt na** of **Ligt voor** bekijkt, zie je een
kalender. Onderaan deze kalender kun je ervoor kiezen een variabele datum te
gebruiken. Selecteer deze optie en stel beide in op 0 dagen. Selecteer bij
**Afronden op hele** de optie *dag*. Dit zorgt ervoor dat alle klanten op hun
verjaardag geselecteerd worden. Wil je klanten bijvoorbeeld een week van
tevoren mailen? In dat geval verander je **Ligt na** en **ligt voor** van 0
naar 7 dagen. Selecteer daarna dat alleen de dag en maand gelijk hoeven te
zijn, anders kijken we alleen naar de mensen die vandaag geboren zijn.
4. Sla je selectie op en bereid een mail voor. Stel een dagelijkse mailing
in naar de verjaardagselectie, deze updaten we namelijk automatisch waneer de
mailing wordt verstuurd.

Vanaf nu krijgen je klanten een mailtje op de verjaardag die zij hebben
ingevoerd. Dit kan zowel in de Publisher als Marketing Suite gedaan worden.
