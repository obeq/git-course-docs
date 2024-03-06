# Mjukvaruutvecklingscykeln i Git
### 13:00

-----

# Introduktion till Mjukvaruutvecklingscykeln

Note:
- Översikt av mjukvaruutvecklingscykeln
- Rollen av Git i att stödja olika faser av utvecklingen

-----

# Planering och Uppstart

Note:
- Användning av Git och GitHub för att planera och spåra arbete
- Skapa en initial branchstruktur för projektet

---

# Projekt

Note:
Hur man använder projekt på bästa sätt

-----

## Feature Branch Workflow

![How branches are created and then merged](images/github-flow.png)

Note:
- Skapa branches för nya funktioner
- Isolera arbete och uppmuntra pull requests för kodgranskning
- Exempelkommando: `git checkout -b feature/<namn>`

-----

# Hantera Merge Konflikter

Note:
- Bästa praxis för att förebygga och lösa merge-konflikter
- Använda `git merge` och `git rebase` för att integrera ändringar

-----

# Release Branches

Note:
- Skapa en branch för varje release
- Hantera förberedelser inför release, inklusive buggrättningar och dokumentation
- Exempelkommando: `git checkout -b release/v1.0`

-----

# Hotfix Branches

Note:
- Snabba fixar på produktionskoden utan att störa pågående arbete
- Direkt integration med master och merge tillbaka till utvecklingsbranchen
- Exempelkommando: `git checkout -b hotfix/bug-fix`

-----

# Tagging och Versionering

Note:
- Använda tags för att markera releases
- Semantisk versionering för att hålla ordning på versionshistoriken
- Exempelkommando: `git tag -a v1.0.0 -m "Release 1.0.0"`

-----

# Underhåll och Iterationer

Note:
- Hantera pågående underhåll av kodbasen
- Iterativ utveckling med branches för ständiga förbättringar

-----

# Sammanfattning av Mjukvaruutvecklingscykeln i Git

Note:
- Genomgång av de olika strategierna och hur de stödjer mjukvaruutvecklingscykeln
- Vikten av god branchhantering och kommunikation i team

-----

# Frågor och Diskussion

- Vilka utmaningar ser ni med att implementera dessa strategier?
- Har ni erfarenheter av andra effektiva arbetsflöden i Git?
