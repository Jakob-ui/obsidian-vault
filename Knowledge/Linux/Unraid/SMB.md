### SMB-Share von Unraid unter Arch Linux einbinden

1. Benötigte Pakete installieren

sudo pacman -S cifs-utils

2. Mount-Verzeichnis erstellen

sudo mkdir /mnt/unraid_share

3. Temporär manuell einbinden

sudo mount -t cifs -o username=dein_unraid_nutzername,password=dein_unraid_passwort //192.168.1.100/dein_share_name /mnt/unraid_share

4. Permanent in fstab eintragen

(Optional, aber empfohlen)

Sichere Methode mit Credentials-Datei:

- Credentials-Datei anlegen (nur für dich lesbar):
    
    nano ~/.smbcredentials
    
    username=dein_unraid_nutzername
    
    password=dein_unraid_passwort
    
- Dateirechte anpassen:
    
    sudo chmod 600 ~/.smbcredentials
    
- Eintrag in /etc/fstab:
    
    sudo nano /etc/fstab
    
    //192.168.1.100/dein_share_name /mnt/unraid_share cifs credentials=/home/dein_nutzer/.smbcredentials,uid=dein_nutzer_uid,gid=dein_nutzer_gid,vers=3.0 0 0
    

5. Mount testen

sudo umount /mnt/unraid_share

sudo mount -a