```mermaid
flowchart TD

start@{"shape":"circle",  "label": "Mulai"}
b@{"shape":"lean-l",  "label": "Input: Angka"}
c@{"shape":"diamond",  "label": "Angka !== 0"}
d@{"shape":"lean-l",  "label": "Output: #quot;Angka Tidak Valid#quot;"}
e@{"shape":"diamond",  "label": "Angka % 2 === 0"}
f@{"shape":"lean-l",  "label": "Output: #quot;Bilangan Ganjil#quot;"}
g@{"shape":"lean-l",  "label": "Output: #quot;Bilangan Genap#quot;"}
h@{"shape":"dbl-circ",  "label": "Selesai"}

start-->b-->c--True-->e
c--False-->d-->h
e--False-->f-->h
e--True-->g-->h
```