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

**Madhësia e dataset** Të dhënat përmbajnë 54,161 rreshta dhe 13 kolona.

**Kolonat**: Dataset përmban kolonat: Spitali, NjesiaReparti, Numri, Shenim, DataRegjistrimit, Artikulli, ArtikulliLloji, RrugaMarrjes, Sasia, Cmimi, Vlera, OperatoriEkonomik, LlojiHyrjes

 **Tipet e të dhënave**: Atributet që përmbajnë tekst (Spitali, NjesiaReparti, Numri, Shenim, DataRegjistrimit, Artikulli, ArtikulliLloji, RrugaMarrjes, OperatoriEkonomik, LlojiHyrjes) janë në formatin e tipit object, ndërsa atributet që përmbajnë numra (Sasia, Cmimi, Vlera) janë në formatin e tipit float.

 **Kuptimi i të gjitha kolonave Para-procesimit**
 1. **Spitali**: Spitali i cili i takon nivelit dytësor ose terciar
 2. **Klinika/Repart**: Klinikë ose repart, në varësi të organizimit që ka spitali
 3. **Numri**: Numër rendor i transaksionit sipas njësisë organizative të spitalit
 4. **Shenim**: Një shënim ose koment për atë transaksion
 5. **DataRegjistrimit**: Data e regjistrimit të transaksionit
 6. **Artikulli**: Emërtimi i produktit, i cili është produkt gjenerik dhe përmban detajet e tij
 7. **ArtikulliLloji**: Lloji i produktit ndahet në tri kategori: barna, citostatikë dhe reagentë
 8. **RrugaMarrjes**: Rruga e marrjes është mënyra e përdorimit të produktit farmaceutik nga pacienti
 9. **Sasia**: Sasia e produkteve e shprehur në doza
 10. **Cmimi**: Çmimi i produktit, i cili përfaqëson çmimin njësi për dozë
 11. **Vlera**: Vlera e produktit si rezultat i shumëzimit të sasisë me çmimin
 12. **OperatoriEkonomik**:Ruhen të dhënat për operatorin ekonomik
 10. **LlojiHyrjes**: Lloji i hyrjes së produktit, që përfaqëson burimin e financimit të produktit

## **Para-procesimi**

**Formati fillestar i fajllit**

Fajlli fillestar është në format '.xlsx', i cili, para ngarkimit në projekt, konvertohet në një fajll '.csv'.

Atributet që përmbajnë tekst (Spitali, NjesiaReparti, Numri, Shenim, DataRegjistrimit, Artikulli, ArtikulliLloji, RrugaMarrjes, OperatoriEkonomik, LlojiHyrjes) janë në formatin e tipit object, ndërsa atributet që përmbajnë numra (Sasia, Cmimi, Vlera) janë në formatin e tipit float.

**Vlera me gabime NULL**
- *Artikulli* ka një rresht me vlerë të munguar (NULL)
  - Trajtimi: Ky rresht është fshirë, pasi përveç artikullit, edhe kolonat e tjera si Sasia, Çmimi dhe Vlera kishin vlera (NULL).
- *Sasia* ka 33 rreshta me vlerë të munguar (NULL)
  - Trajtimi: Këto rreshta janë fshirë, pasi, përveç sasisë, edhe kolonat e tjera si Çmimi dhe Vlera kishin vlera të mungueshme (NULL)
- *Cmimi* ka 33 rreshta me vlerë të munguar (NULL)
  - Trajtimi: Këto rreshta janë fshirë, pasi, përveç çmimit, edhe kolonat e tjera si Sasia dhe Vlera kishin vlera të mungueshme (NULL)
- *Vlera* ka 30 rreshta me vlerë të munguar (NULL)
  - Trajtimi: Këto rreshta janë fshirë, pasi, përveç vlerës, edhe kolonat e tjera si Sasia dhe Çmimi kishin vlera të mungueshme (NULL)

Pra, të gjitha këto kolona me vlera të mungueshme (NULL) kanë qenë njëkohësisht në të njëjtët rreshta. Si rezultat, kemi fshirë gjithsej 33 rreshta për kolonat Artikulli, Sasia, Çmimi dhe Vlera.

### **Para-procesimi i atributeve**

**DataRegjistrimit**

Në kolonën Data e Regjistrimit, formati i datave është rregulluar duke u standardizuar në formatin "yyyy-mm-dd".

**Kolonat Sasia, Cmimi, Vlera**

Për kolonat Sasia, Çmimi dhe Vlera, është formatuar që të shfaqen me dy shifra pas pikës dhjetore.

### **Reduktimi i dimensioneve**

Atributet në vijim janë larguar nga dataset-i, pasi nuk kishim ndonjë interes për t'i përdorur më vonë:

1. Numri
2. Shenim
3. RrugaMarrjes

### Vizualizimi

**Cilesia e të dhënave**

Në tabelën e mëposhtme kemi paraqitur cilësinë e të dhënave për të gjitha kolonat e dataset-it, duke treguar vlerat me gabime, vlerat unike, vlerat e duplikuara, mesataren, medianën, devijimin standard, vlerën minimale dhe vlerën maksimale.

<img src="img/Cilesia_E_Te_Dhenave.png" alt="Cilesia_E_Te_Dhenave"/>