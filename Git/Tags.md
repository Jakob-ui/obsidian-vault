* `-i` -> Interaktiver Modus. Ermöglicht die interaktive Auswahl von Optionen, z.B. bei `git rebase -i` zur Bearbeitung der Commit-Historie.  
* `-m "Nachricht"` -> Fügt eine Commit-Nachricht hinzu. Z.B. bei `git commit -m "Meine Commit-Nachricht"`.  
* `-a` -> Fügt alle geänderten und gelöschten Dateien automatisch zur Staging Area hinzu und committet sie. Z.B. bei `git commit -a -m "Alle Änderungen committen"`.  
* `--amend` -> Ändert den letzten Commit. Ermöglicht das Bearbeiten der Commit-Nachricht oder das Hinzufügen weiterer Änderungen. Z.B. bei `git commit --amend -m "Verbesserte Commit-Nachricht"`.  
* `-p` -> Zeigt die Änderungen jedes Commits an (Diffs). Z.B. bei `git log -p` oder `git show -p`.  
* `--oneline` -> Zeigt jeden Commit in einer einzigen Zeile an, um die Übersichtlichkeit zu verbessern. Z.B. bei `git log --oneline`.  
* `--author="Name"` -> Filtert die Commit-Historie nach einem bestimmten Autor. Z.B. bei `git log --author="Max Mustermann"`.  
* `--grep="Suchbegriff"` -> Sucht nach Commits, deren Nachrichten einen bestimmten Suchbegriff enthalten. Z.B. bei `git log --grep="Bugfix"`.  
* `--global` -> Speichert die Konfiguration global für den aktuellen Benutzer. Z.B. bei `git config --global [user.name](http://user.name/) "Dein Name"`.  
* `--hard` -> Setzt den Arbeitsbereich und die Staging Area auf den Zustand des angegebenen Commits zurück, verwirft alle nicht committeten Änderungen. Z.B. bei `git reset --hard HEAD`.  
* `--soft` -> Setzt nur den HEAD-Pointer auf den angegebenen Commit zurück, behält die Änderungen im Arbeitsbereich und in der Staging Area. Z.B. bei `git reset --soft HEAD~1`.  
* `--mixed` (Standard) -> Setzt den HEAD-Pointer zurück und aktualisiert die Staging Area, behält aber die Änderungen im Arbeitsbereich. Z.B. bei `git reset --mixed HEAD`.