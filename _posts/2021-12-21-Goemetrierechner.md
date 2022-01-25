---
Layout: post
Title: Gruppenarneit Geometrierechner
---

# Gruppenarbeit Geometrierechner

## Aufgabenstellung

An der BBB hatten wir den Auftrag mit Windows Forms einen Geometrierechner zu programmieren. Bei diesem Programm sollen verschiedene Formen und die Art der Berechnung ausgewählt werden können. Nach der Berechnung soll eine Skizze der Form gezeigt werden.

### Ziele:
1. Das Programm kann Fläche, Ufang und Volumen verschiedener Formen berechnen können.
2. Die Eingaben werden geprüft und bei falschen erscheint ein Warnfenster.
3. Nach der Berechnung erscheint ein neues Form mit der Lösung und einer Skizze.

## Code
Für den Anfang möchte ich hier den Teil meines Codes Zeigen, der die Variabeln des Motherforms öffentlich macht und für die anderen Formen zu verfügung stellt. Denn diese Funktion gehört zu den Herzstücken des Programms und ich das neu gelernt habe.
Als voraussetzung gilt, dass die Beiden Forms schon verbunden sind!

Im Motherform müssen alle Variabeln, die auch im zweiten Form Verwendet werden wollen, als public initialisiert werden.
```
   public partial class Form1 : Form
    {
        public double flächekreis;
        public double umfangkreis;
        public Form1 form1;
```

Als nächster Schritt müssen auch im zweiten Form Variabeln initialisiert werden, in unserem Fall haben sie den selben Namen.
Dann wird ihnen mit folgendem Code gesagt das sie das selbe sind.
```
public FormKreis(Form1 form1)
        {
            InitializeComponent();
            this.form1 = form1;
            this.flächekreis = form1.flächekreis;
            this.umfangkreis = form1.umfangkreis;
        }
```

## Bild
Eine der Anforderungen war, das mithilfe einer Dropdownliste die Form gewählt werden kann. Eine Andere war, das eine Skizze erscheint.

[![code](https://snipboard.io/Je17G0.jpg)](https://snipboard.io/Je17G0.jpg)

[![code](https://snipboard.io/BXUp0J.jpg)](https://snipboard.io/BXUp0J.jpg)
## Video

Zusätzlich möchte ich noch ein [Video](https://youtu.be/DjodcIXTTMc) des Programms zeigen.

## Reflexion und Verifikation

### Reflexion:
Unser Programm ist Abgeschlossen mit allen Anforderungen und Funktioniert einwandfrei. 
Ich habe neu gelernt wie man mit Windows Forms programmiert und verschiedene Forms verbindet. 
Am Anfang hatten wir ein paar Probleme mit dem Zusammenfügen des Codes, da wir verschiedene Forms gemacht hatten und keiner einen plan hatte wie man das zusammefügt. Doch zu diesem Problem gab es eine Enführung von unserem Lehrer.

Verbesserungen: Wir hätten uns im gesamten besser aufteilen können, wir waren häufig zu zweit an einem PC beschäftigt was nicht immer effizient war.

### Verifikation:
Meine Ziele habe ich erreicht:

Ziel 1: ✔ Das Programm kann Fläche, Ufang und Volumen verschiedener Formen berechnen können.

Ziel 2: ✔ Die Eingaben werden geprüft und bei falschen erscheint ein Warnfenster.

Ziel 3: ✔ Nach der Berechnung erscheint ein neues Form mit der Lösung und einer Skizze.
