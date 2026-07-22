+++
title = "Prozess"
weight = 20
draft = false
+++

{{<section title="Research & Nutzertests">}}
Ein zentraler Baustein unseres Konzepts und der Entwicklung des ResQ-Frameworks war die direkte und praxisnahe Zusammenarbeit mit der Feuerwehr. Um ein System zu schaffen, das Jugendliche wirklich begeistert und gleichzeitig auf Messen robust funktioniert, waren wir insgesamt dreimal direkt vor Ort bei der **Freiwilligen Jugendfeuerwehr Luckenwalde**:

> "Die Meinung des Jugendbetreuers änderte sich von, „noch mehr digitales Zeug“, zu „gute Idee, nicht schlecht“. …, dass die Kinder herausgefunden hatten, sich gegenseitig zu helfen und zu unterstützen."

* **Erster Besuch (Anforderungsanalyse & Interviews):** Ganz am Anfang der Projektphase besuchten wir die Freiwillige Jugendfeuerwehr Luckenwalde, um die Projektidee vorzustellen und qualitative Interviews mit den Jugendlichen zu führen. Dadurch konnten wir die genauen Wünsche und Vorkenntnisse direkt in unsere Planung einbeziehen.
* **Zweiter Besuch (Erster Prototypen-Test):** Nach der Implementierung unseres ersten spielbaren Prototyps führten wir einen ersten Nutzertest mit den Jugendlichen in Luckenwalde durch. Dies hat uns geholfen unsere Spielidee zu validieren und weitere Vorschläge aufzunehmen.
* **Dritter Besuch (Finaler Test & Validation):** Kurz vor der Fertigstellung führten wir einen zweiten Nutzertest durch. Dabei konnten wir die Stabilität unseres Frameworks und weitere Features anhand einer weiteren Gruppe Jugendlicher validieren.
{{</section>}}

{{<section title="Interner Prozess">}}
Für die interne Zusammenarbeit haben wir einen regelmäßigen Meeting-Rhythmus etabliert. Wir trafen uns im Team wöchentlich mindestens zweimal, um Fortschritte zu besprechen, offene Fragen zu klären und die nächsten Arbeitsschritte gemeinsam zu planen. Zusätzlich zu diesen Treffen gab es ein eigenes **Jour Fixe**, in dem wir über den aktuellen Projektstand, technische Blocker und kommende Entscheidungen reflektierten.

Parallel dazu arbeiteten wir mit einer **Git-Pipeline**, die unter anderem **Linting** und einheitliche Qualitätschecks umfasste. Um die Zusammenarbeit übersichtlich zu halten, haben wir uns auf einheitliche **Branch- und Commit-Messages** verständigt. Zudem wurden alle wichtigen Meetings dokumentiert, damit Entscheidungen, offene Punkte und nächste Schritte für alle Teammitglieder nachvollziehbar blieben.
{{</section>}}

{{<gallery>}}
{{<image src="assets/at_brigade.webp" alt="Interviews bei der Feuerwehr Luckenwalde" caption="Austausch und erste Interviews bei der Freiwilligen Jugendfeuerwehr Luckenwalde">}}
{{<image src="assets/user_test.webp" alt="Nutzertests mit Jugendlichen" caption="Erprobung der Controller-Steuerung und Latenztests vor Ort">}}
{{</gallery>}}

{{<section title="Herausforderungen & Lösungen">}}
Hier sind einige der größten technischen und konzeptionellen Herausforderungen, die wir im Laufe des Projekts gelöst haben:

## Captive Portal

Unser ursprünglicher Plan, die Spielenden über ein automatisiertes Captive Portal direkt nach der Verbindung mit dem WLAN ins Spiel zu leiten, scheiterte an unzureichender Hardware-Verfügbarkeit. Als Lösung entwickelten wir einen zweistufigen Workflow: Zuerst verbinden sich die Spielenden manuell mit dem WLAN, danach kann der QR-Code zum Spielbeitritt gescannt werden.

## Abstraktion der Game-Loop

Das Refactoring des ursprünglichen Spielcodes in ein wiederverwendbares Framework war eine enorme Herausforderung. Wir mussten die gesamte Spiellogik in ein modulares System aufteilen, bei dem die Verbindungs- und Session-Verwaltung generische Ereignisse an unabhängig ladbare Game-Scenes weitergibt. Dies stellt sicher, dass in Zukunft beliebige neue Minispiele mit minimalem Aufwand integriert werden können.
{{</section>}}
