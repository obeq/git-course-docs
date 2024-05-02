### SOAP - Simple Object Access Protocol

Note:
SOAP är ett protokoll för utbyte av strukturerad information i webbtjänster. Trots att det är känt för att vara tungt jämfört med nyare protokoll, används det fortfarande i många företagsmiljöer för dess strikta säkerhets- och transaktionshantering.

---

```
POST /BookService HTTP/1.1
Host: www.example.com
Content-Type: text/xml; charset=utf-8
Content-Length: 100
SOAPAction: "http://example.com/GetBook"

<?xml version="1.0"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:book="http://example.com/book">
    <soap:Header>
        <book:Transaction TransactionID="12345"></book:Transaction>
    </soap:Header>
    <soap:Body>
        <book:GetBookDetails>
            <book:ISBN>978-3-16-148410-0</book:ISBN>
        </book:GetBookDetails>
    </soap:Body>
</soap:Envelope>

```

---

### HTTPS - Secure HyperText Transfer Protocol

Note:
HTTPS är en utökning av HTTP med säkerhet som kärnfokus, där kommunikationen krypteras via SSL/TLS. Det skyddar dataöverföringen från avlyssning och man-in-the-middle-attacker.

---

### DNS - Domain Name System

Note:
DNS översätter domännamn till IP-adresser, vilket gör det möjligt för användare att navigera på internet utan att behöva memorera numeriska IP-adresser.

---

### TCP - Transmission Control Protocol

Note:
TCP är en kärnprotokoll i Internetprotokollsviten som garanterar leverans av data i samma ordning som de skickades, vilket är avgörande för pålitlig kommunikation.

---

### Autentisering

Note:
Autentisering är processen att verifiera identiteten hos en användare, enhet eller annan enhet inom ett nätverk för att ge tillgång till systemets resurser.

---

### Cookies

Note:
Cookies är små datafiler som lagras på användarens dator av webbläsaren för att hålla koll på sessioner och lagra användarspecifik information som anpassade inställningar och inloggningsstatus.

---

### Cache

Note:
Caching minskar serverbelastning och förbättrar prestandan genom att lagra kopior av filer eller databasfrågor och återanvända dem när samma data begärs.

---

### Webhook

Note:
En webhook möjliggör automatiserad dataöverföring mellan applikationer i realtid när en händelse inträffar, utan att användaren behöver manuellt begära informationen.

---

### Websockets

Note:
Websockets tillhandahåller en tvåvägskommunikationskanal över en enda långvarig anslutning, vilket möjliggör realtidsdataöverföring mellan klient och server.

---

### CORS - Cross-Origin Resource Sharing

Note:
CORS är en säkerhetsfunktion som gör det möjligt för webbplatser att be om tillstånd att få tillgång till resurser från en server på en annan domän än den webbplatsen ursprungligen kom ifrån.

---

### Versionering av APIer

Note:
Versionering av APIer är en strategi för att hantera förändringar i API:er utan att störa befintliga klienter genom att hålla flera versioner av API:t tillgängliga samtidigt.

---

### Git

Note:
Git är ett distribuerat versionshanteringssystem som är avgörande för dagens mjukvaruutveckling, vilket möjliggör spårning av ändringar och samarbete i kodbasen.

---

### MQTT - Message Queuing Telemetry Transport

Note:
MQTT är ett lättviktigt meddelandeprotokoll, optimerat för enheter med låg bandbredd och låg prestanda, perfekt för IoT-applikationer.

---

### SMTP - Simple Mail Transfer Protocol

Note:
SMTP är standardprotokollet för att skicka e-postmeddelanden över internet, vilket styr både sändning och vidarebefordran av e-post.

---

### GraphQL

Note:
GraphQL är ett dataförfrågnings- och manipuleringsspråk för API:er som ger klienter möjlighet att begära exakt den data de beh
