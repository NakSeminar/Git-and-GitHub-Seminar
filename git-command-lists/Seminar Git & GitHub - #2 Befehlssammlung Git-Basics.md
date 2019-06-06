# Seminar: Git & GitHub - Befehlssammlung "Git-Basics"

## Projektlose Befehle
* ``git --version`` Zeigt die aktuelle Git-Version an. Gut um zu testen, ob Git installiert und aufrufbar ist.
* ``git config --list`` Zeigt die aktuellen Konfigurationsoptionen an.
* ``git config --global user.name "<user-name-here>"`` Setzt den globalen Benutzernamen, den Git beim Commit verwendet.
* ``git config --global user.email "<user-email-here>"`` Setzt die globale E-Mail-Adresse, die beim Commit verwendet wird. (Hieran wird auch in GitHub/GitLab der Avatar festgemacht.)
* ``git config --global --unset user.name`` Löscht den global eingetragenen Konfigurationseintrag von ``user.name``.  
aus welcher der 3 config-Dateien kommen die Konfigurationen
* git config --list --show-origin
  
## Wichtigste Befehle in einem Projekt
* ``git init`` Legt im aktuellen Ordner ein neues (lokales) Git-Repository an.
* ``git status`` Gibt den aktuellen Status des lokalen Repositories an. Zeigt staged & unstaged changes und aktuelle Version.
* ``git add <file-name/path>`` Fügt eine neue oder geänderte Datei zur Staging-Area hinzu, um diese im nächsten Commit mit hinzuzufügen.
* ``git add -A`` (oder oft auch ``git add .``) Fügt alle geänderten, neuen oder gelöschten Dateien werden zur Staging-Area hinzugefügt.
* ``git commit -m "<message>"`` Committed die Änderungen aus der Staging-Area in den aktuellen Branch im lokalen Repository.
* ``git commit -a -m "<message>" Fügt alle gelöschten oder geänderten (_keine neu erstellten_) in die Staging-Area hinzu und führt einen Commit aus.
* ``git reset <file-name/path>`` Entfernt die Änderungen an der Datei aus der Staging-Area.

## Nützliche andere Befehle
* ``git rm -f <file-name/path>`` Löscht eine Datei __lokal & im Staging-Area__.
* ``git rm --cached <file-name/path>`` Löscht eine Datei (__nur auf der Seite von Git__). Nützlich, um Dateien zu entfernen, die versehentlich mit in das Repository hinzugefügt wurden.
* ``git reset --soft HEAD`` Leert die aktuelle Staging-Area (behält lokale Änderungen)
* ``git reset --hard HEAD`` Leert die aktuellee Staging-Area __& verwirft lokale Änderungen!__
* ``git clean -fd`` Erzwingt das entfernen von Dateien, die nicht im Repository eingecheckt sind.
* ``git tag <tag-name>`` Benennt die aktuelle Revision im Repository über das erstellen eines Tags.
* ``git tag --list`` Gibt alle aktuell im Repository bekannten Tags aus.
