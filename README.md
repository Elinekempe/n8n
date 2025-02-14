# n8n
n8n deepdive


Wat is deze workflow?

Deze n8n workflow automatiseert het proces waarbij een Discord bot een lijst ophaalt van alle leden in een server met een specifieke rol. Vervolgens kan de bot een nieuwe rol toekennen en een melding sturen naar de gebruiker.


Hoe installeer je het?

Installeer n8n als je dat nog niet hebt:
npm install -g n8n
Start n8n:
n8n start
Importeer de workflow:
Download het workflow JSON-bestand.
Ga naar n8n en klik op Menu → Import workflow.


Hoe stel je het in?

Maak een Discord bot aan:
Ga naar Discord Developer Portal.
Maak een nieuwe bot.
Kopieer de Bot Token.
Zorg ervoor dat de bot de juiste permissies heeft (zoals "Rollen beheren" en "Berichten sturen").

Hoe werkt het?

Trigger → De workflow wordt gestart via een geplande trigger die elke minuut draait.
Gebruikers ophalen → De bot haalt de lijst op van alle gebruikers met een specifieke rol in de server.
Rol toewijzen → De bot voegt een extra rol toe aan deze gebruikers.
Bevestigingsbericht sturen → De bot stuurt een melding naar een kanaal of de gebruiker met een bericht zoals:
🎉 Gefeliciteerd! Je hebt de rol "Oreo" gekregen.


Hoe ziet de workflow eruit?

Schedule Trigger → Start automatisch elke minuut.
Get Members (Discord node) → Haalt de lijst op van leden met een specifieke rol.
Check if we have an ID (IF-node) → Controleert of een ID aanwezig is.
Add Roles (Discord node) → Voegt een nieuwe rol toe aan de gebruiker.
Send Notification (Discord node) → Stuurt een bericht naar een kanaal met een bevestiging.
Merge en afsluiten → Combineert gegevens en beëindigt de workflow.

Handige tips
Zorg ervoor dat de bot boven de rollen staat die hij moet toewijzen in de Discord rolhiërarchie.
Voeg een error-handling node toe om foutmeldingen te loggen als de rol niet kan worden toegewezen.
Pas de workflow aan als je een andere rol-ID of een ander kanaal wilt gebruiken.
Gebruik een Google Spreadsheet om gebruikerslogboeken op te slaan (zie de Google Sheets URL in de workflow).
