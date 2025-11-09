# Min kodplugg till Baofeng DM32UV

## Copyright

© 2019-2025 by SM0RUX Pontus Falk & SM0RGM Stefan Helander

Filerna är tillgängliga under [GPLv3](https://github.com/sm0rux/dm32uv/blob/master/LICENSE).

## Uppdatering av SM0RGM 

På grund av att Pontus SM0RUX av personliga skäl inte har möjlighet att uppdatera kodpluggen så har han och jag kommit överens om att jag övertar och uppdaterar kodpluggen. Kodpluggen är och förblir därmed "SM0RUX kodplugg" men underhållen av mig. Jag har skapat en fork av kodpluggarna och publicerat under mitt eget Github-konto och ändrat kontaktytorna i dessa filer, så kommentarer, ändringar och liknande lägger du som en issue på min Github eller kontaktar mig.

Även om man försöker vara minutiöst noggrann så kan det smyga sig in fel. Kodpluggen innehåller i denna version runt 600 kanaler. Så hittar du något fel eller har andra synpunkter, lägga gärna en issue eller skicka ett mail. 

Nacka november 2025
SM0RGM Stefan Helander

## Syfte

Det här är en konverterad version av Pontus/SM0RUX kodplugg för Anytone AT-D878UV till Baofeng DV32UV. Kodpluggen till Anytone AT-D878UV underhålls och uppdateras av mig (SM0RGM) sedan en tid tillbaka. Eftersom ingen av oss äger en Baofeng DM32UV är vi beroende av synpunkter och rapporter från dig som använder den. 
Huvudsyftet med publiceringen av filerna här på GitHub är att förenkla för mig själv när det gäller uppdateringar. Jag har inget emot att dela med mig av filerna så att andra kan nyttja dem under förutsättning att de som återanvänder mina filer följer licensvillkoren i [GPLv3](https://github.com/sm0rux/dm32uv/blob/master/LICENSE).

Om du vill bidra med något så är du naturligtvis välkommen att göra så antingen genom att skapa en Pull Request (kräver en del kunskap om hur GitHub funkar) eller genom att skapa ett [issue](https://github.com/sm0rgm/dm32uv/issues).

## Vad ingår i filerna?

Alla repeatrar i Sverige som kan köra DMR eller FM är inkluderade (källa: [sk6ba.se](https://sk6ba.se/repeater/karta/)). Även repeatrar som kör exempelvis C4FM och FM finns med. Repeatrarna är indelade distriksvis. Tyvärr finns det så många repeatrar i sjätte och sjunde distrikten att alla inte får plats i scanning-listan (Anytone).

Dessa filer är testade med: 
CPS Version: 1.45
Firmware version: 1.47

### Vad ändras vid konverteringen från Anytone till Baofeng DM32UV?

Vid konverteringen från Anytone till Baofeng DM32UV så finns vissa begränsningar som man behöver ta hänsyn till.

* RXGroupList i DM32UV är begränsad till 32 talgrupper så vi har valt de vanligaste i DM32UV-versionen.
* Scan-listor i DM32UV är begränsade till 16 kanaler per lista. Därför går det inte att konvertera scanlistorna från Anytone. Därför har jag skapat en enda scanlista med namnet Default. Lämpligen skapar du dina egna scanlistor för dina behov.

### Vilka filer ska du hämta?

Jag rekommenderar att du hämtar filerna som jag har packat ihop i en [release](https://github.com/sm0rgm/dm32uv/releases) istället för att hämta mina arbetsfiler!

### När filerna är hämtade... 

CSV-filerna kan du använda om du har en befintlig radio eller kodplugg som du vill uppdatera med kanaler, zoner, talgrupper etc. 

Om du snabbt och enkelt vill starta en ny kodplugg eller koda upp en ny radio så finns det en färdig fil med alla inställningar gjorda som heter N0CALL.g77.

Starta CPS-programmet och välj File -> Open och välj N0CALL.data. Gå till fliken DMR ID and callsign och ändra Callsign och DMR ID till och dina egna. 

Förmodligen vill du ändra på fler saker, men det överlåter jag till dig att fixa med själv.


### Uppdatera befintlig kodplugg

Om du bara vill uppdatera din radio med kanaler, zoner och talgrupper men låta resterande inställning vara som de är kan du, istället öppna din befintliga kodplugg i CPS och sedan gå till respektive sektion och klicka på knappen Import. Välj den CSV-fil som har samma namn som den sektion du vill importera till (Channel, Zone, Scan mm).

## Suffix i repeaternamn

För att indikera typ av repeater eller vilket nätverk den är ansluten mot finns numera en eller flera bokstäver som suffix till repeaterns namn. Om repeatern är ansluten till Brandmeister för DMR eller är en lokal FM-repeater utan anslutning till reflektornätverk finns ingen bokstav angiven. Bokstäverna betyder:

L = Link (simplex)
A = AllstarLink
S = SVXlink
E = EchoLink
H = Hotspot (DMR)
F = FreeDMR / FinDMR
+ = DMR+ / DMR Plus
I = IRLP / ircDDB
P = HAMphone

### Tack

Stort tack till SA0BMC Johan Lars för tips, råd och inte minst för lån av en radio så att jag kunde testa kodpluggen!

## SM0RUX/Pontus silent key

Den 9 mars 2025 gick SM0RUX/Pontus silent key efter några års kamp mot cancern. Kodpluggen är och förblir "SM0RUX kodplugg" men underhålls fortsatt av mig, SM0RGM/Stefan. Kodpluggen är gratis att använda men vill du ge ett bidrag så tänk gärna på Cancerfonden tel. 010-199 10 10.

73's de SM0RGM Stefan

2025-11-09
