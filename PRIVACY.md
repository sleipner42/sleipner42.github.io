# Integritetspolicy för Skolschema Be On Time

Be On Time drivs av Kristoffer Nordström, personuppgiftsansvarig för appens egen behandling enligt den här policyn. Kontakt: kristoffer.nordstrom@outlook.com. Policyn uppdateras om appens behandling ändras.

## Vilken version gäller policyn?

**Be On Time 3.0.1 — tillgänglig i TestFlight, kommande App Store-version.** Avsnittet [3.0.1 — kommande](#301--kommande) gäller användning av version 3.0.1 i TestFlight och när den blir offentligt tillgänglig i App Store. Senast uppdaterad 13 september 2026.

**Be On Time 3.0.0 — nuvarande distribuerade version.** Avsnittet [3.0.0 — historisk policy för den distribuerade versionen](#300--historisk-policy-för-den-distribuerade-versionen) är den publicerade 3.0.0-policyn (från Build 3). Det beskriver den versionens tidigare PDF-funktion och manuella sparande av klassval och ska inte läsas som en beskrivning av den kommande 3.0.1.

## 3.0.1 — kommande

### Offentliga klasscheman

När du själv väljer en skola och klass kontaktar appen Skola24s centrala webbtjänst (web.skola24.se). Förfrågningar innehåller vald Skola24-värd, skolans och klassens tekniska identifierare samt begärd vecka och uppgifter som behövs för hämtningen. Skola24 tar också emot vanlig anslutningsinformation, såsom IP-adress och appens klientbeteckning. Appen tar emot skolor, klasser, lektionstider och schematexter, exempelvis ämnen, lärare och salar. Ett offentligt schema kan innehålla personuppgifter. Schemat visas i appens arbetsminne och kan även sparas lokalt enligt avsnittet om veckocache nedan. Om du tidigare har valt en klass visar appen en tillgänglig sparad vecka först och försöker sedan hämta aktuella uppgifter från Skola24.

### Sparat klassval

När du väljer en klass sparas skolans värdnamn och tekniska identifierare för skola och klass i en liten fil på enheten. Filen innehåller inte klassens visningsnamn, lektionsinnehåll, lärares namn, Schema-ID, elev-ID, personnummer eller lösenord. Valet finns kvar mellan appstarter tills du ersätter eller tar bort det. Vid nästa start använder appen valet för att öppna klasschemat. Veckoinnehåll kan sparas i en separat lokal cache enligt nedan. Välj Byt skola eller klass för att ersätta valet eller Glöm sparat schema i Inställningar för att ta bort det. Appen visar fel om lagringen eller raderingen inte lyckas. Detta raderar inte uppgifter hos skolan eller Skola24. Filen ligger i appens dokumentområde och är inte undantagen från enhetsbackup. Tidigare säkerhetskopior hanteras separat från appens radering.

### Lokalt sparade offentliga veckoscheman

Från koduppdateringen för build 11 den 13 september 2026 kan appen spara hämtade offentliga klassveckor som JSON i en separat fil i appens dokumentområde på enheten. Cachen innehåller skolans och klassens tekniska val, visningsnamn, vecka och schemauppgifter som lektionstider, ämnen, salar och eventuella lärarnamn. Högst åtta poster och 512 KiB behålls; poster äldre än 21 dagar återanvänds inte och sorteras bort vid senare skrivning. En tillgänglig sparad vecka kan visas utan att invänta nätverket. Den kan vara äldre än skolans senaste uppgifter: appen försöker uppdatera när den används med internetanslutning. Bara tidigare hämtade veckor kan visas utan nätverk. Originalvyn återanvänds tills vidare bara i arbetsminnet. Glöm sparat schema tar bort klassvalet och veckocachen; ett lyckat byte till ett annat schema rensar tidigare klasscache. Cachefilen är inte undantagen från enhetsbackup och tidigare säkerhetskopior hanteras separat. Detta raderar inga uppgifter hos skolan eller Skola24.

### Schema-ID eller elev-ID

Om den valda skolan stöder det kan du ange ett Schema-ID eller elev-ID. ID:t skickas till Skola24 för att hämta det schema du väljer. Från koduppdateringen för build 11 den 13 september 2026 sparas det stödda ID:t, skolans tekniska val och det senast hämtade veckoschemat i en separat fil i appens dokumentområde på enheten. Filen rymmer ett ID-val med en veckobild av schemauppgifterna, högst 256 KiB, inklusive lektionstider, ämnen, salar och eventuella namn i schematexten. ID-valet finns kvar mellan appstarter tills du ersätter det eller väljer Glöm sparat schema i Inställningar. En sparad vecka återanvänds bara om den är högst 21 dagar gammal och motsvarar den aktuella begärda veckan och året. Annars används det sparade ID:t för att hämta rätt vecka, utan att du behöver ange det igen. Utgångna schemauppgifter kan ligga kvar i filen tills den ersätts eller raderas. Cachen kan vara inaktuell; appen försöker uppdatera via Skola24 när den används med nätverk. ID:t används inte i filnamn, cachenycklar, egna loggar eller analys. Filen är inte undantagen från enhetsbackup; appens radering ändrar inte tidigare säkerhetskopior eller uppgifter hos skolan eller Skola24. Ange inte lösenord, BankID-uppgifter eller personnummer i fältet.

### Konton, annonser och bakgrund

Appen har inga egna användarkonton, annonser eller egna analysfunktioner. Den efterfrågar inte lösenord, personnummer eller BankID-uppgifter. Widgetar är inte integrerade i denna version och appen schemalägger inga schemahämtningar när den inte används. Vi använder inte appens uppgifter för reklamprofilering eller automatiserade beslut om dig.

### Ändamål och rättslig grund

Uppgifter används för att visa det schema du väljer, spara ditt val av klass eller stött ID och tillgängliga schemauppgifter på enheten, leverera kompatibla appuppdateringar och besvara supportfrågor. För den personuppgiftsbehandling vi ansvarar för stöder vi oss på vårt berättigade intresse av att tillhandahålla appens funktioner, hålla appen fungerande och ge support. Behandlingen begränsas till dessa ändamål och du kan invända genom att kontakta oss. Att du använder appen ger oss inte rätt att använda uppgifter för andra ändamål. Skolan och Skola24 ansvarar för sin egen behandling enligt sina roller och uppgifter; den här policyn ersätter inte deras information.

### Support och lagringstid

Support och integritetsfrågor hanteras via kristoffer.nordstrom@outlook.com. Om du mejlar tar vi emot din e-postadress och det innehåll du själv väljer att skicka. Meddelanden används för att hantera ärendet och behålls så länge de behövs för det, för uppföljning eller för att uppfylla tillämpliga rättsliga skyldigheter. Skicka inte personnummer, lösenord, BankID-uppgifter eller en elevs privata schema. Dölj personuppgifter i skärmbilder. E-post hanteras genom Microsoft Outlook; Microsoft beskriver sin behandling, geografiska hantering och överföringsskydd i sin integritetsinformation på privacy.microsoft.com. Vi lovar inte att supportmejl enbart behandlas inom Sverige eller EU.

### Appuppdateringar

Från och med version 3.0.1 (build 11) söker appen automatiskt efter tillgängliga appuppdateringar när den öppnas och hämtar vid behov programkod och tillhörande filer från Expos EAS Update-tjänst. För att tjänsten ska kunna välja en kompatibel uppdatering skickas vanlig anslutningsinformation, såsom IP-adress, samt teknisk information om appen och enheten, bland annat operativsystem/plattform, appens Expo-projektidentifierare, uppdateringskanal och runtime-version. Begäran innehåller också en slumpmässig klientidentifierare som lagras på enheten av uppdateringskomponenten, samt kan innehålla tekniska uppdateringsidentifierare och uppgifter om ett tidigare uppdateringsfel. Expo kan behandla sådan information för att leverera uppdateringen och följa dess funktion. Appens uppdateringskod lägger inte till ditt schema, Schema-ID, elev-ID eller sparade klassval i uppdateringsförfrågningarna. Se även Expos integritetsinformation på https://expo.dev/privacy.

### Externa tjänster

Skola24 och skolan kan hantera förfrågningar, schemauppgifter och anslutningsloggar enligt sina egna regler. Be On Time har inte fastställt en särskild lagringstid för Skola24s API- och anslutningsloggar och lovar inte att dessa raderas när du glömmer ett klassval. Kontakta skolan om ett publicerat schema behöver rättas eller tas bort. När du själv öppnar en extern länk hanterar den webbplatsen vanlig webbtrafik enligt sin information. Länkar öppnas inte automatiskt. Be On Time är en fristående app, inte ansluten till eller godkänd av Skola24.

### Dina rättigheter

Du kan kontakta Kristoffer Nordström på kristoffer.nordstrom@outlook.com för att begära information om och tillgång till personuppgifter som vi ansvarar för, rättelse, radering eller begränsning, samt invända mot behandling som grundas på berättigat intresse. Rätt till dataportabilitet gäller när lagens förutsättningar är uppfyllda. Vi kan behöva kontrollera din identitet på ett proportionerligt sätt innan vi lämnar ut uppgifter. För skolans eller Skola24s egna uppgifter hänvisar vi dig till rätt ansvarig part. Du kan klaga till Integritetsskyddsmyndigheten, imy.se, eller din lokala tillsynsmyndighet. Barn och vårdnadshavare kan använda samma kontaktväg; appen ska inte användas för att kringgå skyddade elevscheman.

### Läs mer

- [Skola24s integritetsinformation](https://www.skola24.com/support/policys/integritet/)
- [Microsofts integritetsinformation](https://privacy.microsoft.com/sv-se/privacystatement)
- [Integritetsskyddsmyndigheten](https://www.imy.se/)
- [Support för Be On Time](README.md)

## 3.0.0 — historisk policy för den distribuerade versionen
### Offentliga klasscheman

När du själv väljer en skola och klass kontaktar appen Skola24s centrala webbtjänst (web.skola24.se). Förfrågningar innehåller vald Skola24-värd, skolans och klassens tekniska identifierare samt begärd vecka och uppgifter som behövs för hämtningen. Skola24 tar också emot vanlig anslutningsinformation, såsom IP-adress och appens klientbeteckning. Appen tar emot skolor, klasser, lektionstider och schematexter, exempelvis ämnen, lärare och salar. Schemat hålls i appens arbetsminne. Ett offentligt schema kan innehålla personuppgifter. Appen hämtar inte ett schema automatiskt vid start.

### Kom ihåg klassval

Om du slår på Kom ihåg sparas skolans värdnamn och tekniska identifierare för skola och klass i en liten fil på enheten. Filen innehåller inte klassens visningsnamn, lektionsinnehåll, lärares namn, personnummer eller lösenord. Valet finns kvar mellan appstarter tills du ersätter eller tar bort det. Du väljer själv att återöppna det sparade klasschemat; hela veckoschemat sparas inte för offlinevisning. Stäng av funktionen eller välj Glöm sparat klassval för att ta bort valet och dess tillfälliga skrivfil. Appen visar fel om raderingen inte lyckas. Detta raderar inte uppgifter hos skolan eller Skola24. Filen ligger i appens dokumentområde och är inte undantagen från enhetsbackup. Tidigare säkerhetskopior hanteras separat från appens radering.

### Lokala PDF:er

En vald PDF kopieras tillfälligt till appens cache och behandlas lokalt för textutvinning och förhandsgranskning. Appens PDF-funktion laddar inte upp filen till Be On Time eller Skola24. Den använder inte OCR och sparar inte förhandsgranskningen som ett färdigt schema. Appen försöker radera sin tillfälliga dokumentväljarkopia efter behandlingen och visar en varning om rensningen inte kan bekräftas. Originalfilen raderas inte. Väljer du en fil från iCloud eller en annan filleverantör kan den tjänsten behöva hämta filen till enheten enligt sina egna villkor.

### Konton, annonser och bakgrund

Appen har inga egna användarkonton, annonser eller analysfunktioner. Den efterfrågar inte personnummer, lösenord eller BankID-uppgifter. Widgetar är inte integrerade i denna version och appen gör inga automatiska schemahämtningar i bakgrunden. Vi använder inte appens uppgifter för reklamprofilering eller automatiserade beslut om dig.

### Ändamål och rättslig grund

Uppgifter används för att visa det offentliga schema du väljer, komma ihåg ditt val när du ber om det, förhandsgranska din valda PDF och besvara supportfrågor. För den personuppgiftsbehandling vi ansvarar för stöder vi oss på vårt berättigade intresse av att tillhandahålla dessa användarvalda funktioner och ge support. Behandlingen begränsas till dessa ändamål och du kan invända genom att kontakta oss. Att du använder appen ger oss inte rätt att använda uppgifter för andra ändamål. Skolan och Skola24 ansvarar för sin egen behandling enligt sina roller och uppgifter; den här policyn ersätter inte deras information.

### Support och lagringstid

Support och integritetsfrågor hanteras via kristoffer.nordstrom@outlook.com. Om du mejlar tar vi emot din e-postadress och det innehåll du själv väljer att skicka. Meddelanden används för att hantera ärendet och behålls så länge de behövs för det, för uppföljning eller för att uppfylla tillämpliga rättsliga skyldigheter. Skicka inte personnummer, lösenord, BankID-uppgifter eller en elevs privata schema. Dölj personuppgifter i skärmbilder. E-post hanteras genom Microsoft Outlook; Microsoft beskriver sin behandling, geografiska hantering och överföringsskydd i sin integritetsinformation på privacy.microsoft.com. Vi lovar inte att supportmejl enbart behandlas inom Sverige eller EU.

### Externa tjänster

Skola24 och skolan kan hantera förfrågningar, schemauppgifter och anslutningsloggar enligt sina egna regler. Be On Time har inte fastställt en särskild lagringstid för anonyma API-loggar och lovar inte att dessa raderas när du glömmer ett klassval. Kontakta skolan om ett publicerat schema behöver rättas eller tas bort. När du själv öppnar en extern länk hanterar den webbplatsen vanlig webbtrafik enligt sin information. Länkar öppnas inte automatiskt. Be On Time är en fristående app, inte ansluten till eller godkänd av Skola24.

### Dina rättigheter

Du kan kontakta Kristoffer Nordström på kristoffer.nordstrom@outlook.com för att begära information om och tillgång till personuppgifter som vi ansvarar för, rättelse, radering eller begränsning, samt invända mot behandling som grundas på berättigat intresse. Rätt till dataportabilitet gäller när lagens förutsättningar är uppfyllda. Vi kan behöva kontrollera din identitet på ett proportionerligt sätt innan vi lämnar ut uppgifter. För skolans eller Skola24s egna uppgifter hänvisar vi dig till rätt ansvarig part. Du kan klaga till Integritetsskyddsmyndigheten, imy.se, eller din lokala tillsynsmyndighet. Barn och vårdnadshavare kan använda samma kontaktväg; appen ska inte användas för att kringgå skyddade elevscheman.

### Läs mer

- [Skola24s integritetsinformation](https://www.skola24.com/support/policys/integritet/)
- [Microsofts integritetsinformation](https://privacy.microsoft.com/sv-se/privacystatement)
- [Integritetsskyddsmyndigheten](https://www.imy.se/)
- [Support för Be On Time](README.md)
