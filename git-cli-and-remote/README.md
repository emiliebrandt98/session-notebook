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
