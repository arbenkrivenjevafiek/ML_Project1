# Shpenzueshmëria e barnave për nivelin dytësor dhe terciar në vitin 2024

## Përmbledhje**

**Titulli i projektit:** *Shpenzueshmëria e barnave për nivelin dytësor dhe terciar në vitin 2024*

**Universiteti:**
UNIVERSITETI I PRISHTINËS “HASAN PRISHTINA

**Fakulteti:**
Fakulteti i Inxhinierisë Elektrike dhe Kompjuterike

**Drejtimi:**
Inxhinieri Kompjuterike dhe Softuerike

**Lënda:**
Machine Learning

**Mësimdhënësit e lëndës:**

| Emri                   | Roli          | Fakulteti                                      |
|------------------------|---------------|-----------------------------------------------------|
| Prof. Dr. Lule AHMEDI  | Professor     | Fakulteti i Inxhinierisë Elektrike dhe Kompjuterike |
| Dr. Sc. Mërgim H. HOTI | Asistent      | Fakulteti i Inxhinierisë Elektrike dhe Kompjuterike |

 **Studentët:**

| Emri             | Roli             | Fakulteti                                           |
|----------------  |------------------|-----------------------------------------------------|
| Arben Krivenjeva | Master's Student | Fakulteti i Inxhinierisë Elektrike dhe Kompjuterike |
| Muhamet Burrniku | Master's Student | Fakulteti i Inxhinierisë Elektrike dhe Kompjuterike |
| Bledian Potera   | Master's Student | Fakulteti i Inxhinierisë Elektrike dhe Kompjuterike |

Ky projekt po realizohet në Universitetin e Prishtinës, specifikisht në Fakultetin e Inxhinierisë Elektrike dhe Kompjuterike, si pjesë e programit të studimeve të nivelit Master, në semestrin e dytë, në vitin akademik 2024/2025.

Objektivi kryesor i këtij projekti është zhvillimi i një modeli të fuqishëm të Mësimit të Makinerive, i cili do të jetë në gjendje të parashikojë me saktësi shpenzueshmërinë e barnave nëpër spitale dhe klinika, bazuar në parametra të ndryshëm si vlera e buxhetit, numri i klinikave/reparteve, llojet e artikujve, etj.

Të dhënat e përdorura për këtë projekt përmbajnë informacion mbi shpenzueshmërinë e barnave në aspektin sasior dhe monetar për nivelin dytësor dhe tretësor në vitin 2024, të ndara sipas spitaleve, klinikave/reparteve, llojeve të artikujve dhe operatorëve ekonomikë.

Duhet theksuar se këto të dhëna nuk përmbajnë asnjë informacion të ndjeshëm që mund të rrezikojë anonimitetin ose privatësinë.

## **Fazat e projektit**

**Faza I - Përgatitja e modelit:**
- Analiza Eksploruese e të Dhënave
- Para-procesimi për përgatitjen e të dhënave për analizë
   - Trajtimi i vlerave të zbrazëta
   - Pastrimi i të dhënave
   - Tipet e të dhënave
   - Reduktimi i Dimensionalitetit
   - Standartizimi, normalizimi, diskretizimi dhe binarizimi, 
   - Vizualizimi
   - Gjetja dhe fshirja e Outliers
- Ndarja e të dhënave sipas niveleve

**Faza II - Trajnimi i modelit:**
- Para-procesimi i të Dhënave: Sigurimi që veçoritë janë të përshtatshme për modelin e Machine Learning, përfshirë kodimin e variablave kategorikë dhe shkallëzimin e të dhënave numerike.
- Trajnimi i Modelit: Përdorimi i një algoritmi të përshtatshëm për klasifikimin dhe parashikimin e shpenzueshmërisë së barnave, duke marrë parasysh buxhetin, numrin e reparteve/klinikave dhe llojet e barnave.
- Vlerësimi i Modelit: Matja e saktësisë dhe efektivitetit të modelit me metrika të përshtatshme për parashikimin e shpenzueshmërisë së barnave.

**Faza III - Analiza dhe evaluimi (ri-trajnimi) dhe aplikimi i veglave të ML:**
- Rregullimi i Hiperparametrave: Eksperimentimi me parametra të ndryshëm për të optimizuar performancën e metodave të analitikës së të dhënave, duke siguruar klasifikime dhe parashikime më të sakta.
- Ritrajnimi i Modeleve: Përdorimi i konfigurimeve optimale për të përmirësuar rezultatet në:
   - Klasterizimin (K-Means) për të grupuar spitalet sipas modeleve të ngjashme të shpenzueshmërisë së barnave.
   - Analizën e Asocimit (Apriori, FP-Growth) për të zbuluar modelet e përdorimit të barnave dhe mungesat në spitale të ndryshme.
   - Klasifikimin (Random Forest, Decision Trees) për të parashikuar përdorimin e barnave në spitale bazuar në faktorë të ndryshëm.
   - Regresionin (Linear, Ridge, Lasso) për të modeluar dhe parashikuar shpenzimet për barna të ndryshme.
- Krahasimi i Performancës: Matja dhe krahasimi i efektivitetit të metodave të ndryshme duke përdorur metrika për saktësinë e grupeve (clustering), rregullsinë e rregullave të asocimit, saktësinë dhe kujtesën për klasifikim, si dhe gabimet e parashikimit për regresion.
- Vizualizimi i Rezultateve: Krijimi i grafikëve për të analizuar më mirë modelet e shpenzueshmërisë së barnave dhe ndikimin e parametrave në rezultatet e metodave të përdorura.
- Analiza e Parametrave: Krahasimi i konfigurimeve më të mira dhe më të këqija për secilën metodë, duke vlerësuar ndikimin e hiperparametrave në performancën e analizës dhe parashikimeve.

## ** Faza I - Analiza Eksploruese e të Dhënave**

**Madhësia e dataset** 