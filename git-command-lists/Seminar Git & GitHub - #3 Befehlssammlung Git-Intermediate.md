# Seminar: Git & GitHub - Befehlssammlung "Git-Intermediate"

## Branch-Operationen
* ``git branch <branch-name>`` Erstellt einen neuen Branch auf dem aktuellen Stand (_wechselt aber nicht auf diesen_).
* ``git branch -d <branch-name>`` Löscht einen lokalen Branch.
* ``git branch -D <branch-name>`` Erzwingt das löschen eines lokalen Branches.
* ``git branch -m <new-branch-name>`` Bennent den aktuellen Branch um.
* ``git branch -m <old-branch-name> <new-branch-name>`` Bennent einen bestimmten Branch um.
* ``git checkout -b <branch-name>`` Erstellt einen neuen Branch auf dem aktuellen Stand (_& wechselt auf diesen_).
* ``git checkout <branch/commit-sha>`` Wechselt lokal auf den angegebenen Branch/Commit.
* ``git worktree list`` Zeigt alle [worktrees](https://git-scm.com/docs/git-worktree) des aktuellen Repositories.

## Merge-Operationen
* ``git merge <branch>`` Merged einen lokalen Branch in den aktuellen Branch.
* ``git merge --no-ff <branch>`` Erzwingt das Mergen, auch, wenn eigentlich kein Merge nötig wäre.
* ``git rebase <from-branch>`` Führt einen Rebase-Merge des angegebenen auf den aktuellen Branch aus. 
* ``git rebase -i <from-branch>`` Führt einen Rebase-Merge im interaktiven Modus aus.

## Remote-Operationen
* ``git remote add <name> <url/uri>`` Fügt eine neue Remote-Referenz zum lokalen Repository hinzu. (Standardname ist ``origin``.)
* ``git clone <url/uri> <lokaler-ordner/pfad>`` Erstellt eine lokale Kopie des über die URL angegebenen Remote-Repositories unter dem angegebenen Pfad.
* ``git remote -v`` Listet alle Remotes des lokalen Repositories auf.
* ``git remote set-url <name> <new-url/uri>`` Ändert die Remote-Referenz eines bestimmten Remote-Eintrages.
* ``git pull --rebase`` Zieht alle Änderungen des Remotes und führt diese mit einem Rebase-Merge mit dem lokalen Stand zusammen.
* ``git pull <remote> <branch>`` Führt einen Merge in den lokalen Stand direkt aus dem Remote-Stand aus.
* ``git push -u <remote> <remote-branch>`` Lädt alle aktuellen Änderungen auf den angegebenen Remote-Branch hoch und setzt die lokale referenz für den aktuellen Branch.
* ``git push`` Lädt alle aktuellen Änderungen auf das Remote-Repository hoch.

## Log-Operationen
* ``git log -p -n <number>`` Zeigt alle Änderungen in den letzten ``number`` commits.
