# Välkomna!

-----

# Energinivå

Nivå:
Lugn - orolig
Låg energi - Hög energi

-----

# Målet för dagen
- Lura andra att förbättra min presentation

-----

# Dina mål
- Förstå grunderna i versionshantering
- Få med en perfekt lärobok i Git hem

-----

## Följ med eller titta hemma
https://gitcourse.olofab.se

-----

# Schema

- **09:00** - Översikt och en första övning
- **10:00** - Använda Git
- **11:00** - Git och Github
- **12:00** - Lunch
- **13:00** - Software Development Cycles
- **14:00** - Gemensamt projekt
- **15:45** - Uppsamling och avslutning

-----

# Vad är Versionshantering?

Note:
Versionshantering är ett system som registrerar ändringar i en fil eller flera filer över tid så att du senare kan återgå till specifika versioner.

Varför är det viktigt?
- Spåra och återställa tidigare versioner
- Samarbeta i team
- Översikt över projektets historia och utveckling

-----

# Introduktion till Git

## Git är...

-----

## Några vanliga kommandon:

```sh
git clone
git add
git commit
git push
````

Note:

## Git är
- Ett av de mest populära versionshanteringssystemen
- Distribuerat, varje kopia är en fullständig backup av repot
- Snabbt och effektivt för både små och stora projekt


-----

# Historiska exempel

- Linux Kernel
- Flutter
- freeCodeCamp
- VS Code
- Styrdatorn till Apollo 11
- oh-my-zsh

Note:
1. Linux Kernel
2. Flutter: Google's UI toolkit for crafting natively compiled applications for mobile, web, and desktop from a single codebase. Flutter is open-source and has a large community of contributors[3].
3. freeCodeCamp: An open-source community that helps you learn to code for free. With thousands of articles, videos, and interactive lessons, freeCodeCamp is one of the most starred projects on GitHub, offering certifications in various domains of software development[7].
4. VS Code: Microsoft's free and open-source code editor, Visual Studio Code, is highly customizable and has a vast ecosystem of extensions. It's managed on GitHub and is one of the most popular development tools among programmers[3].
5. oh-my-zsh: A delightful, open-source, community-driven framework for managing your Zsh configuration. It comes bundled with thousands of helpful functions, helpers, plugins, themes, and a few things that make you shout, "Oh My ZSH!"[7].

-----
# Fler exempel
- wtfjs
- Chromebrew
- The Coding Interview University
- Shakespear's samlade verk
- System Design Primer

Note:
1. wtfjs: A list of funny and tricky JavaScript examples. This project is a collection of quirky and unexpected JavaScript snippets that can surprise even seasoned developers. It's a fun way to learn about the oddities of JavaScript[4].
2. Chromebrew: A package manager for Chrome OS that enables users to install command-line applications and tools on Chromebooks, expanding the capabilities of Chrome OS beyond its default web-based applications[2].
3. The Coding Interview University: Initially a personal study plan for becoming a software engineer, this repository has evolved into a comprehensive guide covering computer science study topics and interview preparation materials. It's a fun project because it started as a personal checklist and grew into a resource used by thousands[3].
4. System Design Primer: Learn how to design large-scale systems. This repository is a great resource for preparing for system design interviews, and it's structured in a way that's both educational and entertaining for those interested in architecture and engineering[3].

-----

## Dags för er att börja jobba

- Installera Git
- Hämta kursrepo på: 

https://github.com/obeq/git-course-docs

```bash
git clone [repository-URL]
```

-----

# Övning 1

1. Gör en intervju med en annan person i rummet.
2. Om det plötsligt bröt ut en zombie-attack, vad skulle du göra då?
3. Skriv ner svaret på frågorna i ett dokument i Markdown-format
4. Spara dokumentet under `interviews`

---
```sh
# Clona repgit clone https://github.com/obeq/git-course-docs

# Navigera in i repomappen
git-course-docs

# Skapa en ny branch med studentens namn
git checkout -b [ditt-namn]

# Skapa en fil med intervjusvar
touch [filnamn].md
# Ersätt [filnamn] med ett lämpligt namn, exempelvis intervjusvar.txt

# Öppna filen i en texteditor för att skriva in svaren
nano [filnamn].md
# Eller
notepad.exe [filnamn].md

# Lägga till filen i staging ar
git add [filnamn].md

# Commita filen med ett meddelan
git commit -m "Lägger till mina intervjusvar"

# Pusha branchen (och ändringarna) till remote repositor
git push --set-upstream origin [studentens-namn]

# Om du får gnäll på att du behöver konfigurera namn och mailadress, följ bara instruktionerna!
```

Note:
Mer information om --set-upstream: https://stackoverflow.com/questions/37770467/why-do-i-have-to-git-push-set-upstream-origin-branch
