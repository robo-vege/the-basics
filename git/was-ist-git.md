# Was ist Git?

Git ist ein Versionskontrollprogramm. Das klingt jetzt erst einmal kompliziert, ist es aber eigentlich gar nicht.

Im ersten Moment sieht das alles verdammt kryptisch aus und man weiß nicht so recht, wo man eigentlich anfangen soll.
Ein großer Vorteil von Git ist aber, dass Du nicht alles wissen musst, um erste Ergebnisse zu erzielen.

Git ist eine Sammlung von Dienstprogrammen in der Kommandozeile, die Änderungen in Dateien verfolgen und aufzeichnen (meistens Quellcode, aber du kannst alle möglichen Dateien wie Textdateien und sogar Bild-Dateien "tracken").

Durch diese Funktionalität kannst du alte Versionen deines Projekts wiederherstellen, miteinander vergleichen, analysieren, Änderungen zusammenführen (mergen) und vieles mehr.

Dieser Prozess wird als **Versionskontrolle** bezeichnet. Es gibt eine Reihe von Versionskontrollsystemen, die diese Aufgabe übernehmen. Vielleicht hast du schon einige von ihnen gehört - Perforce, Mercurial, CVS, SVN und mehr.

Git ist **dezentralisiert**, das bedeutet, dass es nicht von einem zentralen Server abhängig ist, um alte Versionen deiner Dateien aufzubewahren. Stattdessen funktioniert es vollständig lokal, indem es diese Daten als Ordner auf deiner Festplatte speichert. Das nennen wir auch Repository.

Du kannst jedoch eine Kopie deines Repositorys online speichern. Dadurch wird es für Teams einfacher, zusammenzuarbeiten und am selben Code zu arbeiten. Meist werden dafür externe Git-Dienste wie [GitHub](https://github.com) und [BitBucket](https://bitbucket.org) verwendet.

## Git Installieren

Um mit Git arbeiten zu können, musst du es zunächst auf deinem Computer installieren:

1. **Windows** - Am besten funktioniert [Git für Windows](https://git-scm.com/downloads), da es einmal GUI (also Grafikoberfläche) und auch eine Kommandozeile hat.
2. **Linux** - Öffne einfach ein neues Terminal und installiere Git über den Paketmanager deiner Distro, z.B. `sudo apt install git` für Debian und Debian-basiert.
3. **MacOS / OSX** - Am einfachsten ist es, [homebrew](https://brew.sh/) zu installieren und dann in einem neuen Terminal Git mit `brew install git` zu installieren.

Wenn du nicht auf der Kommandozeile mit Git arbeiten willst, kann ich dir Client-Programme wie GitHub Desktop empfehlen. Es gibt jedoch noch viele weitere Git-Programme die kostenlos nutzbar sind. Auch wenn du dich für eine GUI-Anwendung entscheidest, solltest du dennoch die wichtigsten Git Befehle kennen, weshalb wir uns vorwiegend in der Kommandozeile aufhalten werden. So lernst du die Befehle am einfachsten (learning by doing!).

Anschließend kannst du [Git Einrichten](git-einrichten.md) lesen.
