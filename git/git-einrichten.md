## GitHub Einrichten

Um nun auch online mit anderen via Git arbeiten zu können, benötigen wir einen GitHub-Account.

Gehe hierzu auf [GitHub](https://github.com/) und erstelle einen Account. Merke dir die E-Mail-Adresse, die Du benutzt hast, da wir diese gleich brauchen werden.

## Git Einrichten

Damit Git weiß, welche E-Mail zu benutzen ist, müssen wir erst einmal diese einrichten. Öffne hierzu deine Befehlszeile (unter Windows "Git Bash"), und tippe die folgenden Befehle ein:

```shell
git config --global user.name "name"
git config --global user.email "email"
```

Ersetze hierbei `name` mit deinem Nutzernamen auf GitHub, und `email` mit der Adresse, die Du auch auf GitHub für deinen Account genutzt hast.

Damit wir eine Verbindung zu den GitHub-Servern aufbauen können, benötigen wir einen sogenannten SSH-Key. Das klingt erst einmal nach viel, ist aber eigentlich gar nicht so viel.

### SSH Einrichten

Öffne Git Bash und erstelle einen neuen Schlüssel mit dem folgenden Befehl:

```shell
ssh-keygen -t ed25519 -C "deine-email"
```

Erneut gilt: ersetze `deine-email` mit der Adresse, die Du bei GitHub hinterlegt hast.

Anschließend fragt dich das Programm, wo du die Datei speichern möchtest. Drücke hier einfach `Enter`. Danach solltest Du folgendes sehen:

```shell
> Enter passphrase (empty for no passphrase):
> Enter same passphrase again:
```

Tippe dein Kennwort das erste mal ein und drücke `Enter`. Aus Sicherheitsgründen wird nichts angezeigt (auch keine Sternchen oder so!). Danach noch einmal das gleiche Kennwort.

Abschließend müssen wir noch den SSH-Helfer starten und mitteilen, welchen Schlüssel wir benutzen wollen:

```shell
eval "$(ssh-agent -s)"
```

Wenn du einen Output wie `Agent pid 12345` siehst, hat alles funktioniert. Also nur noch den Key hinzufügen:

```shell
ssh-add ~/.ssh/id_ed25519
```

Auch unter Windows nimmst Du `/` statt `\`.

Nun müssen wir noch GitHub den Key mitteilen. Dazu tippen wir als erstes folgenden Befehl ein:

```shell
clip < ~/.ssh/id_ed25519.pub
```

Navigiere jetzt zu deinen Account-Einstellungen auf GitHub und öffne [SSH and GPG keys](https://github.com/settings/keys). Klicke auf "New SSH key" und füge den Inhalt von deiner Zwischenablage ein. Gebe nun noch deinem Key einen Namen, damit du ihn wiederkennst. Abschließend speichern.

Als letzter Schritt verifizieren wir, dass der Key auch wirklich funktioniert. Hierzu nutzen wir folgenden Befehl:

```shell
ssh -T git@github.com
```

Tippe gegebenenfalls dein Kennwort ein. Wenn Du eine Warnung wie diese siehst, tippe `yes` und drücke `Enter`.

```shell
> The authenticity of host 'github.com (IP ADDRESS)' can't be established.
> RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
> Are you sure you want to continue connecting (yes/no)?
```

Wenn alles geklappt hat, dann solltest du folgenden Text sehen:

```shell
> Hi username! You've successfully authenticated, but GitHub does not
> provide shell access.
```

Anschließend kannst Du in [Erstes Projekt](erstes-projekt.md) lesen, wie du ein Repository erstellst und deinen Code hochlädst.
