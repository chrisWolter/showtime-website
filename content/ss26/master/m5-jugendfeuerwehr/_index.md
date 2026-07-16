+++
project_id = "M5"
title = "ResQ: A Scalable BYOD Public Game Framework"
subtitle = "Lokaler Multiplayer für Messe-Crowds direkt im mobilen Browser. Keine App, kein Stress"
claim = "Ein Projekt von Team ResQ. Lokaler Multiplayer für Messe-Crowds direkt im mobilen Browser. Keine App, kein Stress"

# Properties for displaying the project in the project list
card_image = "assets/resq_logo.webp"

# Alphabetically sorted team list
team = ["Luca Hobiger", "Lukas Kaik", "Felix Schindler", "Yan-Lennart Schwanbeck", "Christian Wolter", "Lucas Zaworski"]
supervisor = ["Martin Steinicke", "Alexander Kramer"]
draft = false

website_link = ""
source_link = ""
+++

{{<image src="assets/resq_logo.webp" alt="ResQ Logo">}}

{{<section title="Die Herausforderung">}}
Wie gelingt es auf Messen, Ausstellungen oder öffentlichen Events, eine große Gruppe von Menschen spontan und aktiv in ein interaktives Multiplayer-Erlebnis einzubinden? Herkömmliche Setups scheitern oft an teurer und wartungsintensiver Spezial-Hardware oder an der Hürde, dass Nutzer vorab extra eine App herunterladen müssen. 

Hier setzt das von uns entwickelte ResQ-Framework an. Ursprünglich als interaktiver Anziehungspunkt zur Nachwuchsgewinnung für die Jugendfeuerwehr konzipiert, bietet ResQ eine universelle, erweiterbare Plattform für lokale Multiplayer-Spiele. Das Framework übernimmt die anspruchsvollen Hintergrundprozesse: Es automatisiert das Session-Management, regelt das dynamische Ein- und Auswählen von Spielern und sorgt für eine extrem performante Echtzeit-Synchronisation aller Clients. So können sich Spieleentwickler voll auf das eigentliche Gameplay konzentrieren, während ResQ die reibungslose Vernetzung garantiert.
{{</section>}}

{{<section title="Proof of Concept: \"Wassermarsch\"">}}
Um das ResQ-Framework auf Herz und Nieren zu prüfen und zu demonstrieren, was unter der Haube steckt, haben wir das asymmetrische Koop-Spiel *Wassermarsch* entwickelt.

In diesem actiongeladenen Spiel steuern die Mitspielenden über ein stark vereinfachtes digitales Gamepad auf ihrem eigenspannungsgeladenen Smartphone kleine Feuerwehr-Avatare auf dem Main Screen. Das Ziel: Gemeinsam Brände löschen und die Löschwassertanks koordinieren. Da die Steuerung vollständig im Browser läuft und das Framework Latenzen minimiert, reagieren die Avatare ohne spürbare Verzögerung. Das Spiel verlangt eine enge Absprache unter den Spielenden und beweist eindrucksvoll die Praxistauglichkeit unseres Frameworks.

{{</section>}}

{{<mediathek id="1e6347a8206cd49acc85f444b7039eeb" title="Wassermarsch in Aktion">}}


{{<section title="Zukunft & Open Source">}}
* **Erweiterbarkeit durch neue Spielmodule:** Die Architektur des Frameworks ist modular aufgebaut. Dadurch können neue Minispiele und Spielideen, wie physikbasierte Team-Challenges, unkompliziert hinzugefügt werden.
* **Dynamisches Auto-Balancing:** Eine geplante API-Erweiterung wird den Schwierigkeitsgrad des Spiels in Echtzeit an die aktuelle Anzahl der aktiven Spieler-Smartphones anpassen, um stets eine faire Herausforderung zu bieten.
{{</section>}}
