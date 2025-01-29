### Häufigste Commands
#### Erstellen
* `. git init` -> Initialisiert ein neues Git-Repository im aktuellen Verzeichnis.  
* `. git clone <repository_url>` -> Erstellt eine lokale Kopie eines bestehenden Git-Repositories.  
#### Commits
* `. git add <filename>` -> Fügt eine Datei zur Staging-Area hinzu, um sie für den nächsten Commit vorzubereiten.  
* `. git add .` -> Fügt alle geänderten Dateien im aktuellen Verzeichnis und seinen Unterverzeichnissen zur Staging-Area hinzu.  
* `. git commit -m "Commit message"` -> Erstellt einen neuen Commit mit den Änderungen, die sich in der Staging-Area befinden.  

#### Git status
* `. git status` -> Zeigt den Status des Repositorys an, einschließlich geänderter, hinzugefügter und gelöschter Dateien.  
* `. git log` -> Zeigt die Commit-Historie des aktuellen Branches an.  
* `. git branch` -> Listet alle Branches im Repository auf.  

#### Git branches aktualisieren
* `. git checkout <branch_name>` -> Wechselt zum angegebenen Branch.  
* `. git merge <branch_name>` -> Führt den angegebenen Branch in den aktuellen Branch ein.  
* `. git pull` -> Holt die neuesten Änderungen vom Remote-Repository und führt sie in den aktuellen Branch ein.  
* `. git push` -> Überträgt die lokalen Commits an das Remote-Repository.  
* `. git remote add origin <repository_url>` -> Fügt ein Remote-Repository mit dem Namen "origin" hinzu. (Oft verwendet, um dein lokales Repository mit einem auf GitHub oder GitLab zu verbinden)
#### Git branches löschen 
* `. git branch --delete <branch_name>` -> löscht einen lokalen branch
* `. git branch --delete --remote <origin/branch_name>` -> löscht einen remote branch