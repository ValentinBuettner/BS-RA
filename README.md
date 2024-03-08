# BS-RA

## 1.Rechnerarchitektur

<details>
  <summary>1. Definieren Sie den Begriff Rechnerarchitektur!</summary>
  
  * Rechnerarchitektur ist ein Teilgebiet der technischen Informatik und befasst sich mit der Beschreibung von Rechnern aus vorgefertigten Bausteinen und der Verbindung (Organisation) dieser Bausteine

</details>
<br>

<details>
  <summary>2. Was versteht man unter der äußeren Sicht auf die Architektur eines Computers?</summary>
  
  * Die Sicht des Anwenders (auch Programmierer) auf das System. Innere Sicht wäre die Sicht des Ingenieurs.

</details>
<br>

<details>
  <summary>3. Defnieren Sie den Begriff Parallelität!</summary>
  
  * Abarbeitung von mehreren Tasks
    * richtige Parallelität: mehrere Verarbeitungseinheiten
    * pseudo-Parallelität: nur eine, Einteilung in Zeitscheiben
  
      
</details>
<br>

<details>
  <summary>4. Was ist ein ASIC? Welche Arten von ASICs kennen Sie? Nennen Sie einen Vorteil und einen
Nachteil eines ASICs!</summary>
  
* Application specific integrated circuit: Ein für die Anwendung spezialisiert entwickelter Schaltkreis.
* vollständig kundenspezifisch (Transistorebene) und Makroebene (Gatter, FlipFlops)
* Vorteil: sehr effizient für seine Aufgabe, Nachteil: teuer, nur genau eine Funktion


</details>
<br>

<details>
  <summary>5. Definieren Sie eingebettete Systeme!</summary>
  
* Ein ES ist ein informationsverarbeitendes System, welches in ein übergeordnetes Produkt
integriert ist. Das Gesamtprodukt dient nicht vordergründig der Informationsverarbeitung.
Die Informationsverarbeitung ist von auÿen nicht wahrnehmbar.

</details>
<br>

<details>
  <summary>6. Welche Funktionseinheiten vereint ein Microcontroller auf einem Chip?</summary>
  
* CPU, Speicher, Peripherie (mindestens I/O)

</details>
<br>

<details>
  <summary>7. Welche besonderen Eigenschaften weisen Embedded Systems hinsichtlich der Effizienz auf?</summary>
  
* Preis, Laufzeit-Effzienz, Energie, Codegröße, Gewicht, Programmierbarkeit
</details>
<br>

<details>
  <summary>8. Was ist aktives Warten?</summary>
  
* Die CPU wird angewiesen Kommandos mit dem Inhalt "no operation" durchzuführen um Zeit zu überbrücken.
</details>
<br>

<details>
  <summary>9. Erläutern Sie die Funktionsweise eines Flash-DAC! (die anderen Varianten...da können Sie sich
die Fragen aus dieser Frage vererben...)</summary>
  
* Am Besten das Schaltbild erklären...
</details>
<br>

<details>
  <summary>10. Ein 3-Bit-Flashwandler gibt das Wort 011 aus. Die Referenzspannung beträgt 4V. Welche Spannung wurde gemessen?</summary>
  
* 1,5V
</details>
<br>

<details>
  <summary>11. Ein DAC mit sukzessiver Approximation gibt das Wort 01101 aus. Die Referenzspannung beträgt
4V. Welche Spannung wurde gemessen?</summary>
  
* 1,625V
</details>
<br>

<details>
  <summary>12. Welche Voraussetzungen müssen erfüllt sein, damit ein Interrupt ausgelöst wird?</summary>
  
* globale Freigabe der Interrupts, lokales Bit des Interrupts ist aktiviert, das auslösende Ereignis tritt ein
</details>
<br>

<details>
  <summary>13. Begründen Sie Ihre Aussage ob der AtTiny 261A in Harvard- oder in von-Neumann-Architektur
aufgebaut ist!</summary>
  
* Harvard, da verschiedene Speicher über verschiedene Busse an die CPU angebunden sind
</details>
<br>

<details>
  <summary>14. Welche grundsätzlichen Verdrahtungsmöglichkeiten bestehen bei der SPI-Schnittstelle? Erläutern
Sie diese! Eigenschaften?</summary>
  
* sternförmig (parallel): Clk, MOSI und MISO sind parallel zu allen Slaves (immer MOSI an
MOSI, MISO an MISO), jeder Slave hat eigene CS-Leitung, +:schnell, -: Verdrahtungsaufwand hoch
* kaskadiert (daisy chain): Clk parallel zu allen Slaves, CS parallel an alle Slaves, MOSI von
Master zu Slave 1 MOSI, Slave 1 MISO zu Slave 2 MOSI...nach letztem Slave zurück zu
Master MISO; +: langsam bei vielen Slaves, Verdrahtungsaufwand geringer
</details>
<br>

<details>
  <summary>15. Welche Klassifizierungsmöglichkeiten existieren bei Schnittstellen?
</summary>
  
* near range 
* short range 
* medium range 
* wide range
</details>
<br>

<details>
  <summary>16. Definieren Sie Schnittstelle!
</summary>
  
* von Rechnerbaugruppen gemeinsam genutzte elektrische Abgrenzung zum Austausch von Informationen
* Verbindungsstelle zwischen Funktionseinheiten eines Datenverarbeitungs- oder -übertragungssystems, an der der Austausch von Daten oder Steuersignalen erfolgt
</details>
<br>

<details>
  <summary>17. Welche Unterschiede bestehen bei der Datenübertragung mittels UART bei TTL-UART und RS-232?</summary>
  
* TTL: logisch 1: 5V, logisch 0: 0V
* RS-232: logisch 1: -9..15V, logisch 0: +9...15V
</details>
<br>

<details>
  <summary>18. Was bedeutet "interne Schnittstelle"? Nennen Sie Beispiele für interne Schnittstellen!</summary>
  
* Schnittstelle innerhalb eines Geräts, Bsp.: I2C, SPI, ...
</details>
<br>

<details>
  <summary>19. Zeichnen Sie den allgemeinen Aufbau eines Timers!</summary>
  
* Funktionsblöcke mit: Taktquelle -> Vorteiler -> Zähler -> Vergleichslogik -> Ausgabe
</details>
<br>

## 2.Betriebssysteme

<details>
  <summary>1. Was ist ein Betriebssystem und was sind dessen Aufgaben?</summary>
  
* Ansammlung von Programmen, die
  * die Bereitstellung vorhandener Hardware-Ressourcen für die Anwendungsprogramme gewährleistet unter
  * der Berücksichtigung der Kriterien Fairness und Ezienz,
  * so dass keine direkte Kommunikation der Anwenderprogramme mit der Hardware stattndet.
* Aufgaben:
   * Verwaltung der Betriebsmittel (Ressourcen) - CPU, Speicher ...
   * Koordinierung der Prozesse
   * Verschleierung der Komplexität der Hardware dem Anwender gegenüber
   * Bereitstellung einer API (Application Program Interface)
   * Bereitstellung einer (ergonomischen) Benutzerschnittstelle
   * Schutz der Informationen vor unbefugten Zugriff
</details>
<br>

<details>
  <summary>2. Erläutern Sie an einem selbst gewählten Beispiel, wie ein Betriebssystem die Komplexität der Hardware dem Anwender gegenüber verbirgt (virtualisiert)</summary>
  
* 
</details>
<br>

<details>
  <summary>3. Was ist ein Systemaufruf? Gehen Sie bei der Erklärung auf die Begriffe **User-Mode** und **Kernel-Mode** ein! </summary>
  
* Aufrufmechanismus für das Angebot von Diensten durch das Betriebssystem
* der Syscall ist dabei ist eine synchrone Programmunterbrechung
* User Mode: Modus des Prozessors
* Kernel Mode: privilegierterer Modus des Prozessors, d.h. erweiterter Befehlssatz und erweiterte Rechte für den Zugriff in bestimmte Speicherregionen, in die im User Mode nicht zugegriffen werden darf. Grund für die Unterscheidung sind Sicherheitsaspekte
</details>
<br>

<details>
  <summary>4. Welche Funktionen sind im user mode oder im kernel mode eines Prozessors zulässig?</summary>
  
* Sperren eines Interrupts: Kernel Mode, da Support-Funktion eine typische Kernel-Aufgabe
ist
* Verschieben eines Bits um 4 Stellen nach links: User Mode
* Speichern des Maschinen Status Wortes: Kernel Mode, Änderung hätte Auswirkung auf den Betrieb des Rechners, Supportfunktion
* Berechnung der Quadratwurzel einer Gleitkommazahl mit doppelter Genauigkeit: User Mode
* Laden der eektiven Adresse eines Operanden in ein Register: User Mode
* Aufruf des **HLT (HALT)** Befehls: Kernel Mode, Zugri nur über API, HLT stoppt den Hauptprozessor und kann somit in die Prozessverwaltung eingreifen (Kernelaufgabe: Betriebsmittelverwaltung und Prozessverwaltung)

</details>
<br>

<details>
  <summary>5. Erklären Sie den Unterschied zwischen den Begriffen Programm und Prozess? </summary>
  
* Prozess: Programm im Zustand der Ausführung, oder auch Ausführungseinheit eines Programms. Der Prozess beinhaltet den Program Counter und aktuelle Werte der Register und Variablen.
* Programm: eine Folge von Anweisungen, mit denen man mittels Computer Funktionen oder Aufgaben zur Lösung von Problemen bearbeiten kann. Ein Programm kann mehrere Prozesse beinhalten.
</details>
<br>

<details>
  <summary>6. Begründen Sie, warum es kein Zustandsübergang von ready zu blocked im 5-Zustands-Prozessmodell gibt!
</summary>
  
* Zustandsübergang von ready zu blocked nie möglich, da eine Blockierung immer nur während der Ausführung des Prozesses (im Zustand running) festgestellt werden kann.
</details>
<br>

<details>
  <summary>7. Zeichnen und beschriften Sie das 7-Zustands-Prozessmodell!</summary>
  
  
* ![image](https://github.com/ValentinBuettner/BS-RA/assets/157825537/af738249-7fb7-43af-b8b8-b7ca3584c077)

</details>
<br>

<details>
  <summary>8. Was sind Threads und welcher Arten werden unterschieden?</summary>
  
* Threads: lightweight processes, Ausführungseinheit, welche zu einem Prozess gehört, aber selber keine Ressourcen besitzt
* User level threads und kernel level threads
</details>
<br>

<details>
  <summary>9.Begründen Sie, warum der Prozesswechsel aufwendiger als ein Threadwechsel ist?</summary>
  
* Threadwechsel benötigt kein Umschalten in den Kernel Mode (ULT)
* PCB muss bei Threadwechsel nicht aktualisiert werden
* Es muss nicht der komplette Prozesskontext gesichert werden
* Scheduling bei ULT bedingt kein Scheduling des Prozesses
</details>
<br>

<details>
  <summary>10.Welche Interprozesskommunikationsmittel kennen Sie? </summary>
  
* Dateien, Pipes, Sockets, Shared Memory, Semaphoren, Message Queues, Signale
</details>
<br>

<details>
  <summary>11. Welche Arten von Semaphoren kennen Sie, warum gibt es verschiedene Arten? Nennen Sie die
möglichen Operationen von Semaphoren </summary>
  
* binäre Semaphoren
* Zählsemaphoren
</details>
<br>

<details>
  <summary>12. Was ist ein Socket und welche Arten werden unterschieden?</summary>
  
* Socket ist das einzige Interprozesskommunikationsmittel, welches über Rechnergrenzen hinaus genutzt werden kann
* Stream Socket und Datagram Socket

</details>
<br>

<details>
  <summary>13. Was ist eine Race condition?</summary>
  
* zwei oder mehrere Prozesse nutzen gemeinsame Daten oder greifen auf eine gemeinsam genutzte Ressource zu und das Ergebnis hängt vom Prozessfortschritt ab
</details>
<br>

<details>
  <summary>14. Nennen Sie die Anforderungen an eine Speicherverwaltung</summary>
  
* Relocation (Wiederfinden)
* Protection (Schutz)
* Sharing (Teilen/Aufteilen)
* Logical Organization
* Physical Organization
</details>
<br>

<details>
  <summary>15. Erklären Sie den Buddy-Algorithmus zur Speicherpartitionierung bei 1 MByte verfügbaren Hauptspeicher! Dabei treten die Prozesse in der Reihenfolge ihrer Nennung nacheinander in das System
ein: Prozess A mit 115 KByte, Prozess B mit 240 KByte, Prozess C mit 100 KByte und Prozess D
mit 210 KByte. Der Prozess D und danach der Prozess A verlassen das System und die Prozesse
E mit 400 KByte gefolgt von Prozess F mit 120 KByte betreten das System. </summary>

  
* ![image](https://github.com/ValentinBuettner/BS-RA/assets/157825537/5c5db699-8e6c-4c38-89bb-da90031dfb51)

</details>
<br>

<details>
  <summary>16. Warum ist die Longest-Forward-Distance - Strategie in heutigen Betriebssystemen nicht implementiert?</summary>
  
* Bei LFD werden zukünftig aufgerufene Speicherzugriffe ausgewertet, allerdings: wir können nicht in die Zukunft sehen
</details>
<br>

<details>
  <summary>17. Ein Prozess habe die Seitenanforderungen {2, 3, 2, 1, 5, 2, 4, 6, 3, 2, 5, 2, 4, 1, 3, 6}. Der Hauptspeicher besteht aus vier Kacheln die zu Beginn nicht belegt sind. Berechnen Sie die Belegung desSpeichers mit LFD, LRU, Clock und FiFo! Wie viele Seitenfehler treten je Verfahren auf?
</summary>
  
* Verschiedene Algorithmen anschauen
</details>
<br>

<details>
  <summary>18. Was sind interne Fragmente und externe Fragmente? Wo entstehen diese?
</summary>
  
* Interne Fragmente entstehen bei statischer Partitionierung(z.B. bei Pagingsystemen). Ein
internes Fragment ist hierbei der nicht genutzte Speicherplatz innerhalb einer Partition.
(Bsp: Partition ist 128 K, aber der Prozess belegt hier nur 110 K, d.h. in dieser Partition
sind 18 K ungenutzer und nicht nutzbarer Speicher)
* Externe Fragmente entstehen bei dynamischer Partitionierung. Während der Laufzeit wird
Speicherplatz genutzt und auch wieder freigegeben. Die Gröÿe der Partitionen kann dann
jedoch nicht mehr verändert werden. Durch die Freigaben entstehen so, unter Umständen,
Partitionen welche zu klein für manche Prozesse sind und ungenutzt bleiben. Diese nennt
man Externe Fragmente.
* Bei Buddy-Systemen kommt es zu interner und externer Fragmentierung, da der BuddyAlgorithmus ein Kompromiss zwischen statischer und dynamischer Partitionierung ist
</details>
<br>

<details>
  <summary>19. Sie wollen bei einem Paging-System die virtuelle Adresse aus der physischen Adresse berechnen. Wie gehen Sie vor?</summary>
  
* Seitenrahmen und Oset berechnen
* zum Seitenrahmen zugehörige Seite aus der Seitenzuordnungstabelle ablesen
* virtuelle Adresse aus Seite und Oset berechnen
</details>
<br>

<details>
  <summary>20. Erklären Sie die Funktion des Dispatchers und des Schedulers!</summary>
  
* Scheduler (Planer) sortiert Prozesse in Warteschlangen ein.
* Ein Dispatcher dient dazu, bei einem Kontextwechsel dem derzeit aktiven Prozess die CPU zu entziehen und anschließend dem nächsten Prozess die CPU zuzuteilen
</details>
<br>

<details>
  <summary>21.. Gegeben sind die Prozesse P1, P2, P3, P4, und P5. Die Prozesse betreten zu verschiedenen Zeiten
das System. Der Prozess P1 ist bei t1 = 0, P2 bei t2 = 2, P3 bei t3 = 4, P4 bei t4 = 6 und
P5 bei t5 = 8 bereit. Die Prozesse benötigen in der Reihenfolge ihrer Nennung 4, 9, 5, 7 und 3
Zeiteinheiten für die Bearbeitung. Geben Sie für die Prozesse die Ausführungsreihenfolge an für
RR mit einem Quantum von q=3, FCFS, SJF, SRPT.</summary>
  
* 
</details>
<br>

<details>
  <summary>22. Welche Effekte treten auf, wenn man bei der Verwendung von Round Robin das Quantum zu groß bzw. zu klein wählt?</summary>
  
* zu kleines Quantum: Overhead entsteht durch übermäÿig viele Kontextwechsel (häuges Dispatching), Zeitverschwendung.
* zu großes Quantum: Strategie nähert sich FCFS an und erreicht FCFS wenn Quantum gleich der längsten Bearbeitungsdauer
</details>
<br>

<details>
  <summary>23. Welche Ziele werden an das Scheduling eines BS gestellt?</summary>
  
* CPU-Utilisation: Möglichst hohe CPU-Auslastung
* High Throughput: Hoher Durchsatz (hohe Zahl Jobs pro ZE)
* Policy Enforcement: Durchsetzung der Systemstrategien
* Fairness: Keine Sonderbehandlung von Jobs
* Low Turnaround Time: Niedrige Ausführungszeit (Zeitspanne von Jobbeginn bis Jobende)
* Low Waiting Time: Niedrige Wartezeit (Schedulerstrategie beschränkt sich auf Minimierung
der Wartezeit in der ?ready? ?Liste
* Low Response Time: Niedrige Antwortzeit (Zeit zwischen interaktiver Eingabe und Ausgabe
der Antworten auf dem Ausgabegerät sollte kurz sein)
</details>
<br>


# Alte Klausuren
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
* ADC, Watchdog-Timer, Timer, Komparator

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
