# Timme 2: Grunder i Git

-----

# Repetition och Frågor

- Kort repetition av vad vi lärt oss hittills
- Har ni några frågor?

-----
### Slide 2: Git Konfiguration

# Git Konfiguration

## Grundläggande Konfiguration
För att börja använda Git, måste vi konfigurera det:
```sh
git config --global user.name "Ditt Namn"
git config --global user.email "dinemail@example.com"
```
## Varför är detta viktigt?
- Identifierar dig som författare av dina commits
- Viktigt för samarbete och översikt

-----

# Skapa och Clona Repositories

## Skapa ett nytt lokalt repository
```sh
git init
```

## Clona ett befintligt repository
```sh
git clone [repo-URL]
```
- `git init` skapar ett nytt Git-repository lokalt
- `git clone` kopierar ett befintligt repo till din lokala maskin

Note:
Skapa en ny mapp
Kör `git init`
Visa vad som finns i `.git`, särskilt objects och refs

- objects: hjärtat
- refs: referenser till commits

-----


### Slide 4: Grunderna i Git Workflow

# Grunderna i Git Workflow

1. **Ändra** filer i din arbetskatalog
2. **Stagea** ändringar med:
   ```sh
   git add [fil]
   ```
3. **Commita** för att spara dina ändringar i repots historik:
   ```sh
   git commit -m "En beskrivande commit-meddelande"
   ```
4. **Pusha** ändringarna till remote repository:
   ```sh
   git push
   ```

- Detta är den grundläggande cykeln för att arbeta med Git.


### Slide 5: Branching och Merging

# Branching och Merging

## Branching
Skapa en ny branch:
```sh
git checkout -b [branch-namn]
```

## Merging
Sammanfoga en branch med master:
```sh
git checkout master
git merge [branch-namn]
```

- Branches tillåter dig att utveckla funktioner, fixa buggar, eller experimentera med ny kod säkert, separerat från huvud "master" branchen.


### Slide 6: Övning - Branching och Merging
# Övning - Branching och Merging

- Vi kommer nu att göra en enkel övning:
  1. Skapa en ny branch
  2. Gör några ändringar
  3. Mergea tillbaka till master

### Detta kommer att ge oss en praktisk förståelse för hur branching och merging fungerar.

### Slide 7: Sammanfattning
# Sammanfattning

- Nu har vi täckt grunderna i Git, inklusive konfiguration, skapa/clona repos, den grundläggande arbetsflödet, samt branching och merging.
- Är det något ni undrar över eller vill diskutera mer?
