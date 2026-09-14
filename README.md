# Support för Skolschema Be On Time

## Vilken version använder du?

**Be On Time 3.0.1 — finns i TestFlight för iPhone och iPad, är kommande App Store-version och är kandidat för Google Play på Android.** Androidversionen är ännu inte offentlig. Informationen under [Hjälp för 3.0.1](#301--testflight-och-kommande-app-store-version) gäller iOS build 12 och build 11 med den senaste kompatibla koduppdateringen samt Android 3.0.1 när den publiceras. I iOS build 12 finns det beskrivna sparandet direkt i appen och kräver ingen koduppdatering vid första start.

**Be On Time 3.0.0 — nuvarande App Store-version.** Informationen under [3.0.0 — historisk hjälp för den distribuerade versionen](#300--historisk-hjälp-för-den-distribuerade-versionen) beskriver den versionen, inklusive dess tidigare PDF-funktion och manuella sparande av klassval.

[Integritetspolicy](PRIVACY.md)

## 3.0.1 — TestFlight och kommande App Store-version

Be On Time hjälper dig att se skolans schema.

### Kom igång

1. Öppna Be On Time och sök efter din skola.
2. Välj skolan. Appen kontrollerar då om den går att använda just nu.
3. Välj en tillgänglig klass eller, om skolan stöder det, ange Schema-ID eller elev-ID.
4. Se dagens schema och svep mellan dagar, eller öppna veckovyn. Vrid telefonen för en kompakt veckoöversikt. Dra ned för att uppdatera.
5. Byt skola eller klass under Inställningar när du behöver. Välj Glöm sparat schema där för att ta bort sparat klass- eller ID-val och schemacache.

Vilka klasser och sätt att öppna ett schema som visas beror på skolans publicering i Skola24. Appens inbyggda skolregister är en hjälp för sökningen, inte ett löfte om att varje skola eller klass alltid är tillgänglig. Appen behöver internetanslutning när du väljer skola och hämtar eller uppdaterar schema.

En vald offentlig klass sparas automatiskt som ett tekniskt klassval på enheten och används för att hämta klasschemat när appen startar. Med den senaste koduppdateringen kan tidigare hämtade offentliga klassveckor sparas lokalt, visas direkt vid omstart och uppdateras när nätverk finns. Bara hämtade veckor finns tillgängliga utan nätverk; kontrollera alltid ändringar mot skolans ordinarie schema. Ett stött Schema-ID eller elev-ID och dess senast hämtade vecka sparas separat på enheten. ID-valet återanvänds efter omstart tills du byter schema eller väljer Glöm sparat schema. Bara en sparad ID-vecka som matchar aktuell vecka och år och är högst 21 dagar gammal visas utan nätverk; annars hämtas rätt vecka med ditt sparade ID. Originalvyn kan också återanvända tidigare hämtade vektorunderlag efter omstart. När visningsstorleken är känd kan appen förbereda valt underlag samt närliggande dagar och veckor i bakgrunden medan appen används. En ännu inte hämtad dag eller en annan visningsstorlek kan behöva nätverk.

Ange aldrig lösenord, BankID-uppgifter eller personnummer i appen. Be On Time har inga egna konton, annonser eller köp i appen och är en fristående app, inte ansluten till eller godkänd av Skola24.

### Originalschema och uppdateringar

Växla mellan **Schema** och **Original** för att se appens lektionsvy eller skolans originalschema anpassat till skärmen, där skolan gör det tillgängligt. Original är inte en PDF-import. Från koduppdateringen för build 11 den 13 september 2026 kan hämtade originalvyer även sparas lokalt på enheten och visas utan nätverk när ett giltigt underlag för valt schema och visningsstorlek finns. Högst åtta underlag och sammanlagt 512 KiB sparas; underlag äldre än 21 dagar återanvänds inte. En ny dag eller visningsstorlek kan behöva nätverk, och sparade uppgifter kan vara inaktuella. Glöm sparat schema tar bort Originalcachen. Läs om schematext, lagring, säkerhetskopior och radering i [integritetspolicyn](PRIVACY.md).

Valet mellan **Schema** och **Original** sparas lokalt mellan appstarter och koduppdateringar. Byt läge med väljaren längst ned på skärmen.

Från version 3.0.1 build 11 kan appen automatiskt hämta kompatibla koduppdateringar via Expo EAS Update när appen startar. Det kan ge förbättringar utan en ny installation från App Store. Uppdateringstjänstens tekniska uppgifter beskrivs i [integritetspolicyn](PRIVACY.md). På Android kan kompatibla koduppdateringar på samma sätt hämtas utan en ny installation från Google Play.

På Android är säkerhetskopiering av appdata avstängd i appens konfiguration. Det är inte ett löfte om kryptering eller om radering av äldre eller externa kopior utanför appens kontroll.

### Om något inte fungerar i 3.0.1

**Jag hittar inte skolan.** Prova en kortare del av skolans namn. Skolregistret kan sakna en skola eller innehålla ett äldre namn. Använd skolans ordinarie schemalänk om skolan inte går att hitta. Vid kontakt med oss räcker skolans namn och den offentliga schemalänken — skicka inte elevuppgifter.

**Skolan finns, men ingen klass går att öppna.** Att skolan finns i sökningen betyder inte att den tillåter offentlig schemavisning. Kontrollera internetanslutningen och försök igen senare. Skolan kan ha ändrat sin publicering. Använd skolans ordinarie schema om appen inte kan hämta uppgifterna; försök inte kringgå inloggning eller andra åtkomstbegränsningar.

**Original går inte att visa.** Prova vyn **Schema**. Skolans publicering avgör vilka uppgifter som kan hämtas. Om tider saknas eller verkar fel ska du kontrollera dem mot skolans ordinarie schema.

**Måste jag välja skola igen efter en koduppdatering?** Ett sparat klass- eller ID-val och markeringen att du redan har kommit igång ligger kvar på enheten när appen får en koduppdatering. Om veckans schema inte kan hämtas kan du försöka igen utan att börja om. ID-val som gjordes innan lokal ID-lagring infördes behöver dock väljas en gång för att kunna sparas. Radering av appen eller ett uttryckligt Glöm sparat schema tar bort det lokala valet.

**Kommer appen ihåg mitt Schema-ID?** Ja, från den senaste koduppdateringen för build 11 sparas stödda Schema-ID och elev-ID på enheten tillsammans med ett veckoschema. Ett ID som angavs före uppdateringen behöver väljas igen en gång för att sparas. Ta bort det med Glöm sparat schema i Inställningar. På iOS är uppgifterna inte undantagna från enhetsbackup; se integritetspolicyn.

**Hur får jag en kompatibel koduppdatering?** Från build 11 söker appen efter uppdateringar när den startar med internetanslutning. En hämtad uppdatering kan börja användas först nästa gång appen startas om. En ny appversion eller en ändring av appens inbyggda delar kan fortfarande kräva en uppdatering via TestFlight eller App Store. Radera inte appen för att försöka tvinga fram en koduppdatering.

## Kontakta oss

Mejla [kristoffer.nordstrom@outlook.com](mailto:kristoffer.nordstrom@outlook.com) och skriv **Be On Time** i ämnesraden. Ange appversion, iOS- eller Android-version och vilka steg som ledde till problemet.

Skicka inte personnummer, lösenord, BankID-uppgifter eller en elevs privata schema. Om en skärmbild behövs, dölj namn, schemaidentifierare och andra personuppgifter först.

## 3.0.0 — historisk hjälp för den distribuerade versionen

Följande gäller Be On Time 3.0.0. Det är historisk information för den nuvarande distribuerade versionen och gäller inte den kommande 3.0.1-versionen ovan.

### Hämta ett offentligt klasschema

1. Öppna **+** och välj **Offentlig klass**.
2. Ange skolans Skola24-värd, utan `https://`.
3. Välj skola och en offentligt tillgänglig klass.
4. Visa dagens lektioner eller vrid enheten för en veckoöversikt.

Funktionen använder Skola24s tjänst, inte demonstrationsdata. Skolan måste tillåta offentlig visning av klasser. Skolor som kräver inloggning, personnummer eller BankID stöds inte i denna version. Be On Time är en fristående app och är inte ansluten till Skola24.

**Viktigt:** Den nya offentliga hämtningen är ännu inte färdigverifierad genom hela flödet på iPhone. Kontrollera lektionstider mot skolans ordinarie schema. Om du slår på **Kom ihåg** sparas skolans och klassens tekniska val lokalt mellan appstarter. Nästa gång väljer du själv att öppna det sparade klasschemat. Hela schemat sparas inte för offlinevisning. Stäng av funktionen eller välj **Glöm sparat klassval** för att ta bort valet.

### Varför visas en demonstrationsvecka?

Appen börjar med en tydligt märkt **syntetisk demo**. Det är påhittade lektioner för att prova dag- och veckovyer, inte ditt riktiga skolschema. Ett offentligt klasschema hämtas först när du själv väljer skola och klass.

### PDF-förhandsgranskning

Öppna **+** och välj **Importera PDF** för att välja en lokal PDF. Funktionen är avsedd att visa möjliga tider och textrader; den sparar inte innehållet som ett schema. Det valda PDF-flödet är ännu inte färdigverifierat på iPhone.

- PDF:en behöver innehålla läsbar text. Skannade bilder och lösenordsskyddade filer stöds inte.
- Gränserna är 10 MB och 20 sidor. Även skadade eller annars oläsbara filer kan avvisas.
- Appen behandlar en tillfällig kopia lokalt och laddar inte upp PDF:en. Originalfilen raderas inte.
- Appen försöker radera sin tillfälliga dokumentväljarkopia efter behandlingen och visar en varning om rensningen inte kan bekräftas.

### Funktioner som inte ingår

Version 3.0.0 har ännu inte originalbilder av scheman, Schema-ID/personnummer, BankID, widgets, påminnelser eller smartalarm. Gamla inställningar migreras inte automatiskt. Vissa av dessa val kan synas som otillgängliga i den aktuella versionen.

### Om hämtningen misslyckas

Kontrollera värdnamnet och internetanslutningen. Skolan kan ha stängt av offentlig klassvisning eller använda en annan tjänst. Försök inte kringgå inloggning eller åtkomstbegränsningar. Använd skolans ordinarie schemalänk om uppgifterna inte går att hämta eller verkar felaktiga.
