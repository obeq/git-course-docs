# Mjukvaruutvecklingscykeln i Git
### 13:00

-----

# Introduktion till Mjukvaruutvecklingscykeln

- Översikt av mjukvaruutvecklingscykeln
- Rollen av Git i att stödja olika faser av utvecklingen

-----

# Planering och Uppstart

- Användning av Git och GitHub för att planera och spåra arbete
- Skapa en initial branchstruktur för projektet

-----

# Feature Branch Workflow

- Skapa branches för nya funktioner
- Isolera arbete och uppmuntra pull requests för kodgranskning
- Exempelkommando: `git checkout -b feature/<namn>`

-----

# Hantera Merge Konflikter

- Bästa praxis för att förebygga och lösa merge-konflikter
- Använda `git merge` och `git rebase` för att integrera ändringar

-----

# Release Branches

- Skapa en branch för varje release
- Hantera förberedelser inför release, inklusive buggrättningar och dokumentation
- Exempelkommando: `git checkout -b release/v1.0`

-----

# Hotfix Branches

- Snabba fixar på produktionskoden utan att störa pågående arbete
- Direkt integration med master och merge tillbaka till utvecklingsbranchen
- Exempelkommando: `git checkout -b hotfix/bug-fix`

-----

# Tagging och Versionering

- Använda tags för att markera releases
- Semantisk versionering för att hålla ordning på versionshistoriken
- Exempelkommando: `git tag -a v1.0.0 -m "Release 1.0.0"`

-----

# Underhåll och Iterationer

- Hantera pågående underhåll av kodbasen
- Iterativ utveckling med branches för ständiga förbättringar

-----

# Sammanfattning av Mjukvaruutvecklingscykeln i Git

- Genomgång av de olika strategierna och hur de stödjer mjukvaruutvecklingscykeln
- Vikten av god branchhantering och kommunikation i team

-----

# Frågor och Diskussion

- Vilka utmaningar ser ni med att implementera dessa strategier?
- Har ni erfarenheter av andra effektiva arbetsflöden i Git?
