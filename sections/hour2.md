# Grunder i Git
### 10:40

-----

# Repetition och Frågor

- Kort repetition av vad vi lärt oss hittills
- Har ni några frågor?

-----

## Skapa ett nytt lokalt repository
```sh
git init
```

## Clona ett befintligt repository
```sh
git clone [repo-URL]
```

Note:
Skapa en ny mapp
Kör `git init`
Visa vad som finns i `.git`, särskilt objects och refs

- objects: hjärtat
- refs: referenser till commits

-----

### Arbetsflöde

1. **Ändra** filer i din arbetskatalog
2. **Stagea** ändringar med:
   ```sh
   git add [fil]
   ```
3. **Commita** för att spara dina ändringar i repots historik:
   ```sh
   git commit -m "Ett *beskrivande* commit-meddelande"
   ```
4. **Pusha** ändringarna till remote repository:
   ```sh
   git push
   ```

Note:
Vad ska _inte_ finnas i ett commit-meddelande?

Visa vad som händer i .git för varje steg!
Add: checksum per file, save snapshot of file, updates index file with new checksum
Commit: blob object in ./git/objects, .git/HEAD and .git/index updated, .git/logs/HEAD appended
Push: calculate diff local/origin, compress, refs and objects sent

---

### Git Add Cheat Sheet

```sh
# Lägga till specifika filer
git add filnamn.txt
# Lägger till en specifik fil till staging area.

# Lägga till alla filer i katalogen (och underkataloger)
git add .
# Lägger till alla ändrade och nya filer i den aktuella katalogen och alla dess underkataloger till staging area.

# Lägga till filer interaktivt
git add -i
# Startar det interaktiva läget där du kan välja specifika filer eller delar av filer att stagea.

# Lägga till specifika delar av filer (patch)
git add -p
# Tillåter dig att interaktivt välja exakta ändringar i filer att inkludera i nästa commit. Du kan granska varje ändring och bestämma om du vill stagea den eller inte.

# Lägga till ändringar i filer, exklusive nya filer
git add -u
# Lägger till ändringar i redan spårade filer till staging area utan att lägga till nya filer som inte redan är spårade.

# Lägga till ändringar i filer, inklusive nya filer, i en specifik katalog
git add katalognamn/
# Lägger till alla ändringar och nya filer i den angivna katalogen.

# Lägga till filer med viss pattern
git add *.txt
# Lägger till alla filer som matchar patternet, i detta fall alla `.txt`-filer.
```

---

### Git commit cheat sheet

```sh
# Commita det som finns i staging med ett meddelande
git commit -m "Initial commit"

# Rätta till en gjord commit
git commit --amend -m "Corrected commit message"

# Committa alla ändringar till spårade filer, även de som inte är i staging.
git commit -a -m "Updated files with bug fixes"

# Verbose, visar mer information när du ska författa ditt meddelande.
git commit -v

# Välj filer interaktivt
git commit -p

# Ange författare till en commit
git commit --author="Author Name <author@example.com>" -m "Commit on behalf of another author"
```

---

### Git push cheat sheet

```sh
# Git Push Cheat Sheet

# Pusha den aktuella branchen till default remote (oftast origin)
git push
# Pushar commits från den lokala branchen till motsvarande remote branch.

# Pusha en specifik branch till origin
git push origin branch-namn
# Byt ut 'branch-namn' mot den faktiska branchen du vill pusha.

# Pusha alla lokala branches till remote
git push --all
# Pushar alla branches från lokalt repo till remote repo.

# Pusha tags
git push --tags
# Pushar alla lokala tags som inte finns på remote.

# Sätta upp en ny branch för tracking på remote
git push -u origin ny-branch
# Pushar 'ny-branch' till remote och sätter upp tracking. Användbart när du pushar en branch för första gången.

# Tvinga push (OBS! Använd med försiktighet)
git push -f origin branch-namn
# Tvingar en push till den angivna branchen. Detta kan skriva över historiken på remote, så använd endast när du är säker.

# Pusha en specifik commit
git push origin commit-SHA:branch-namn
# Byt ut 'commit-SHA' mot SHA-id för commiten du vill pusha och 'branch-namn' mot den branch du vill pusha till.

# Ta bort en branch på remote
git push origin --delete branch-namn
# Tar bort den angivna branchen från remote.

# Pusha en tag
git push origin tag-namn
# Pushar en specifik tag till remote.

# Pusha en branch till en specifik remote med ett annat namn
git push origin lokal-branch:remote-branch
# Pushar 'lokal-branch' till 'remote-branch' på origin. Användbart om branch-namnen skiljer sig åt.
```

-----


### Skapa en ny branch:

```sh
git checkout -b [branch-namn]
```

### Sammanfoga en branch med master:
```sh
git checkout master
git merge [branch-namn]
```

---

### Merge, rebase, fast-forward

---

![](images/git-master.png)

---

![](images/git-fastforward.png)

---

![](images/git-complex.png)

---

![](images/git-merge.png)

---

![](images/git-rebase.png)





----- 

### Övning - Branching och Merging

1. Skapa en branch där ni rättar till dessa fel
1. Se om ni kan hitta några smärre fel i `sections/hour1.md`!
3. Committa era förändringar
4. Pusha

-----

### Om det blir fel

![XKCD on git](../images/git-xkcd.png)

-----

# Sammanfattning

- Nu har vi täckt grunderna i Git, inklusive konfiguration, skapa/clona repos, det grundläggande arbetsflödet, samt branching och merging.
- Är det något ni undrar över eller vill diskutera mer?
