---
Layout: post
Title: Robocode Taktik
---

# Roboter mit Robocode


## Aufgabenstellung

An der BBB hatte ich den Auftrag bekommen mit Robocode einen Roboter zu programmieren. Robocode ist eine Applikation auf der jeder mit Java einen Kampfroboter erstellen kann. Diese Roboter kämpfen dann in einer Arena. Da es bei so einem Kampf wichtig ist eine Strategie zu haben, möchte ich meine hier erklären.

### Ziele:
1. Ich erkläre die Strategie meines Roboters.
2. Ich verdeutliche die Strategie mit einem Video.

## Inhalt Nr.1
Meine Taktik bei diesem Roboter war, das er sich als erstes richtung Wand begibt. Wenn er bei der Wand ist sucht er denn Ecken, der am nächsten bei ihm ist. Er geht in diesen Ecken und wartet erst mal dort. Wenn nur noch eine gewisse Anzahl Spier auf dem Feld sind (bei mir unter 15), dann fängt er wieder an sich zu bewegen. Er fährt immer am gleichen Rand hin und her.
## Inhalt Nr.2
Im Code sieht diese Taktik so aus. 

Hier wird die nächste Wand auf der X-Achse gesucht
```
int position;
public void run() {

    if (robotX > fieldWidth / 2) {
        turnTo(90);
        position = 1;
    } else {
        turnTo(-90);
        position = 3;
    }
}
```
Hier fährt er vor und dreht immer wieder zum scannen. Ausser er steht in der Ecke, dann dreht er immer nur um 90° hin und her.
```
int scanStart = -1;
while (true) {
    ahead(100);

    if (scanStart == -1) {
        turnGunLeft(360);
    } else {
        turnGunTo(scanStart);
        turnGunLeft(90);
    }

    out.println(position);

    switch (position) {
        case 1:
            scanStart = -90;
            break;
        case 2:
            scanStart = 0;
            break;
        case 3:
            scanStart = 180;
            break;
        case 4:
            scanStart = 90;
            break;
    }
}
```
Hier wird die Aktion etschieden wenn er in eine Wand fährt. Sind noch mer als 14 Spieler dabei dreht er sich zur nächsten Ecke und führt wieder das normale verhalten aus, heisst richtung Wand vorwärtsfahren und drehen.
Falls es weniger als 15 sind fährt er an der Wand hin und her.

```
public void onHitWall() {
    if (others > 14) {
        if (robotY > fieldHeight / 2) {
            turnTo(0);
        } else {
            turnTo(180);
            if (position == 1 || position == 3) {
                position += 1;
            }
        }
    }
    if (others < 15) {
        if (robotX > fieldWidth / 2) {
            turnTo(-90);
            ahead(100);

        } else {
            turnTo(90);
            ahead(100);

        }
    }
}
```

## Inhalt Nr.3

Zusätzlich möchte ich noch ein [Video](https://youtu.be/So2-RSsF7Xc) zeigen um die Taktik zu verdeutlichen. Im Video habe ich sie auf weniger Spieler angepasst damit die Partie schneller geht.

## Reflexion und Verifikation

### Reflexion:
Ich habe einen fertigen Roboter mit einer guten Taktik und kann diese Leuten erklären die keine Ahnung haben.
Probleme gab es bei diesem Projekt keine.

Verbesserung: Ich sollte das nächste mal wenn ich etwas ohne Integrierte Entwicklungsumgebung programmiere von Anfang an den Code sauber einrücken.

### Verifikation:
Meine Ziele habe ich erreicht:

Ziel 1: ✔ Ich erkläre die Strategie meines Roboters.
Ziel 2: ✔ Ich verdeutliche die Strategie mit einem Video.
