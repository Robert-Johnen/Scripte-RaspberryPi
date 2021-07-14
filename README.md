# Scripte-RaspberryPi
Ein Projekt von 2016 zur Steuerung eines ehemaligen Bombenräumpanzers mit diversen Funktionen über einen Raspberry Pi. Die Daten zur Steuerung der Komponenten wurden über eine in C# für Laptop und Smartphone erstellte Netzwerkschnittstelle geliefert. Aufgabe war der Empfang der Daten über Netzwerk, das Parsen und
Ansteuern über GPIO, Ausgabe einer Log-Datei im Browser sowie eines Live-Streams der angeschlossenen Kamera.

- nc_readgpiodata - Python-Script zum Empfang der Steuerdaten über Netzwerkschnitstelle, Parsen und Einstellen der Komponenten des Panzers (benötigt: python)
- nc_htmlserver - Bash-Script mit netcat als rudimentären HTML-Server um eine Logdatei über den momentanen Zustand der Steuerung für die Abfrage als here-Document über einen Browser bereitzustellen (benötigt: locate, nc, und cat oder tac)
- nc_camstart - Bash-Script das einen Videostream über netcat bereitstellt, der auf der Gegenseite mit mplayer abgespielt werden konnte (benötigt: locate, nc und raspivid) raspivid bot von allen Möglichkeiten die geringste Latez
