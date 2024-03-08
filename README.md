# BS-RA

## 1.Rechnerarchitektur

<details>
  <summary>1. Definieren Sie den Begriff Rechnerarchitektur!</summary>
  Rechnerarchitektur iist ein Teilgebiet der Technischen Informatik, das sich mit der Beschreibung von Rechnern und elektrischer Bauteile und deren Verbindung beschäftigt.

</details>
<br>

<details>
  <summary>2. Was versteht man unter der äußeren Sicht auf die Architektur eines Computers?</summary>


</details>
<br>

<details>
  <summary>3. Defnieren Sie den Begriff Parallelität!</summary>


</details>
<br>

<details>
  <summary>4. Was ist ein ASIC? Welche Arten von ASICs kennen Sie? Nennen Sie einen Vorteil und einen
Nachteil eines ASICs!</summary>


</details>
<br>

<details>
  <summary>5. Defnieren Sie den Begriff Parallelität!</summary>


</details>
<br>

<details>
  <summary>6. Welche Funktionseinheiten vereint ein Microcontroller auf einem Chip?</summary>


</details>
<br>

## 2.AD-Wandlung
<details>
  <summary>1. Beschreiben Sie den Aufbau und die Funktionsweise eines Flashwandlers! Welche Eigenschaften
hat dieser?</summary>


</details>
<br>

<details>
  <summary>2. Mittels AD-Wandler mit sukzessiver Approximation wird eine Spannung von 1,8 V quantisiert.
Die Referenzspannung beträgt 4 V. Geben Sie das binäre Ergebnis der Messung an, geben Sie
dabei den Rechenweg an! (5 Bits bieten hier eine ausreichende Genauigkeit)</summary>


</details>
<br>

## 3.Atmel AtMega328p
<details>
  <summary>1. Nennen Sie die 3 Bedingungen die für das Auslösen eines Interrupts notwendig sind!</summary>


</details>
<br>

<details>
  <summary>2. Über welche 3 Register wird ein GPIO-Pin gesteuert. Erläutern Sie die entsprechenden Funktionen!</summary>


</details>
<br>

<details>
  <summary>3. Nennen Sie 3 Peripheriebaugruppen in einem AtMega!</summary>


</details>
<br>

## 4. Portprogrammierung

## 5. Timer-Konfiguration

## 6. Prozesse

<details>
  <summary>1. Was ist ein Prozess?</summary>


</details>
<br>

<details>
  <summary>2. Wir betrachten das 7-Zustands-Prozessmodell und treffen folgende Annahme: Ein Prozess befindet sich im Zustand running. Unter welchen Umständen wird dieser Prozess in seine möglichen
Folgezustände überführt?</summary>


</details>
<br>

<details>
  <summary>3. Klären Sie die Begriffe "aktivieren" und "suspendieren" hinsichtlich des 7-Zustands-Prozessmodells!
</summary>


</details>
<br>

## 7. User-Mode und Kernel-Mode

<details>
  <summary>1. Klären Sie die Begriffe User-Mode und Kernel-Mode!</summary>


</details>
<br>

<details>
  <summary>2. Nennen Sie die typischen Aufgaben des Kernels!</summary>


</details>
<br>

<details>
  <summary>3. Muss für folgende Operationen ein System Call durchgeführt werden? Begründen Sie Ihre Antworten!(4)
</summary>
I) Das Deklarieren einer Zählvariable mit doppelter Genauigkeit,
II) Das Sperren eines Interrupts,
III) Das Erzeugen eines Prozesses,
IV) Die Änderung einer globalen Programmvariable.

</details>
<br>

## 8. Interprozesskommunikaton

<details>
  <summary>Die Semaphore ist ein bedeutendes Mittel der Interprozesskommunikation. Sie wird vorwiegend zur
Prozesssynchronisation genutzt.</summary>
a) Welche Arten von Semaphoren kennen Sie?

  
b) Welche atomare Operationen sind für Semaphoren zulässig? Erläutern Sie dabei das Wort "atomar"!


c) Nennen Sie ein Beispiel, bei dem es nicht ausreicht einen Semaphor als *{0,1}-Datenstruktur* zu
initialisieren! Wie könnte man die Implementierung dahingehend ändern, dass Semaphoren für Ihr
Beispiel als Mittel der Interprozesskommunikation funktionieren?
</details>
<br>

## 9. Buddy-Systeme

<details>
  <summary>Ihr Hauptspeicher sei 1 Mbyte groß.
</summary>
a) Erläutern Sie den Buddy-Algorithmus (Anwenden des Buddy-Algorithmus am Beispiel) einer Speicherpartitionierung anhand des Beispiels: Zuerst betritt Prozess A (320kB) in das System ein, danach betritt Prozess B das System (69kB). Anschließend tritt Prozess C (127 kB) in das System
ein. Im Anschluss daran verlässt Prozess B das System. Anschließend soll Prozess C das System
ebenfalls verlassen. Abschlieÿend tritt Prozess D (240 kB) in das System ein.
  
b) Erläutern Sie die Effekte "externe Fragmentierung" und "interne Fragmentierung"! In welchen Systemen der Speicherverwaltung kommen diese im Allgemeinen vor?

c) Kennzeichnen Sie innerhalb Ihrer Lösung je ein externes und ein internes Fragment!


</details>
<br>

## 10. Replacement-Strategien

<details>
  <summary>Falls bei der Benutzung von virtuellem Speicher Zugrisfehler auftreten, müssen Seiten im Hauptspeicher durch Ersetzungsregeln (Replacement-Policy) ersetzt werden. Wir betrachten die Aufteilung eines
virtuellen Speichers in Pages (Seiten) und des Hauptspeichers in Kacheln (Frames). Ein Prozess fordert
folgende Seiten in zeitlicher Reihenfolge an: {1,5,1,3,6,1,2,6,5,1,6,1}. Erläutern Sie an diesem Beispiel
die Anwendung der Ersetzungsregeln, wenn der Hauptspeicher 3 Frames besitzt, nach:</summary>
a) Optimalstrategie (Longest Forward Distance (LFD))

b) Clock Strategy

c) Kennzeichnen Sie die entstehenden Seitenfehler!

</details>
<br>

## 11. Paging-Systeme

<details>
  <summary>Ein Paging-System hat einen maximalen virtuellen Speicher von 32 MB. Die Seitengröÿe beträgt 1024
Byte und die Seitentabelle eines aktiven Prozesses hat folgende Zuordnung:</summary>
  
![Bild-Seitennummer.png
](https://github.com/ValentinBuettner/BS-RA/blob/main/Seitennummer.png?raw=true)

  
a) Welche virtuelle Adresse wird mit der physischen Adresse 4500 abgebildet? 
b) Berechnen Sie die physische Anfangsadresse des Speicherbereichs der Seite des virtuellen Speichers
mit der Nummer 3! 

</details>
<br>
