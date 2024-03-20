# Nedelja 4

## Assembly 

- PCR = za umnozavanje dnk

- flow cell = plocica na kojoj se stavlja uzorak koji se satvlja u sekvencer

- sequencing reading = ciranje ridova 

- human genome project = 

- hromozomi kod coveka = 23 para 

- central dogma = dnk - rnk - protein

- fasta fajlovi = referetni genomi
- fai = iz sekvence

## Graph assembly

- spajanje sekvenci, nalazenje preklapanja izmedju sekvenci, sirenje sih sekvenci i spajanje od pocetka do kraja
    - kada smo sekvencirali neku novu vrsu koju nismo do sada 

- komplikovan zato sto imamo jako puno poredjenje stringova

- n ridova => n^2 operacija 

- ripitovi = nanje sekvence koje se vise puta ponavljaju u okviru jedne sekvence
    - jako je tesko asemblovati takve sekvence koje tek izadju iz sekvencera

- PIPLINE 
    1. ROW READS - izlazenje sirovih ridova
    2. READS ERROR CORRECTION - dobijamo kontige koji nemaju prekida
    3. SINGLE READS INDEXING; SINGLE READS ASSEMBLY - pravljenje skalfolda
    4. PAIRED READS SCAFFOLDING - 5and ridova je rastojanje ridova, maid paid ridovi - razmak je veci
    5. SCAFFOLDS GAP-CLOSING - govorenje o poziciji ridova; da dobijemo kontinualnu sekvencu, genom od pocetka do kraja
    6. CONTIGS, SCAFFOLDS 


- Paired end ridovi = dolaze sa istog reegiona i blizu su
- Mate pair reads = isto sto i paired ridovi samo sto su vise razdvojeni 
- skalfoldi = moze da sadrzi neke rupe 

- ERROR CORRECTION
    - greske u sekvenciranju mogu da smetaju kada pravimo kontige; da poremeti neko preklapanje koje je mozda najvece
    - proverava se paired ridovi; da li se zaista preklapaju? ili se ti ridovi ne poticu sa istog genoma 
    - ako ne ostranimo ridove sa puno gresaka dobicemo los genom
        - odsecanje ridova koji nisu dobri 
        - ili ce odbaciti tu sekvencu ili ce je prepraviti bez da se izgubi informacija 

- overlaps izmedju ridova = to su preklapanja izmedju stringova 


- DE BRUJIN GRAFOVI
    - k fiksiramo (da bude neparan broj)
        - cvorovi = k-1 meri koji se nalaze u ridu 
        - grane = k-mer u sekvenci 

    - cvorovi koji vise su najcesce greske
    - ponavljanja - ne znamo koliko smo se tacno provrteli kroz ciklus 

```

AACTG i k=4

_____ AACT  _____ ACTG _____
|AAC|  =>   |ACT|  =>  |CTG|
-----       -----      -----

k = 3

   AAC     ACT     CTG 
AA  =>  AC  =>  CT  =>  TG

```

- STRING GRAPHS
    - OVERLAP GRAPH
        - cvorovi - ridovi
        - grane - dva cvora su povezana ukoliko imaju overlap

    - modifikacija OVERLAP Grafova su STRING GRAFOVI
        - uklonimo tranzitivnosti 
        
- STRING VS DE BRUIJI grafovi
    - string celustrukturu zadrzavaju
    - de bruji = za luminu; tj. za krace ridove

- kako biramo k?
    - balansiramo - vece K kod de bruji grafova (imamo vise manjih grafova)

- kntizi = sekvence bez prekida 
    - kontinualne sekvence koje mozemo da napravimo a da nema ponavljanja
    
- gledamo sekvence na krajevima; da li ima neka sekvenca koja se overlapuje sa ivicom ovog kontika koja ima paired read

- 