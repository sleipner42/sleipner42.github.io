# Support för Skolschema Be On Time

## Vilken version använder du?

**Be On Time 3.0.1 — kommande, ännu inte distribuerad.** Informationen under [Kommande 3.0.1](#kommande-301) gäller först när version 3.0.1 finns tillgänglig.

**Be On Time 3.0.0 — nuvarande distribuerade version.** Informationen under [3.0.0 — historisk hjälp för den distribuerade versionen](#300--historisk-hjälp-för-den-distribuerade-versionen) beskriver den versionen, inklusive dess tidigare PDF-funktion och manuella sparande av klassval.

[Integritetspolicy](PRIVACY.md)

## Kommande 3.0.1

Be On Time hjälper dig att se skolans schema.

### Kom igång

1. Öppna Be On Time och sök efter din skola.
2. Välj skolan. Appen kontrollerar då om den går att använda just nu.
3. Välj en tillgänglig klass eller, om skolan stöder det, ange Schema-ID eller elev-ID.
4. Se dagens schema eller öppna veckovyn. Dra ned för att uppdatera.
5. Byt skola eller klass under Inställningar när du behöver.

Vilka klasser och sätt att öppna ett schema som visas beror på skolans publicering i Skola24. Appens inbyggda skolregister är en hjälp för sökningen, inte ett löfte om att varje skola eller klass alltid är tillgänglig. Appen behöver internetanslutning när du väljer skola och hämtar eller uppdaterar schema.

En vald offentlig klass sparas automatiskt som ett tekniskt klassval på enheten och används för att hämta klasschemat när appen startar. Hela veckoschemat sparas inte för offlinevisning. Ett Schema-ID eller elev-ID används bara under den aktuella sessionen och sparas inte som ett klassval eller efter en omstart.

Ange aldrig lösenord, BankID-uppgifter eller personnummer i appen. Be On Time har inga egna konton, annonser eller analysfunktioner och är en fristående app, inte ansluten till eller godkänd av Skola24.

## Kontakta oss

Mejla [kristoffer.nordstrom@outlook.com](mailto:kristoffer.nordstrom@outlook.com) och skriv **Be On Time** i ämnesraden. Ange appversion, iOS-version och vilka steg som ledde till problemet.

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
