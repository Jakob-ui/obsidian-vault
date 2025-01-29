* `-i` -> Interaktiver Modus. Ermöglicht die interaktive Auswahl von Optionen, z.B. bei `git rebase -i` zur Bearbeitung der Commit-Historie.  
* `-m "Nachricht"` -> Fügt eine Commit-Nachricht hinzu. Z.B. bei `git commit -m "Meine Commit-Nachricht"`.  
* `-a` -> Fügt alle geänderten und gelöschten Dateien automatisch zur Staging Area hinzu und committet sie. Z.B. bei `git commit -a -m "Alle Änderungen committen"`.  
* `--amend` -> Ändert den letzten Commit. Ermöglicht das Bearbeiten der Commit-Nachricht oder das Hinzufügen weiterer Änderungen. Z.B. bei `git commit --amend -m "Verbesserte Commit-Nachricht"`.  
* `-p` -> Zeigt die Änderungen jedes Commits an (Diffs). Z.B. bei `git log -p` oder `git show -p`.  
* `--oneline` -> Zeigt jeden Commit in einer einzigen Zeile an, um die Übersichtlichkeit zu verbessern. Z.B. bei `git log --oneline`.  
* `--author="Name"` -> Filtert die Commit-Historie nach einem bestimmten Autor. Z.B. bei `git log --author="Max Mustermann"`. 