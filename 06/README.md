# Nedelja 6 - Variant Calling

- DNA Sekvenciranje - 
    - izlaz FASTQ fajlovi -- 4 fajla za svaki
    - fredova skala 
    - koji kvalitet baza je prihvatljiv kod sekvenciranja? --- 90% je neka minimala
        - kabidz = koliko puta je neka pozicija sekvencirana => jednom u 100 puta ce se desiti jedna greska.
    - ridovi su dugacki 150-200 sekvenci, tako opada kvalitet baza
    - alingment - uporedjivanje sa referetnim genomom = 

### Varijante 
- predstavljaju odstupanje sekvenci od referentnog genoma
- uzroci nastanka ovih varijacija:
    - zbog cega moze da dodje do mutacija? -> zbog zracenja, zagadjenog vazduga... dolazi do greske repikacije
    - somaske(ispoljava se fizicki) i polne(prenose se sa generacije na generaciju) celije
        - u somatskim celijama dolazi do nastanka kancera

- delecije = fali neka sekvenca u genomu
- insertion = dodaju se neke sekvence u genomu
- inverzija = promena koja ne menja broj baza, ali se menja redosled u genomu
- translokacija = prenosenje genoma

- genomske varijante mogu da budu povezane sa specificnim nukleotidima
    - na kom hromozomu i na kojoj poziciji

- TRANSKRIPCIJA - kada nastaje informaciona RNA => protein 
    - nastaju svi RNA
    - samo se EXON-i prevode
    - EXOM-i svi koji se prevode u proteine 
    - uvek 3 nukleotida kodiraju jednu nukleo kiselinu
    - stop kodoni -> sa njima nastaje nefunkcionalni 
    - insertion/deletion -> nastaju indels
        - in frame - kada su deljivi sa 3 (1 aminu kiselinu kodiraju 3 nukleotida)
        - out of frame - kada stavimo 10 i ostane 1 koja pomeri citanje

- variant calling - razlike izmedju referetne sekvence i ridova
    - **KAVRIDZ** - broj ridova koji se mapira na jednom mestu!!! (zapamtiti)
    -  pileup format = 

- genom je diploidan  
    - 0/0 = homozigot - kad su ista slova
    - 0/1 = heterozigot - kada su razlicita slova
    - 1/1 = homozigot 
    - 1/2 = jedan alel sadrzi dve varijante ali nije ista referenca 

- idealno je da imamo isti kavridz = da isti broj ridova pokriva poziciju 
    - postoje regioni genoma koji se ne mogu sekvencirati, zbog toga kavridz nije isti 
    - tokom PCR-a = nikad se ne umnoze sve sekvence

- 
