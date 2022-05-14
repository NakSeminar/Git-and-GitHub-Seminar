
# Seminar: Git & GitHub - Generierung von SSH-Keys

## 1) Generierung der SSH-Keys (public und private)<br>
``$ ssh-keygen -t rsa -b 4096 -C "myName@myProvider.myContry"`` z.B. ``naksem@gmx.de``<br>
>``Generating public/private rsa key pair.``<br>
>``Enter file in which to save the key (/home/ubuntu/.ssh/id_rsa):``<br>
>``/home/ubuntu/.ssh/id_rsa already exists.``<br>
>``Overwrite (y/n)? y`` <== nur überschreiben, wenn alte Key nicht mehr nötig<br>
>``Enter passphrase (empty for no passphrase):`` <== Ein gutes Passwort eingeben und merken/aufschreiben<br>
>``Enter same passphrase again:`` <== Dasselbe Passwort erneut eingeben<br>
>``Your identification has been saved in /home/ubuntu/.ssh/id_rsa.``<br>
>``Your public key has been saved in /home/ubuntu/.ssh/id_rsa.pub.``<br>

## 2) Der ssh-agend startet ein "Socket" und check die SSH-Verbindung.
* ``$ eval $(ssh-agent -s)``
## 3) Den Key dem ssh-agent hinzufügen
* ``$ ssh-add ~/.ssh/id_rsa``
## 4) Den public key anzeigen
* ``$ cat ~/.ssh/id_rsa.pub``
## 5) Um die Verbindung per ssh-keys zu nutzen, muss ein Repository per ssh geclont werden, bei Abfrage des Passwort dieses eintippen.
* ``git clone ssh://git@github.com/NakSeminar/nak-seminar-base.git``
## 6) Testen der SSH-Verbindung (wenn erfolgreich, ist das auf GitHub zu erkennen)
* ``$ ssh -T git@github.com``

## Weiterführende Infos
[Infos zu SSH-Keys bei Git](https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key)<br>
[Infos zu SSH-Keys bei GitHub](https://help.github.com/articles/connecting-to-github-with-ssh)
