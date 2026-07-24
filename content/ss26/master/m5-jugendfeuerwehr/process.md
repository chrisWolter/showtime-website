+++
title = "Das Framework"
weight = 20
draft = false
+++

# Das Framework
## ResQ nimmt einem Spiel alles ab, was nichts mit dem Spiel zu tun hat.



{{<section title="Was das Framework übernimmt">}}
Session & Verbindung

- QR-Code und automatische Verbindung
- Session-Management, Session-IDs
- Drop-In und Drop-Out, auch bei Inaktivität

Spieler-Handling

- Namenszuweisung
- Farbzuweisung
- Verwaltung der Spieleranzahl

Spielablauf

- Endlosloop mit Auswahl der Spiele
- Phasen-Handling: Connecting, Spiel läuft, Ergebnisse, Disconnecting
- Timer
- Scoring
- Leaderboard

Darstellung

- MainScreen für den großen Bildschirm
- Device Screen für die Handys
- Frontend-UI-Gerüst und Routing

{{</section>}}

{{<section title="Was ein Spielmodul liefert">}}
Drei Dateien. Mehr braucht es nicht, um ein neues Spiel in ResQ einzuhängen.
{{</section>}}

{{<section title="Belege">}}
Nach der Umstellung sind drei weitere Spiele entstanden – Quiz, Memory und Schlauchstaffel. Alle drei wurden KI-gestützt umgesetzt: Wir haben die Framework-Konventionen in einer AGENTS.md dokumentiert, sodass ein Coding-Agent neue Spielmodule regelkonform erzeugen kann. Dass das funktioniert, ist selbst ein Beleg für die Klarheit der Schnittstelle: Was eine Maschine aus der Doku bauen kann, kann auch ein fremdes Team bauen.
{{</section>}}