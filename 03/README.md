# Nedelja 3

<hr>

# Osnove sembli alajmenta - ljudski genomi

### PCR - polymerase chain reaction

- imamo 5 ciklusa
    1. Denaturation 
    2. Annealing 
    3. 
    4. 

- **Problem**:
    - DNK polimeraza nije idealna, ona nekako krene da zatvara drugi lanac i time krece da napravi gresku, pa se ona moze umnozavati ukoliko je na pocetku
    - moze se detektovati i resiti 

- **SEKVENCIRANJE** 
    - koriscenja u projektovanju ljudskog genoma 
    - illumina sekvenciranje kao najdominantnije 
        - kratki ridovi sa manje gresaka
        - sekvencira rid sa obe strane 



    - Oxford, Nano, BackBayIo
        - rid duzine milion 

    - **rid** = sekvenca nukleotida odredjene duzine
        - konketno nesto sto izalzi iz sekvencera, deo je genoma ali ne znamo gde je 

    - nas genom je duzine 3 milijarde parova


```
    ----
    ACCTGCA
    TGGACGT
         --


    - nesekvencira celu sekvencu, sekvencira prvih 4 karaktera prve sekvence i 2 karaktera iz druge sekvence
    - distanca izmedju ridova je 300 
    - govore nam gde se nalaze u nasem genomu
    - PND sekvenciranje
```

- **ANSEMBLING GENOMA (Genome Assembly)** - pokusaj da napravimo najduze sto mozemo sekvencu uz pomoc ridova koje smo dobili iz sekvence
    - greedy alg = svaki sa svakim da poredimo 
    - treba nam ljudski genom od pocetka do kraja, jer nam je on potreban kako bismo mogli da sekvenciraamo
    - ostaci koji nisu isti:
        - gde se nalaze? da li su na genima? 
    - nemamo referencu 

- **REFERENTNI GENOM**
    - mozemo da uzmemo manje stringove 
    - **ALIGMENT** - metod spajanje genoma, tako sto spajamo na osnovu reference rida

- Prvi referentni genom: 
    - sekvencirati ceo ljudski genom od pocetka do kraja je veoma jako dug posao 
    - mozemo da sekvenciramo iz samo jednog coveka i da taj genom predstavlja referencu 

#### Ljudski Genomi
- muskarci : 22 autozoma, jedan X i jedan Y hromozom
- zene : 22 autozoma, i dva X hromozoma

- **EGZOM** = deo koji kodira proteine (2% genoma)
    - sekvenciranje je dosta jeftinije, jer imamo bas dosta materijala 
    - kodiranje proteina 

#### **HG38** 

#### FASTA file format

- jednostavniji format
- cuvaju se referntni modeli (ridovi)
- >ime_regiona pa_sledi_sekvenca_koju_smo_sekvencirali

- imamo IUPAC codes
    - R = A ili G
    - Y = C, T ili U
    - N = bilo koja baza 

- FASTA index file
    - **.fai** format
    - nalaze se neke informacije o fasta fajlu 
    - zahtevaju referenncu, kako bi algoritmi radili brze

- trimer = sekvenda duzine 3 
- k-mer = sekvenca dizine k

