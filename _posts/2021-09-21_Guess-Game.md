---
Layout: post
Title: Random-Number guessing Game
---

# Random number guessing Game


## Aufgabenstellung

An der BBB hatte ich den Auftrag bekommen in C# ein Random-Number guessing Game zu programmieren. Dieses Programm soll eine zufällige Zahl zwisch 1 und 100 generieren, die geheim gehalten wird und eratet werdend kann. Je nach Antwort wird ein Tipp ausgegeben.

### Ziele:
1. Ich kann eine zufällige Zahl generieren.
2. Ich kann Eingaben testen lassen und darauf antworten.
3. Das Spiel ist bedienerfreundlich.

## Inhalt Nr.1
Für den Anfang möchte ich hier den Teil meines Codes Zeigen der eine Zufällige Zahl generiert und die Eingaben prüft. Da diese Funktion das Herzstück des Programms darstellt und ich das neu gelernt habe.
```
int number = new Random().Next(1, 101);

```

```
   }
   else
   {
        if (guessconvert < number)
      Console.WriteLine("try a bigger number:");
        Console.Beep();

        if (guessconvert > number)
      Console.WriteLine("Try a smaller number:");
       Console.Beep();
   
       guess = Console.ReadLine();
      guessconvert = Convert.ToInt32(guess);                            
       tries = tries + 1;
     }
```

## Inhalt Nr.2
Als eigene Anforderung habe ich mir auch vorgenommen neben den Tipps bei den Versuchen eine Grafische Rückgabe zu programmieren. 

[![code](https://snipboard.io/ZJj7R9.jpg)](https://snipboard.io/ZJj7R9.jpg)
## Inhalt Nr.3

Zusätzlich möchte ich noch ein [Video](https://www.youtube.com/watch?v=bglrcrPmM8Q&ab_channel=AmonBurgherr) vom Gameplay zeigen.

## Reflexion und Verifikation

### Reflexion:
Mein Programm ist Abgeschlossen mit allen Anforderungen und Funktioniert, ich habe verschiedene neue Funktionen auf Visual Studio kennengelernt.

Verbesserungen: Ich sollte nächstes mal mehr optionale Ziele planen, falls ich schneller fertig bin als gedacht.

### Verifikation:
Meine Ziele habe ich erreicht:

Ziel 1: ✔ Ich kann eine zufällige Zahl generieren.
Ziel 2: ✔ Ich kann Eingaben testen lassen und darauf antworten.
Ziel 3: ✔ Das Spiel ist bedienerfreundlich.

