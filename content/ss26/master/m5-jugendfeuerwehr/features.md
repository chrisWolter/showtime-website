+++
title = "Features"
weight = 10
draft = false
+++

{{<section title="🧩 Modulares Design">}}
Die Kernarchitektur unseres Frameworks basiert auf einer strikten Trennung zwischen der Rendering-Engine auf dem Hauptbildschirm (Main Screen) und den Controllern auf den Smartphones der Spieler (Device Screens). Durch diese lose Kopplung ist das System extrem flexibel: Neue Spielideen, Spielregeln oder grafische Benutzeroberflächen können als eigenständige Module implementiert und nahtlos in das ResQ-Framework integriert werden, ohne dass die zugrunde liegende Netzwerkinfrastruktur modifiziert werden muss.
{{</section>}}

{{<section title="📱 Einfaches BYOD-Onboarding">}}
Um die Einstiegshürde für die Spieler so gering wie möglich zu halten, setzt ResQ auf das "Bring Your Own Device" (BYOD)-Prinzip. Spieler müssen keinerlei Software installieren. Über einen zweistufigen QR-Code-Flow verbinden sie sich zuerst mit dem lokalen, autarken WLAN des Systems und werden anschließend direkt im mobilen Browser auf den Spielserver weitergeleitet. Das Onboarding funktioniert innerhalb weniger Sekunden und stellt eine direkte Verbindung zum WebSocket-Server her.
{{</section>}}

{{<section title="⏳ Dynamisches Session-Management">}}
Das ResQ-Framework verwaltet alle Spieler-Verbindungen vollautomatisch. Sobald ein Spieler das Spiel verlässt oder die Netzwerkverbindung abbricht, greift ein Time-to-Live (TTL)-Mechanismus, der verwaiste Clients nach kurzer Zeit automatisch entfernt. Neue Spieler können jederzeit mitten im laufenden Spiel beitreten (Drop-In), während ausscheidende Spieler das Spielgeschehen nicht blockieren (Drop-Out). Das Framework kümmert sich eigenständig um das Neuzuweisen freigewordener Avatare.
{{</section>}}

{{<section title="⚡ Lokaler Massen-Multiplayer">}}
Der synchronisierte Spielzustand wird mit extrem hoher Frequenz zwischen Server und Clients abgeglichen. Dank der performanten Implementierung mit Colyseus und Phaser.js können bis zu 13 Spieler gleichzeitig auf demselben Bildschirm agieren, ohne dass es zu spürbaren Latenzen oder Rucklern kommt. Dies garantiert eine flüssige Spielbarkeit und maximale Responsivität, die besonders bei schnellen kooperativen Spielen wie *Wassermarsch* entscheidend ist.
{{</section>}}