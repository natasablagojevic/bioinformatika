# NORMALIZACIJA 

- analizira se velika kolicina podataka 
- transkripti - dobijen RNK molekul iz transkripcije 
- EGZONI 

- normalizaciju radimo kad god imamo eksperiment - bitno je da imamo veliku kolicinu uzoraka 
    - normalizacija svih uzoraka 
    - normalizacija izmedju uzoraka
        - kako bi rezultati bili realni = znaci ova dva tipa metoda treba da se uradi

- na ispitu:
    - normalizujemo na duzinu gena i na library size(dubina sekvenciranja)

- NITRONI, EGZONI 

- NA ISPITU: 
- MEJERI: 
    - **RPKM** =  dubina pa duzina
        - dubina sekvenciranja = broj ridova (ako je ista dubina sekvenciranja)
        - duzina = vrednosti delimo sa kilobazama 

    - **FPKM** = dubina pa duzina

    - **TPM**  = duzina pa dubina (najbolji)
        - bolji je, jer na kraju kada saberemo sve vrednosti imacemo iste vrednosti mecu uzorcima i tu nemamo varijacije

    - razlikuju se po redosledu normalizacije

- dajemo BAN fajlove za **RPKM**
    - kako sve moze da se poravna na referentni genom:
        - 1. alajnovanje 
        - 2. slajsovanje 
        - 3. transkripton - nema introne 
        - 4. 

- **BEETWEN-SAMPLES**
    - geni za delove celija koji su esecijalni 
    - ekstremiran istu u svakom uzorku 
    
    - **TMM** 
        - 

    - **DESeq**
        - za vecinu alata
        - koristi se za analizu dijerencijalne ekspresije 
        
    - minimum 3 sempla po uzorku, ali treba ih biti vise jer se neki odbacuju 

- **DIFERENCIJALNA EKSPRESIJA GENA** = proces koji pravi proteine putem transkripcije i translacije 
    - problem: jer dobijamo lazno pozitivne
    - p-vrednost = koja je sansa da se slucajno izvuce ta vrednost
        - imamo normalnu raspodelu - u repovima se nalazi sve sto je statisticki znacajno 

- MULTIPLE TESTING CORRETCION 
    - ne moze da se bazira na samo jednom genu!!! 
    - 
    1. Benjamini-Hochberg = skoro uvek je bolja (bioloski proces je uvek regulisan velikim brojem gena)
    2. Bonferroni correction = 