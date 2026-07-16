+++
title = "Prozess"
weight = 20
draft = false
+++

{{<section title="Research & Nutzertests">}}
Ein zentraler Baustein unseres Konzepts und der Entwicklung des ResQ-Frameworks war die direkte und praxisnahe Zusammenarbeit mit der Feuerwehr. Um ein System zu schaffen, das Jugendliche wirklich begeistert und gleichzeitig auf Messen robust funktioniert, waren wir insgesamt dreimal direkt vor Ort bei der **Freiwilligen Jugendfeuerwehr Luckenwalde**:

* **Erster Besuch (Anforderungsanalyse & Interviews):** Ganz am Anfang der Projektphase besuchten wir die Freiwillige Jugendfeuerwehr Luckenwalde, um die Projektidee vorzustellen und qualitative Interviews mit den Ausbildern sowie den Jugendlichen zu führen. Dadurch konnten wir die genauen Wünsche, Vorkenntnisse und die räumlichen/technischen Gegebenheiten des Feuerwehr-Anhängers direkt in unsere Planung einbeziehen.
* **Zweiter Besuch (Erster Prototypen-Test):** Nach der Implementierung unseres ersten spielbaren Prototyps führten wir einen ersten Nutzertest mit den Jugendlichen in Luckenwalde durch. Dieser war ein echter Augenöffner: Wir bemerkten schnell, dass die Nutzer fast ausschließlich auf ihr Smartphone-Display starrten, anstatt das Geschehen auf dem großen Hauptbildschirm zu verfolgen. Dies gab den Ausschlag für ein radikales Redesign unseres mobilen Interfaces.
* **Dritter Besuch (Finaler Belastungstest & Validation):** Kurz vor der Fertigstellung führten wir einen zweiten, intensiven Nutzertest unter Volllast durch. Mit der überarbeiteten, blind bedienbaren Steuerung spielten die Jugendlichen in wechselnden Teams. Dabei konnten wir die Stabilität unseres WebSocket-Servers (Colyseus) und die Latenzfreiheit des Systems erfolgreich unter realen Bedingungen validieren.

{{</section>}}
{{<gallery>}}
{{<image src="assets/at_brigade.webp" alt="Interviews bei der Feuerwehr Luckenwalde" caption="Austausch und erste Interviews bei der Freiwilligen Jugendfeuerwehr Luckenwalde">}}
{{<image src="assets/user_test.webp" alt="Nutzertests mit Jugendlichen" caption="Erprobung der Controller-Steuerung und Latenztests vor Ort">}}
{{</gallery>}}
{{<section title="Herausforderungen & Lösungen">}}
Hier sind einige der größten technischen und konzeptionellen Herausforderungen, die wir im Laufe des Projekts gelöst haben:

<details style="margin-bottom: 1.5rem; padding: 1rem; border: 1px solid #ccc; border-radius: 4px; cursor: pointer;">
  <summary style="font-weight: bold; font-size: 1.1rem;">🌐 Netzwerk-Routing & Captive Portal</summary>
  <p style="margin-top: 0.5rem; line-height: 1.5;">Unser ursprünglicher Plan, die Spieler über ein automatisiertes Captive Portal direkt nach der Verbindung mit dem WLAN ins Spiel zu leiten, scheiterte an den strengen Sicherheits- und Betriebssystem-Restriktionen moderner Smartphones (insbesondere iOS und neuere Android-Versionen). Als Lösung entwickelten wir einen robusten, zweistufigen QR-Flow: Der erste QR-Code verbindet das Gerät mit dem lokalen WLAN, und der zweite leitet den Browser direkt auf den Web-Socket-Server weiter.</p>
</details>

<details style="margin-bottom: 1.5rem; padding: 1rem; border: 1px solid #ccc; border-radius: 4px; cursor: pointer;">
  <summary style="font-weight: bold; font-size: 1.1rem;">🎮 Der "Blindflug-Faktor" (Interface Design)</summary>
  <p style="margin-top: 0.5rem; line-height: 1.5;">Wie in unseren Nutzertests beobachtet, lenkte eine komplexe Steuerung die Aufmerksamkeit vom Hauptbildschirm ab. Um dies zu lösen, haben wir das mobile Interface radikal auf das Wesentliche reduziert: Ein riesiger Touch-Bereich, der als virtueller Joystick fungiert, und haptisches Feedback (Vibration) bei Interaktionen. Dadurch können die Spieler das Spiel komplett steuern, ohne ein einziges Mal auf ihr Handy schauen zu müssen.</p>
</details>

<details style="margin-bottom: 1.5rem; padding: 1rem; border: 1px solid #ccc; border-radius: 4px; cursor: pointer;">
  <summary style="font-weight: bold; font-size: 1.1rem;">🔄 Abstraktion der Game-Loop</summary>
  <p style="margin-top: 0.5rem; line-height: 1.5;">Das Refactoring des ursprünglichen monolithischen Spielcodes in ein wiederverwendbares Framework war eine enorme Herausforderung. Wir mussten die gesamte Spiellogik in ein modulares System aufteilen, bei dem die Verbindungs- und Session-Verwaltung generische Ereignisse an unabhängig ladbare Phaser-Scenes weitergibt. Dies stellt sicher, dass in Zukunft beliebige neue Minispiele mit minimalem Aufwand integriert werden können.</p>
</details>
{{</section>}}