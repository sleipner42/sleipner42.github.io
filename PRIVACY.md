# Integritetspolicy för Skolschema Be On Time

Be On Time drivs av Kristoffer Nordström, personuppgiftsansvarig för appens egen behandling enligt den här policyn. Kontakt: kristoffer.nordstrom@outlook.com. Policyn uppdateras om appens behandling ändras.

## Vilken version gäller policyn?

**Be On Time 3.0.6 finns på App Store för iPhone och iPad samt på Google Play för Android.** Policyn omfattar även kompatibla koduppdateringar och widgetstödet i iOS-testversion 3.0.7. Widgetstödet ingår inte i 3.0.6. Frivillig användningsstatistik med slumpmässigt nummer finns på iOS från den 19 oktober 2026 och är avstängd tills du väljer "Ja, dela". På Android används inte detta nummer. Senast uppdaterad 14 november 2026.

**Be On Time 3.0.0 — historisk version.** Avsnittet om 3.0.0 nedan beskriver den äldre PDF-funktionen och ska inte läsas som en beskrivning av den nuvarande versionen.

## 3.0.6 på iOS och Android samt 3.0.7 på iOS

### Offentliga klasscheman

När du själv väljer en skola och klass kontaktar appen Skola24s centrala webbtjänst (web.skola24.se). Förfrågningar innehåller vald Skola24-värd, skolans och klassens tekniska identifierare samt begärd vecka och uppgifter som behövs för hämtningen. Skola24 tar också emot vanlig anslutningsinformation, såsom IP-adress och appens klientbeteckning. Appen tar emot skolor, klasser, lektionstider och schematexter, exempelvis ämnen, lärare och salar. Ett offentligt schema kan innehålla personuppgifter. Schemat visas i appens arbetsminne och kan även sparas lokalt enligt avsnittet om veckocache nedan. Om du tidigare har valt en klass visar appen en tillgänglig sparad vecka först och försöker sedan hämta aktuella uppgifter från Skola24.

### Sparat klassval

När du väljer en klass sparas skolans värdnamn och tekniska identifierare för skola och klass i en liten fil på enheten. Filen innehåller inte klassens visningsnamn, lektionsinnehåll, lärares namn, Schema-ID, elev-ID, personnummer eller lösenord. Valet finns kvar mellan appstarter tills du ersätter eller tar bort det. Vid nästa start använder appen valet för att öppna klasschemat. Veckoinnehåll kan sparas i en separat lokal cache enligt nedan. Välj Byt skola eller klass för att ersätta valet eller Glöm sparat schema i Inställningar för att ta bort det. Appen visar fel om lagringen eller raderingen inte lyckas. Detta raderar inte uppgifter hos skolan eller Skola24. På iOS ligger filen i appens dokumentområde och är inte undantagen från enhetsbackup. Tidigare säkerhetskopior hanteras separat från appens radering.

### Kom ihåg att du har kommit igång

När ett schema har valts och sparats behåller appen också en liten lokal markering om att du redan har kommit igång. Den ligger i appens dokumentområde, oberoende av koduppdateringar, och innehåller bara en teknisk formatversion och värdet att ett val har sparats, inte skola, klass, ID eller schemainnehåll. Giltiga tidigare sparade val kan skapa markeringen automatiskt. Om aktuella schemauppgifter inte kan hämtas visas en möjlighet att försöka igen eller byta schema i stället för att nätverksfelet behandlas som en första appstart. Glöm sparat schema tar bort markeringen tillsammans med det sparade valet. På iOS är filen inte undantagen från enhetsbackup och tidigare säkerhetskopior hanteras separat.

### Sparat visningsläge

Appen kommer ihåg om du senast valde Schema eller Original. Bara visningsläget och en teknisk formatversion sparas i en liten separat fil i appens dokumentområde, utan skola, klass, ID eller schemainnehåll. Valet behålls mellan appstarter och koduppdateringar tills du väljer ett annat visningsläge; Glöm sparat schema ändrar inte denna visningsinställning. På iOS är filen inte undantagen från enhetsbackup.

### Lokalt sparade offentliga veckoscheman

Från koduppdateringen för build 11 den 13 september 2026 kan appen spara hämtade offentliga klassveckor som JSON i en separat fil i appens dokumentområde på enheten. Cachen innehåller skolans och klassens tekniska val, visningsnamn, vecka och schemauppgifter som lektionstider, ämnen, salar och eventuella lärarnamn. Högst åtta poster och 512 KiB behålls; poster äldre än 21 dagar återanvänds inte och sorteras bort vid senare skrivning. En tillgänglig sparad vecka kan visas utan att invänta nätverket. Den kan vara äldre än skolans senaste uppgifter: appen försöker uppdatera när den används med internetanslutning. Bara tidigare hämtade veckor kan visas utan nätverk. Originalvyn kan också sparas enligt det separata avsnittet nedan. Glöm sparat schema tar bort klassvalet och veckocachen; ett lyckat byte till ett annat schema rensar tidigare klasscache. På iOS är cachefilen inte undantagen från enhetsbackup och tidigare säkerhetskopior hanteras separat. Detta raderar inga uppgifter hos skolan eller Skola24.

### Lokalt sparad Originalvy

Originalvyn kan sparas som normaliserade vektordata i en separat fil i appens dokumentområde. Den innehåller schemats texter, exempelvis ämnen, lärare och salar, samt rutornas och linjernas placering och utseende. Högst åtta visningsunderlag och sammanlagt 512 KiB sparas. Ett underlag återanvänds bara om det är högst 21 dagar gammalt och matchar valt schema, år, vecka, dag eller veckoformat och visningsstorlek. Äldre uppgifter kan ligga kvar även efter att de slutat återanvändas, tills de ersätts eller filen raderas. För offentliga klasser används skolans och klassens tekniska val; ett ID-schema kopplas med en slumpmässig lokal nyckel till ditt sparade ID-val. Appen lägger inte till ID:t som identifierare i Originalfilen eller dess nycklar. Schemat kan innehålla personuppgifter i de texter som skolan visar. När visningsstorleken är känd kan appen förbereda den valda veckans dagar och ett begränsat antal närliggande dagar och veckor i bakgrunden medan appen används. Hämtningarna gäller samma valda schema och ryms inom cachegränserna ovan. Sparat underlag visas först och uppdateras via Skola24 när nätverk finns. Ett ännu inte hämtat underlag, en annan dag eller en ny visningsstorlek kan behöva nätverk. Glöm sparat schema tar även bort Originalcachen och ett byte av schema rensar andra val. På iOS är filen inte undantagen från enhetsbackup; tidigare säkerhetskopior hanteras separat.

### Schema-ID eller elev-ID

Om den valda skolan stöder det kan du ange ett Schema-ID eller elev-ID. ID:t skickas till Skola24 för att hämta det schema du väljer. Från koduppdateringen för build 11 den 13 september 2026 sparas det stödda ID:t, skolans tekniska val och det senast hämtade veckoschemat i en separat fil i appens dokumentområde på enheten. Filen rymmer ett ID-val med en veckobild av schemauppgifterna, högst 256 KiB, inklusive lektionstider, ämnen, salar och eventuella namn i schematexten. ID-valet finns kvar mellan appstarter tills du ersätter det eller väljer Glöm sparat schema i Inställningar. En sparad vecka återanvänds bara om den är högst 21 dagar gammal och motsvarar den aktuella begärda veckan och året. Annars används det sparade ID:t för att hämta rätt vecka, utan att du behöver ange det igen. Utgångna schemauppgifter kan ligga kvar i filen tills den ersätts eller raderas. Cachen kan vara inaktuell; appen försöker uppdatera via Skola24 när den används med nätverk. ID:t används inte i filnamn, cachenycklar, egna loggar eller analys. På iOS är filen inte undantagen från enhetsbackup; appens radering ändrar inte tidigare säkerhetskopior eller uppgifter hos skolan eller Skola24. Ange inte lösenord, BankID-uppgifter eller personnummer i fältet.

### Frivillig widget i iOS-testversion 3.0.7

Widgetstödet kräver iOS 17 eller senare och en version av appen med den nya widgetkomponenten. Du kan själv aktivera nästa lektion i Inställningar och lägga till widgeten på hemskärmen. Den är avstängd från början och visar bara tider om du inte separat väljer Visa lektionsdetaljer. Då kan även namn och andra personuppgifter i skolans schematext synas på hemskärmen.

Appen delar en begränsad bild av den aktuella veckans redan hämtade tider, och bara efter ditt separata val även lektionsdetaljer och färg, med widgeten i ett lokalt App Group-område på enheten. Bilden använder en slumpmässig lokal valnyckel, inte Schema-ID, elev-ID eller skolans och klassens tekniska identifierare. Widgeten kontaktar inte Skola24 och spårar inte visningar. Uppgifterna gäller högst 24 timmar från hämtningen, aldrig längre än den aktuella veckan i svensk tid; öppna appen och uppdatera aktuella veckan för nya uppgifter. Andra veckor som du bläddrar till ersätter inte widgetens aktuella vecka.

Byte av schema rensar tidigare widgetunderlag innan ett nytt delas. Avstängning och Glöm sparat schema stänger av delningen, tar bort underlaget och återställer detaljvalet till bara tider; en ändring som inte kan bekräftas visas som fel med möjlighet att försöka igen. iOS kan behålla en tidigare widgetbild efter en begränsning eller radering. Den delade filen är inte undantagen från enhetsbackup; radering ändrar inte tidigare säkerhetskopior. Radering i appen är inte ett löfte om omedelbar visuell radering från hemskärmen.

När appen har bekräftat att du uttryckligen aktiverat widgeten kan en summerad händelse räknas med bara plattform, appversion och händelsetyp, enligt avsnittet om summerad räkning nedan. Det är aktiveringsåtgärder, inte unika personer, installerade widgetar eller visningar.

### Konton, annonser och bakgrund

Appen har inga egna användarkonton eller annonser. Användningsräkningen och den frivilliga användningsstatistiken beskrivs nedan. Den efterfrågar inte lösenord, personnummer eller BankID-uppgifter. Widgetar är inte integrerade i 3.0.6; det frivilliga widgetstödet i iOS-testversion 3.0.7 beskrivs ovan. Appen schemalägger inga schemahämtningar när den inte används. Vi använder inte appens uppgifter för reklamprofilering eller automatiserade beslut om dig.

### Summerad räkning av appanvändning på iOS och Android

Appen skickar begränsade signaler när vissa saker händer: appen öppnas (och om det är första starten efter installation), en skolsökning påbörjas, en sökning ger ingen träff, en skola väljs, vad som hände när skolan hämtades (klasslista visad, Schema-ID krävs, inloggning krävs, skolan visar inte schemat eller fel), en klass eller ett ID väljs och ett offentligt schema har hämtats. Vid en sökning utan träff skickas bara en grov kategori som räknas fram i telefonen (för kort sökning, innehåller siffror, innehåller en ort vi känner till, eller annat), aldrig själva sökorden. För att känna igen första starten sparar appen en tom markeringsfil i appens dokumentområde; den innehåller inget om dig och skickas inte. Från koduppdateringen den 4 november 2026 kan även en separat tom lokal fil markera att signalen ännu inte har bekräftats. Om försöket misslyckas görs högst ett nytt försök vid nästa app-process, tills servern bekräftar mottagandet. Då sparas den vanliga markeringen och den tillfälliga filen tas bort. Ingen av filerna innehåller ett nummer, datum, skola eller andra uppgifter om dig och ingen fil skickas. Signalen räknas på mottagningsdagen, som kan vara senare än första starten. Om servern tog emot signalen men svaret försvann kan ett nytt försök räknas igen; räknaren är därför inte ett exakt antal installationer. Äldre markeringar räknas inte om. Signalen innehåller endast plattformen, händelsens namn och appens versionsnummer. Sökord, skola, klass och schemainnehåll skickas inte. Servern sparar summerade antal per dag, plattform, händelse och appversion, inte en installationsidentifierare. Schemahämtningen räknas högst en gång per app-process och UTC-dag; övriga händelser begränsas per app-process. Vår webbvärd behandlar vanlig anslutningsinformation för att leverera tjänsten. Antalen är inte antal unika människor. Ingen installationsidentifierare skickas med denna räknare. Händelserna utöver schemahämtning och versionsnumret lades till den 18 oktober 2026 via en koduppdatering på iOS; stegen efter skolvalet, första starten och kategorin för sökningar utan träff lades till den 22 oktober 2026. Från den 27 oktober 2026 räknas även när hämtning eller sparande av ett schema misslyckas, uppdelat i en grov feltyp (dataformat, nätverk, övrigt eller sparfel), utan skola, klass eller felmeddelande. Från den 29 oktober 2026 räknas även att frågan om frivillig användningsstatistik visades (summerat per dag, utan identifierare och oavsett svar).

### Uppskattning av dagliga användare utan identifierare

För att uppskatta ungefär hur många enheter som använder appen per dag beräknar servern, när appen öppnas eller ett schema hämtas, ett envägsvärde (nyckelad hash) av anslutningens IP-adress och webbläsar-/appidentifiering (user-agent) tillsammans med en slumpmässig nyckel som byts ut varje dygn (UTC). IP-adressen och user-agent sparas inte. Efter dygnsskiftet räknas antalet olika värden per plattform och både värdena och dygnets nyckel raderas vid nästa berörda appöppning, schemahämtning eller förfrågan om dagsuppskattningen. Dessutom finns en planerad daglig körning som summerar och raderar äldre värden och dygnsnycklar även när appen inte används. Misslyckade eller uteblivna körningar övervakas med en intern varningsrutin. Vid driftfel kan raderingen försenas; vi garanterar inte en exakt raderingstid. Kvar finns endast ett antal per dag och plattform. Inget sparas eller skapas i telefonen för detta, och dagar kan inte kopplas ihop. Siffran är en grov uppskattning: flera elever på samma skolnätverk kan räknas som en.

### Frivillig feedback i appen (från koduppdateringen 2026-11-05)

Du kan välja att skicka ett problem eller förslag via appens formulär. Endast den kategori och text du själv väljer skickas. Formuläret kräver inte namn, konto eller e-postadress och bifogar inte schema, skolval, skärmbilder, analys-ID eller annan automatisk appinformation. Skriv inte personuppgifter, skola, klass eller schema-ID. Fritext kan innehålla det du själv skriver; vi lovar därför inte att varje meddelande är anonymt.

Feedback används för att förstå problem, förbättra appen och prioritera funktioner, med stöd av vårt berättigade intresse av att förbättra och ge support för appen. Det är frivilligt och inget skickas förrän du trycker på Skicka. Texten lagras separat från användningsstatistik hos vår driftleverantör Pion med Cloudflare som teknisk infrastruktur. Vi sparar inte IP-adress eller user-agent i feedbacktabellen och kopplar inte meddelanden till analys-ID. Vanlig anslutningsinformation behandlas av infrastrukturen för att leverera och skydda tjänsten. Feedback används inte för reklam eller spårning. Vi lovar inte att all driftbehandling sker enbart i Sverige eller EU.

Meddelanden tas bort automatiskt inom 30 dagar. Du kan inte få ett personligt svar genom formuläret eftersom kontaktuppgifter inte efterfrågas. För kontakt eller frågor om rättigheter finns supportadressen nedan. Betygslänken öppnar App Store eller Google Play bara när du väljer den; butiken hanterar eventuell recension enligt sina villkor.

### Frivillig delning av en länk till appen (iOS-koduppdatering 7 november 2026)

Om du väljer Dela appen öppnas enhetens vanliga delningsfunktion med en fast beskrivning av appen och en länk till vår nedladdningssida. Vi bifogar inte skola, klass, schema, schema-ID, analys-ID eller kontaktuppgifter och läser inte dina kontakter. Du väljer själv om och till vem länken skickas; den valda tjänsten hanterar delningen enligt sina villkor. Appen får inte någon bekräftelse på att en mottagare har fått eller läst länken.

Som del av den summerade räkningen ovan räknas på iOS även att Inställningar öppnas och att du trycker på Dela appen. Bara plattform, händelsens namn och appversion skickas, inte mottagare, meddelandeinnehåll eller delningens utfall. Att Inställningar öppnas bevisar inte att delningsknappen har varit synlig. Länken har den begränsade källkategorin share. Om någon öppnar den räknar webbplatsen sidförfrågningar per dag och källkategori, utan besöks-ID eller cookies; vanlig anslutningsinformation hanteras av driftleverantören. Antalet kan även innehålla länkförhandsvisningar och automatiska förfrågningar och visar inte mottagare eller appinstallationer. Se även webbplatsens integritetsinformation på https://skolschema-beontime.pion.dev/integritet.

### Frivillig användningsstatistik (endast om du väljer "Ja, dela")

Från den 19 oktober 2026 frågar appen på iOS, efter att ett schema visats första gången, om du vill dela anonym användningsstatistik. Standard är av; inget nummer skapas innan du har svarat "Ja, dela". Väljer du "Nej tack" skapas inget nummer, och endast att ett svar gavs räknas summerat per dag utan identifierare. På Android ställs ingen sådan fråga och inget installationsnummer skapas; där används bara den summerade räkningen och krasch- och felrapporterna som beskrivs i det här dokumentet.

Om du väljer "Ja, dela" skapar appen ett slumpmässigt installationsnummer. Kontrollen görs när du väljer att dela och när appen öppnas eller återgår till förgrunden. Appen skickar numret, plattform och appversion; servern registrerar datum och räknar högst en aktivitet per nummer och kalenderdag. Det hjälper oss att se om samma installation används igen nästa dag eller vecka. Antalen gäller installationer, inte personer; en ominstallation eller rensad appdata kan ge ett nytt nummer. Numret är inte kopplat till ditt namn, din skola, ditt schema, sökord, ditt Apple- eller Google-konto eller din position. Servern sparar inte IP-adress eller enhetsinformation tillsammans med numret, men vår webbvärd kan tillfälligt behandla vanlig anslutningsinformation för att leverera tjänsten. Uppgifterna raderas automatiskt efter 90 dagar. Vi visar bara summerade antal, aldrig enskilda nummer.

Du kan när som helst stänga av detta under Inställningar > "Dela anonym användningsstatistik". Då raderas numret i appen och appen ber servern radera uppgifterna som hör till numret. Saknas nätverk vid det tillfället raderas de senast efter 90 dagar.

### Ändamål och rättslig grund

Uppgifter används för att visa det schema du väljer, spara ditt val av klass eller stött ID och tillgängliga schemauppgifter på enheten, leverera kompatibla appuppdateringar och besvara supportfrågor. För den personuppgiftsbehandling vi ansvarar för stöder vi oss på vårt berättigade intresse av att tillhandahålla appens funktioner, hålla appen fungerande och ge support. Behandlingen begränsas till dessa ändamål och du kan invända genom att kontakta oss. Att du använder appen ger oss inte rätt att använda uppgifter för andra ändamål. Skolan och Skola24 ansvarar för sin egen behandling enligt sina roller och uppgifter; den här policyn ersätter inte deras information.

### Support och lagringstid

Support och integritetsfrågor hanteras via kristoffer.nordstrom@outlook.com. Om du mejlar tar vi emot din e-postadress och det innehåll du själv väljer att skicka. Meddelanden används för att hantera ärendet och behålls så länge de behövs för det, för uppföljning eller för att uppfylla tillämpliga rättsliga skyldigheter. Skicka inte personnummer, lösenord, BankID-uppgifter eller en elevs privata schema. Dölj personuppgifter i skärmbilder. E-post hanteras genom Microsoft Outlook; Microsoft beskriver sin behandling, geografiska hantering och överföringsskydd i sin integritetsinformation på privacy.microsoft.com. Vi lovar inte att supportmejl enbart behandlas inom Sverige eller EU.

### Appuppdateringar

I version 3.0.1 söker appen automatiskt efter tillgängliga kompatibla koduppdateringar när den öppnas och hämtar vid behov programkod och tillhörande filer från Expos EAS Update-tjänst. För att tjänsten ska kunna välja en kompatibel uppdatering skickas vanlig anslutningsinformation, såsom IP-adress, samt teknisk information om appen och enheten, bland annat operativsystem/plattform, appens Expo-projektidentifierare, uppdateringskanal och runtime-version. Begäran innehåller också en slumpmässig klientidentifierare som lagras på enheten av uppdateringskomponenten, samt kan innehålla tekniska uppdateringsidentifierare och uppgifter om ett tidigare uppdateringsfel. Expo kan behandla sådan information för att leverera uppdateringen och följa dess funktion. Appens uppdateringskod lägger inte till ditt schema, Schema-ID, elev-ID eller sparade klassval i uppdateringsförfrågningarna. På Android är denna klientidentifierare en slumpmässig beständig installationsidentifierare (EAS-Client-ID). Expo-komponenten skickar dessutom identifierare för den aktuella och inbyggda uppdateringen och, när det finns, identifierare för nyligen misslyckade uppdateringar. Om appens nödstart tidigare registrerat ett allvarligt startfel kan en begränsad feltext skickas med nästa uppdateringsförfrågan. Detta används för att leverera kompatibla uppdateringar och återställa appen efter uppdateringsfel, inte för annonsering, allmän analys eller spårning. Installationsidentifieraren är inte Schema-ID, elev-ID eller Androids annonserings-ID. Se även Expos integritetsinformation på https://expo.dev/privacy.

### Radering på Android

På Android är säkerhetskopiering av appdata avstängd i appens konfiguration. Det är inte ett löfte om kryptering eller om radering av äldre eller externa kopior utanför appens kontroll. Glöm sparat schema tar bort appens aktuella lokala val och cache. Det skickar ingen raderingsbegäran till Skola24 eller Expo och påverkar inte deras anslutnings- eller felloggar.

### Krasch- och felrapporter

Från och med version 3.0.4 skickar appen tekniska krasch- och felrapporter till Sentry (Functional Software, Inc.) för att vi ska kunna hitta och rätta fel. Rapporterna behandlas i Sentrys EU-region (de.sentry.io). En rapport innehåller felets typ, ett rensat felmeddelande, programkodens anropsstack och grov teknisk information om app och enhet, såsom plattform, appversion, byggnummer och operativsystemsversion.

Rensningen nedan gäller rapporter från appens JavaScript-lager, inte rapporter som skapas direkt i den underliggande iOS- eller Android-koden. I den kompatibla koduppdateringen den 5 november 2026 stängs därför Sentrys inbyggda rapportering från den underliggande koden av; endast JavaScript-fel och uttryckliga felrapporter går genom appens rensning. En koduppdatering börjar gälla först när enheten har hämtat den och appen startats med uppdateringen. Äldre eller ännu inte uppdaterade installationer kan fungera annorlunda. Rapportering av systemnära krascher är inte verifierad.

Innan en JavaScript-rapport skickas rensas den i appen: skolnamn, klassnamn, söktext, citerade textstycken, långa sifferserier, e-postadresser och frågesträngar i adresser tas bort. Vi kopplar ingen användaridentifierare till rapporten, så den kan inte kopplas till appens valfria användningsstatistik. För dessa rensade JavaScript-rapporter sätts IP-fältet till null för att Sentry inte ska lägga till en IP-adress i rapporten. Schema-ID, elev-ID, personnummer, lösenord och schemainnehåll skickas inte. Från den 27 oktober 2026 skickas även en kort rapport när en schemahämtning misslyckas utan att appen kraschar; den innehåller bara en feltypskod (till exempel nätverk eller dataformat), inte felmeddelandet, skolan, klassen eller adressen. Rapporterna används enbart för felsökning, inte för annonsering, profilering eller spårning. Se Sentrys integritetsinformation på https://sentry.io/privacy/.

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
