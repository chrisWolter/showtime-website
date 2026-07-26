+++
title = "Der Prozess"
weight = 10
draft = false
+++

# Der Prozess

## Unser Prozess hat einen Bruch, der sich lohnt zu erzählen: Wir sind mit dem Auftrag gestartet, ein einzigesSpiel zu bauen, und haben uns in der Konzeption bewusst dagegen entschieden.

```mermaid
flowchart TB
    %% Visuelle Themes & Styles
    classDef startPhase fill:#1e293b,stroke:#ff4d4d,stroke-width:2px,color:#ffffff,rx:6px,ry:6px;
    classDef researchPhase fill:#1e293b,stroke:#ff7a00,stroke-width:2px,color:#ffffff,rx:6px,ry:6px;
    classDef conceptPhase fill:#1e293b,stroke:#ffc107,stroke-width:2px,color:#ffffff,rx:6px,ry:6px;
    classDef devPhase fill:#1e293b,stroke:#0066ff,stroke-width:2px,color:#ffffff,rx:6px,ry:6px;
    classDef testPhase fill:#1e293b,stroke:#00f2fe,stroke-width:2px,color:#ffffff,rx:6px,ry:6px;
    classDef milestonePhase fill:#1e293b,stroke:#00e676,stroke-width:2px,color:#ffffff,rx:6px,ry:6px;

    %% Subgraph Styling (Transparent)
    style PROCESS fill:none,stroke:#475569,stroke-width:0px,color:#3e2d4a,rx:8px;

    %% Nodes
    subgraph PROCESS ["<b>PROJEKTVERLAUF & ENTWICKLUNGSPHASEN</b>"]
        direction TB

        A["<b>Herausforderung</b><br/>• Kinder warten am Messestand der Jugendfeuerwehr"]
        B["<b>Interviews in Luckenwalde</b><br/>• Wünsche & Anforderungen ermitteln<br/>• Verfügbarkeit von Handys prüfen"]
        C["<b>Recherche</b><br/>• Vergleichbare Spiele & Interaktionsformen"]
        D["<b>Konzeption</b><br/>• 11 Spielideen entwickelt"]
        F["<b>Wassermarsch v0.0.1</b><br/>• Erstes Spiel als Prototyp"]
        G["<b>1. Nutzer-Test</b><br/>• Erprobung bei der Jugendfeuerwehr"]
        H["<b>Entwicklung Framework</b><br/>• Basis-Architektur aufbauen"]
        
        I["<b>Entwicklung weitere Spiele</b><br/>• Lösch-Quiz<br/>• Feuerwehr-Memory<br/>• Schlauchstaffel"]
        J["<b>Wassermarsch v0.0.2</b><br/>• Weiterentwicklung Spiel 1"]
        
        N["<b>Validierung des Frameworks</b><br/>• Überprüfung der Modul-Architektur"]
        L["<b>2. Nutzer-Test</b><br/>• Feedback von IMI-Studierenden"]
        M["<b>3. Nutzer-Test</b><br/>• Iteration bei der Jugendfeuerwehr"]
        
        Q["<b>Wassermarsch v0.0.3</b><br/>• Finale Überarbeitung Spiel 1"]
        O["<b>Stand heute</b><br/>• ResQ-Framework mit vier fertigen Spielen"]
        P["<b>Ausblick</b><br/>• Neue Spiele einfach andocken"]
    end

    %% Ablauf-Verbindungen
    A ==> B
    B ==> C
    C ==> D
    D ==> F
    F ==> G
    G ==> H

    %% Parallele Stränge aus H
    H --> I
    H --> J

    I --> N
    J --> L
    L --> M
    M --> Q

    N ==> O
    Q ==> O
    O -. "Zukünftige Erweiterung" .-> P

    %% Class Assignments
    class A startPhase;
    class B,C researchPhase;
    class D conceptPhase;
    class F,H,I,J,Q devPhase;
    class G,L,M,N testPhase;
    class O,P milestonePhase;

    %% Link Styling
    linkStyle 0,1,2,3,4,5 stroke:#94a3b8,stroke-width:2px;
    linkStyle 6,7 stroke:#0066ff,stroke-width:2px;
    linkStyle 8 stroke:#0066ff,stroke-width:2px;
    linkStyle 9,10,11 stroke:#00f2fe,stroke-width:2px;
    linkStyle 12,13 stroke:#00e676,stroke-width:2px;
    linkStyle 14 stroke:#00e676,stroke-width:2px,stroke-dasharray: 4 4;
```

{{<section title="Phase 1: Interviews">}}
Beim ersten Termin bei der Jugendfeuerwehr Luckenwalde haben wir mit Kindern zwischen 10 und 15 Jahren gesprochen und ihre Wünsche, Vorschläge und Anforderungen aufgenommen.

Drei Erkenntnisse haben das Projekt geprägt:

- **Viele Kinder haben ein eigenes Handy.** Das hat unseren BYOD-Ansatz gestützt.
- **Multiplayer macht Spaß, allein spielen weniger.** Die Kinder sind es Spiele gewohnt in denen sie gegeneinander und miteinander spielen.
- **Die Kinder kennen Joystick-Steuerung.** Brawl Stars, Fortnite und Animal Crossing

Konkrete Spielwünsche: Brandbekämpfung, auf Zeit, gegeneinander.

Dazu kamen die Rahmenbedingungen aus der Betreuung: ohne Internet, Drop-In und Drop-Out, große Gruppen sowie Replay-Value.

{{</section>}}

{{<gallery>}}
{{<image src="assets/at_brigade.webp" alt="Interviews bei der Feuerwehr Luckenwalde" caption="Austausch und erste Interviews bei der Freiwilligen Jugendfeuerwehr Luckenwalde">}}
{{<image src="assets/user_test.webp" alt="Nutzertests mit Jugendlichen" caption="Erprobung der Controller-Steuerung und Latenztests vor Ort">}}
{{</gallery>}}

{{<section title="Phase 2: Recherche">}}
Wir haben vergleichbare Projekte in Bezug auf Public Games sowie Feuerwehr analysiert: Kahoot, Terra-2042, einen Skribbl.io-Klon, ein Online-Escape-Game zum richtigen Verhalten im Brandfall sowie je zehn Spiele von GamesforCrowds und Gaming Couch.

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
Die Umstellung nach dem Beta-Test war der aufwendigste Teil des Projekts: Alles, was nicht spezifisch zu Wassermarsch gehört, musste heraus: MainScreen, Device Screen, QR-Verbindung, Session-Handling, Scoring, Timer, Leaderboard, Phasenwechsel.

Was übrig blieb, war Wassermarsch als reines Spielmodul. Und daneben ein Framework, das alles andere übernimmt.

{{</section>}}

{{<section title="Phase 7: Zwei Stränge">}}
Danach lief die Arbeit zweigleisig: Auf der einen Seite wurden drei weitere Spiele entwickelt, um die Funktionsweise des Framworks zu valdieren. Auf der anderen Seite wurde Wassermarsch weiterentwickelt. Für Version v0.0.2 wurde eine richtige Map sowie weitere Assets erstellt. Zudem wurden Animationen für Punktgewinn und Punktverlust sowie Sterne bei Kollisionen hizugefügt.

{{</section>}}

{{<section title="Phase 8: Validierung">}}
Beide Stränge liefen in der Validierung zusammen: das Framework über die drei neuen Spiele, das Spiel über die Nutzertests. Details auf der Testing-Seite.

{{</section>}}
