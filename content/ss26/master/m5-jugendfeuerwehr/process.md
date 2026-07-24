+++
title = "Prozess"
weight = 10
draft = false
+++
# Prozess
## Unser Prozess hat einen Bruch, der sich lohnt zu erzählen: Wir sind mit dem Auftrag gestartet, ein Spiel zu bauen, und haben uns in der Konzeption bewusst dagegen entschieden.

{{<image src="assets/process.webp" alt="Prozess" caption="Unser Projektverlauf">}}


{{<section title="Phase 1: Interviews">}}
Beim ersten Termin bei der Jugendfeuerwehr Luckenwalde haben wir mit Kindern zwischen 10 und 15 Jahren gesprochen und ihre Wünsche, Vorschläge und Anforderungen aufgenommen.

Drei Erkenntnisse haben das Projekt geprägt:

- **Fast alle haben ein eigenes Handy.** Das hat unseren BYOD-Ansatz von einer Annahme zu einer belastbaren Grundlage gemacht.
- **Multiplayer macht Spaß, allein spielen weniger.** Gegeneinander und miteinander wurde immer wieder genannt.
- **Die Kinder kennen Joystick-Steuerung.** Brawl Stars, Fortnite und Animal Crossing arbeiten alle mit einem physischen oder digitalen Joystick plus Interaktionsbuttons. Wir mussten keine neue Steuerung erfinden, sondern eine bekannte übernehmen.

Konkrete Spielwünsche: Brandbekämpfung, auf Zeit, gegeneinander.

Dazu kamen die Rahmenbedingungen aus der Betreuung: ohne Internet, Drop-In und Drop-Out, große Gruppen sowie Replay-Value.

{{</section>}}

{{<gallery>}}
{{<image src="assets/at_brigade.webp" alt="Interviews bei der Feuerwehr Luckenwalde" caption="Austausch und erste Interviews bei der Freiwilligen Jugendfeuerwehr Luckenwalde">}}
{{<image src="assets/user_test.webp" alt="Nutzertests mit Jugendlichen" caption="Erprobung der Controller-Steuerung und Latenztests vor Ort">}}
{{</gallery>}}

{{<section title="Phase 2: Recherche">}}
Wir haben vergleichbare Projekte analysiert: Kahoot, Terra-2042, einen Skribbl.io-Klon, ein Online-Escape-Game zum richtigen Verhalten im Brandfall sowie je zehn Spiele von GamesforCrowds und Gaming Couch.

Parallel haben wir die Interaktionsformen sortiert, die auf einem Smartphone überhaupt zur Verfügung stehen (Gesten, Tippen, Wischen, GPS), und sie gegen das gehalten, was die Kinder aus ihren eigenen Spielen bereits kennen.

{{</section>}}

{{<section title="Phase 3: Konzeption und die Entscheidung">}}
Aus Interviews und Recherche sind **11 verschiedene Spielideen** entstanden. Genau an dieser Stelle stand die Entscheidung an, die das Projekt geprägt hat.

Eine der Anforderungen lautete Replay-Value: Die Kinder sollen auch beim dritten Besuch am Stand noch Lust haben. Ein einzelnes Spiel löst das nur begrenzt, denn irgendwann kennt man es. Abwechslung entsteht nicht dadurch, dass ein Spiel größer wird, sondern dadurch, dass es mehrere gibt.

Dazu kam eine zweite Überlegung: Ein Messestand der Jugendfeuerwehr ist nicht der einzige Kontext. Ein Stadtfest, ein Tag der offenen Tür, eine andere Altersgruppe: Überall passt ein anderes Spiel.

Wir haben uns deshalb entschieden, nicht ein Spiel zu bauen, sondern eine Plattform mit einer Spiele-Loop, in die sich beliebige Minispiele einhängen lassen. Aus 11 Ideen wurde damit kein Auswahlproblem mehr, sondern ein Backlog.

## Wassermarsch
Wassermarsch haben wir als erstes Spiel ausgewählt, weil es alle Anforderungen auf einmal abdeckt: Brandbekämpfung (der meistgenannte Wunsch), gegeneinander und miteinander, auf Zeit, rundenbasiert und damit messetauglich, viele Spieler gleichzeitig, Drop-In und Drop-Out, Replay-Value durch Verbesserung, und es testet genau die Interaktionsform, die aus den Interviews kam: Joystick plus Button.

{{</section>}}

{{<section title="Phase 4: Wassermarsch v0.0.1">}}
Die erste Version stand als klassischer Prototyp: ein MainScreen für den großen Bildschirm, beliebig viele User Devices als Controller, Verbindung über QR-Code, eine funktionierende Game-Loop, erste Assets und Kollisionen.

{{</section>}}

{{<section title="Phase 5: Beta-Test in Luckenwalde">}}
Mit v0.0.1 sind wir zurück nach Luckenwalde. Der Test hatte drei Ziele: die Spielidee validieren, die Interaktionsform bestätigen und die Verbindungsstabilität unter realen Bedingungen prüfen.

Der Beta-Test bestätigte zwar die Spielidee, zeigte jedoch Schwachstellen beim Verbindungsaufbau und Aufklärungsbedarf bei der Steuerung.

{{</section>}}


{{<section title="Phase 6: Umstellung auf das Framework">}}
Die konzeptionelle Entscheidung war gefallen, technisch stand aber ein gewachsener Prototyp da. Die Umstellung nach dem Beta-Test war der aufwendigste Teil des Projekts: Alles, was nicht spezifisch zu Wassermarsch gehört, musste heraus: MainScreen, Device Screen, QR-Verbindung, Session-Handling, Scoring, Timer, Leaderboard, Phasenwechsel.

Was übrig blieb, war Wassermarsch als reines Spielmodul. Und daneben ein Framework, das alles andere übernimmt.

{{</section>}}

{{<section title="Phase 7: Zwei Stränge">}}
Danach lief die Arbeit zweigleisig: Auf der einen Seite drei weitere Spiele als Beleg, dass das Framework hält, was es verspricht. Auf der anderen Seite Wassermarsch v0.0.2 mit HLFs, einer richtigen Map, Spielerfarben, Animationen für Punktgewinn und Punktverlust, Sternen bei Kollisionen sowie vielen Bugfixes.

{{</section>}}

{{<section title="Phase 8: Validierung">}}
Beide Stränge liefen in der Validierung zusammen: das Framework über die drei neuen Spiele, das Spiel über die Nutzertests. Details auf der Testing-Seite.

{{</section>}}