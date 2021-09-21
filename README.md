# nanoreseau

Schema pour la carte nanoreseau Thomson


Résistances 1/4w +/-5%
```
R1, R2, R3, R4, R5, R7, R10 : 4.7K
R6: 1K
R8, R9: 27K
```

Circuits intégrés
```
IC1: 74LS157
IC2: 74LS09
IC3,IC4: 75176 montés sur support (important, doivent être remplaçables)
IC5: 74LS123
IC6: 74LS393
IC7: 74LS14
IC8: 74LS04
IC9: 74LS11
IC10,IC11: 74LS138
IC12: 74LS139
IC13: 74LS245 monté sur support
IC14: D7201C (Nec) monté sur support
IC15: D8253C-5 (Nec) ou 8253-5 (AMD) monté sur support
```


Condensateurs
```
C1, C8, C12: Tantale "Goutte" 4.7uF 35V
C3: céramique 10pF 25V
C4: céramique 22nF 25V
C2, C5, C6: céramique 100nF 50V
C7: céramique 10nF 25V
C9, C10, C11, C13, C14, C15: céramique 22nF 25V
C16: electrolytique 10uF 25V
```


Typical DMA Channel Assignments

| Channel 	      | Assignment                                                   |
| ----------------|------------------------------------------------------------- |
| DRQ 0 ( 8-bit) 	| User Available (Business audio)                              |
| DRQ 1 ( 8-bit) 	| User Available (Business audio or LAN)                       |
| DRQ 2 ( 8-bit) 	| DISKETTE DRIVE                                               |
| DRQ 3 ( 8-bit) 	| User Available (Business audio, LPTx - ECP or EPP mode)      |
| DRQ 4 (16-bit) 	| RESERVED (cascade channel) Memory-(DMA)-REFRESH              |
| DRQ 5 (16-bit) 	| User Available (ISA bus)                                     |
| DRQ 6 (16-bit) 	|User Available (ISA bus)                                      |
| DRQ 7 (16-bit) 	| User Available (ISA bus / 6384 P60/D Hard Disk)              |


 Typical IRQ Assignments


| Interrupt Ctrl #1 | Interrupt Ctrl #2 | Assignment                                |	8-bit 16-bit type |
|-------------------|-------------------|--------------------------------------------|----|                       
| SMI 	  	        |                   | System/Power Management IRQ                |	-- |
| NMI 	  	        |                   | Parity Error or I/O Channel check          |	-- |
| IRQ 0 	  	      |                   | Interval Timer 	                           | -- |
| IRQ 1 	  	      |                   | Keyboard bffr.-full                        |	-- |
| IRQ 2 	  	      |                   | Cascade IRQ-req. (IRQ-8 to IRQ-15)         |	-- |
|                   | IRQ 8             | Real Time Clock 	                         | -- |
|                   | IRQ 9             | Redirect Cascade to IRQ 2 (User Available) | 8/16 |
|                   | IRQ 10            | User Available                             | 16 |
|                   | IRQ 11            | User Available (2137-SL A - USB) 	         | 16 |
|                   | IRQ 12            | Auxiliary device (Mouse) (User Available)  | 16 |
|                   | IRQ 13            | Math Coprocessor exception 	               | -- |
|                   | IRQ 14            | Hard Disk (Primary IDE)                    | 16 |
|                   | IRQ 15            | Secondary IDE (User Available)<br> Used by NOVELL, if installed. |16 |
| IRQ 3             |                   | COM2: 	                                   | 8/16 |
| IRQ 4             |                   | COM1: 	                                   | 8/16 |
| IRQ 5             |                   | LPT2: / Sound Card User Available 	       | 8/16 |
| IRQ 6             |                   | Diskette drive controller 	               | 8/16 |
| IRQ 7             |                   | LPT1: (User Available, if shareable) 	     | 8/16 |

Doc sur l'ISA :

http://wearcam.org/ece385/lecture6/isa.htm

Plus bas niveau, et très intéressant

http://ancrobot.free.fr/fiches/pdf/index(5).pdf

Intéressant sur le fonctionnement de l'ISA

https://www.robots.ox.ac.uk/~adutta/blog/interfacing-with-the-isa-bus.html

A voir : 

http://5lair.free.fr/PCB/
