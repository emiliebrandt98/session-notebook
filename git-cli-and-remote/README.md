# **iTerm:**

- **git init**: Git repo erstellen
- **gitignore**: Dateien werden ignoriert, sobald man es in dieser Datei einträgt. _Beispiele:_
  - .DS.Store
  - .env
  - node_modules
- **git add:** Datei in `staged` gelegt
- **git add .**: Es werden alle Dateien, die bearbeitet wurden, commited
- **git commit -m”added .gitignore”:** Es wurde ein “Schappschuss” (`commit`) erstellt
- **git log --oneline**: Alle Commits werden in in jeweils einer Zeile angezeigt (Commit History)
- **git restore**: “Discard Changes” (You can always return to the last committed state of the entire project)
- **git restore <filename>**: You can also restore individual files:
- **git remote -v**: Ist der Git mit einem Server verbunden?
- **git remote add:** Lokales Git wir mit dem Server verbunden
- **git push**: Und die Local Dateien mit dem auf GitHub synchronisieren (Branches sind dabei wichtig! Git Branches and PRs)
- **git pull**: Download content from the remote repository
- **git clone:** Das was in GitHub ist wird geclont und Local wieder herstellen (You can create a copy of the remote repository on your local machine)
- **git status**: Man sieht, welche Dateien `untracked`, `modified` und `staged` sind und es werden alle aufgelistet

- `untracked`: Diese Datei wurde noch nicht zu Git hinzugefügt
- `staged`: Fürs nächste `commit` vorbereitet.
- `commit`: Alle Änderungen wurden in git gesichert
- `modified`: Hast sich zum letzten `commit` geändert und muss neu hinzugefügt werden.

# How to …

…Git CLI and Remote:

1. Gehe **IN** deinen gewünschten Ordner rein.
2. `git init` eingeben und `Enter` -Drücken
3. Dieser Ordner ist nun ein Git-Respository
4. Erstelle nun auf **GitHub** ein neues Respository mit dem gleichen Namen.
5. Kopiere den SSH-Respository-Adresse, z.B. `git@github.com:<your-github-name>/web-challenges.git` und gebe `git remote add origin <ssh link>` ins iTerm ein und die Beiden miteinander zu verbinden.
6. Überprüfe den Befehl, ob das Remote-Repository erfolgreich verknüpft wurde mit `git remote -v` . Es sollten eine „Fetch“- und eine „Push“-Adresse im Terminal ausgegeben werden.
7. Nun kannst deine Unterordner oder Dateien nun mit GitHub synchronisieren oder neue Dinge hochladen.
8. Dateien die nicht zusehen sein sollen, sollten in ein `.gitignore` -File gelegt werden.
   1. Dafür verwendest du `touch .gitignore` und diese Datei zu erstellen und mit `nano .gitignore` kannst du diese im Terminal einfügen (z.B. .DS.Store, .env, node_modules).
9. Nun können alle `untracked` -Files `gestaged` werden. Das machst du für einzelne Dateien mit `git add <name>` oder mit alles Dateien mit `git add .` .
10. Diese sind nun `gestaged` und können commited werden mit dem Befehl `git commit -m ""` - die Message dabei nicht vergessen.
11. Beim ersten “Push” musst du den Befehl `git push -u origin main` ausführen, danach reicht `git push` .
12. Nun liegen alle Dateien und Ordner in einem Respository auf GitHub.
13. Bei Änderungen müssen die jeweiligen Dateien neu “geadded” werden, da sie nun `modifiziert` sind.
    1. Also `git add <name>` .
    2. `git commit -m ""`
    3. `git push`
