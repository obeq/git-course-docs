### Introduktion till JSON och XML

- **JSON (JavaScript Object Notation)**: Lättviktig dataformat som används för att representera enkla datastrukturer och objektliteraler i webbutveckling.
- **XML (eXtensible Markup Language)**: Ett flexibelt textformat som används i komplexa datautbyten mellan olika system och teknologier.

---

### Syftet med JSON och XML

- **JSON**
  - Fokus på att vara kompakt och snabbtolkat.
  - Ofta använd i webbapplikationer och för API-respons.
- **XML**
  - Fokus på flexibilitet och utvidgbarhet.
  - Används ofta för att representera komplexa datastrukturer och som konfigurationsfiler.

---

### Syntax för JSON

```json
{
  "användare": {
    "namn": "Erik Svensson",
    "ålder": 30,
    "intressen": ["segling", "läsning", "programmering"]
  }
}
```

---

### Syntax för XML

```xml
<användare>
  <namn>Erik Svensson</namn>
  <ålder>30</ålder>
  <intressen>
    <intresse>segling</intresse>
    <intresse>läsning</intresse>
    <intresse>programmering</intresse>
  </intressen>
</användare>
```

---

### Jämförelse av Data Representation

- **JSON**
  - Använder objekt och arrayer.
  - Mindre verbost.
- **XML**
  - Använder element och attribut.
  - Kan innehålla metadata och namespace-information.

---

### Användningsområden

- **JSON**
  - Idealisk för mobila och webbapplikationer.
  - Snabb bearbetning och överföring.
- **XML**
  - Perfekt för komplext dokument och datavalidering.
  - Stöder avancerade funktioner som XSLT och XPath.

---

### Exempel på API-respons med JSON

```json
{
  "status": "success",
  "data": {
    "användare": {
      "id": 1,
      "namn": "Anna Lindh"
    }
  }
}
```

---

### Exempel på API-respons med XML

```xml
<respons>
  <status>success</status>
  <data>
    <användare id="1">
      <namn>Anna Lindh</namn>
    </användare>
  </data>
</respons>
```

---

### JSON Data Typer - Översikt

- JSON stödjer följande datatyper:
  - Strängar (Strings)
  - Nummer (Numbers)
  - Objekt (Objects)
  - Arrayer (Arrays)
  - Boolean (true/false)
  - null

---

### Strängar (Strings)

- Strängar måste vara inom dubbla citattecken.

```json
{
  "namn": "Olof"
}
```

---

### Nummer (Numbers)

- JSON nummer kan vara heltal eller flyttal.

```json
{
  "ålder": 42,
  "vikt": 72.5
}
```

---

### Objekt (Objects)

- Objekt är samlingar av nyckel/värde-par.

```json
{
  "användare": {
    "id": 1,
    "namn": "Lena"
  }
}
```

---

### Arrayer (Arrays)

- Arrayer är listor av värden.

```json
{
  "intressen": ["musik", "vandring", "programmering"]
}
```

---

### Boolean (true/false)

- Representerar sanningsvärden.

```json
{
  "student": false,
  "anställd": true
}
```

---

### Null

- Representerar frånvaro av ett värde.

```json
{
  "bil": null
}
```

---

### Sammansatt Exempel

- Kombinerar alla datatyper i en struktur.

```json
{
  "person": {
    "namn": "Karin",
    "ålder": 34,
    "gift": true,
    "barn": null,
    "intressen": ["fotografi", "cykling"],
    "adress": {
      "stad": "Stockholm",
      "land": "Sverige"
    }
  }
}
```

---

### XML

---

```xml
<recept>
  <namn>Chokladkaka</namn>
  <portioner>8</portioner>
  <ingredienser>
    <ingrediens mängd="200g" typ="choklad">Mörk choklad</ingrediens>
    <ingrediens mängd="100g" typ="smör">Smör</ingrediens>
    <ingrediens mängd="3st" typ="ägg">Ägg</ingrediens>
  </ingredienser>
  <instruktioner>
    <steg>Smält chokladen och smöret i ett vattenbad.</steg>
    <steg>Vispa äggen och sockret pösigt.</steg>
    <steg>Blanda alla ingredienser och häll i en form.</steg>
    <steg>Grädda i ugnen på 175 grader i 25 minuter.</steg>
  </instruktioner>
</recept>
```

---

### XML-scheman

````xml
<?xml version="1.0"?>

<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="namn" type="xs:string"/>
  <xs:element name="ålder" type="xs:integer"/>
</xs:schema>

---

```xml
<?xml version="1.0"?>
<library xmlns:bk="http://www.example.com/books"
         xmlns:cd="http://www.example.com/cds">
  <bk:title>Sailing Basics</bk:title>
  <cd:title>Favorite Sea Shanties</cd:title>
  <bk:author>Olof Larsson</bk:author>
  <cd:artist>The Sailor's Choir</cd:artist>
</library>
````

---

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:element name="användare">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="namn" type="xs:string"/>
        <xs:element name="ålder" type="xs:integer"/>
        <xs:element name="födelsedatum" type="xs:date"/>
        <xs:element name="registreringsdatum" type="xs:dateTime"/>
        <xs:element name="registrerad" type="xs:boolean"/>
        <xs:element name="email" type="xs:string"/>
        <xs:element name="pris" type="xs:decimal"/>
      </xs:sequence>
    </xs:complexType>
  </xs:element>

</xs:schema>
```

---

# Använda scheman

```xml
<?xml version="1.0" encoding="UTF-8"?>
<person xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:noNamespaceSchemaLocation="person.xsd">
  <namn>Olof Larsson</namn>
  <ålder>45</ålder>
</person>
```

---

### XSLT

- Automatisk "transform" av xml-data

---

```xml
<?xml version="1.0"?>
<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
  <xsl:template match="/användare">
    <html>
      <body>
        <h2>Användarinformation</h2>
        <ul>
          <xsl:for-each select="person">
            <li>Namn: <xsl:value-of select="namn"/></li>
            <li>Email: <xsl:value-of select="email"/></li>
          </xsl:for-each>
        </ul>
      </body>
    </html>
  </xsl:template>
</xsl:stylesheet>
```
