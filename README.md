# Neuer Proxmox Tuya-Convert Container

Dieses Skript erstellt einen neuen Proxmox LXC Container mit der aktuellste Debian Version und richtet tuya-convert ein. Um das Skript zu starten führe den folgenden Befehl in einer SSH Session oder im Proxmox Terminal aus:

```
bash -c "$(wget -qLO - https://github.com/nurChrisYT/proxmox-tuya/raw/master/create_container.sh)"
```

Während des Installationsprozesses wirst du eventuell aufgefordert deinen Speicherort oder das WiFi-Interface festzulegen (Wenn du mehr als eine Option hast). Das WiFi Interface wird dem Container zugewiesen. _(Hinweis: Wenn der Container läuft dann wird kein anderer Container oder VM zugriff auf das WiFi-Interface haben.)_ Nach der erfolgreichen Installation starte den Container, welchen das Skript erstellt hat. Benutze die angezeigten Login-Information. Um tuya-convert zu stoppen drücke `STRG + C`, tuya-convert wird angehalten und du wirst zum Login Screen zurückgebracht. Nach einem neuen Login wird tuya-convert wieder starten.

## Was benötigt wird

Damit das Skript ordentlich läuft musst du funktionables WiFi haben, dafür gibt es Linux-Wifi Sticks, schau auf meiner Seite www.netztüfteln.de, dort habe ich einen Beitrag dazu. Das Skript wird zu Beginn nach gültigen WiFi-Interfaces suchen und wird einen Error auswerfen wenn keines gefunden wird.

## Custom Firmware

Um Custom Firmware hinzuzufügen (nicht von tuya-convert), verbinde dich mit dem Samba Share den der Container erstellt. (Login Daten werden beim Login an der Shell angezeigt) und füge die Datei zum Ordner: `tuya-convert/files/` hinzu. Deine Datei wird unter dem "custom firmware" Menü gelistet.


## Forks und Edits

Dieser Fork ist von whiskerz007 und durch mich angepasst, weitere Informationen findest du bei whiskerz007 und jayroo1976.

https://github.com/whiskerz007/proxmox_tuya-convert_container

https://github.com/jayroo1976/tuyaproxmox
