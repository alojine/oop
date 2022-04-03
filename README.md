# objective-programming
Repository created for objective programming using C++

# v0.1
Šioje versijoje uždavinys buvo sprendžiamas dviem budais:
1. Cmasyvo būdu **Cmasyvas.cpp** faile - Studento duomenys saugomi struktūroje *data*
2. Vektorių būdu **Vektoriai.cpp** faile - Studento duomenys saugomi *data* tipo *vektoriuje*

Programa turi 7 funkcijas: input, output, mediana, vidurkis, select, addmark, genrandom. Programa paklausia vartotojo kiek jis noretų sugeneruoti studentų, paprašo įvesti vardą, pavardę, pažymių kiekį(po įvedimo galime pasirinkti ar norime papildytį kiekį), pasirenkame kaip vesti rezultatą, medianos ar vidurkio metodu.

Į terminalą išvedami šie duomenys: *Vardas*, *Pavardė*, *Galutinis rezultatas*(Vidurkis/Mediana).

# v0.2
Šioje versijoje kodas yra atnaujintas, pridėtas skaitymas ir rašymas į failą. 

Paleidus programa vartotojo paklausiama ar jis nori skaityti studentus iš failo:

Jei **ne**: vyksta praeitos versijos **v0.1** skaitymas iš terminalo.

Jei **taip**: Nuskaitomas failas *studentai.txt*, į failą *kursiokai.txt* išvedamas studento vardas, pavardė, galutinis vidukis ir mediana.

# v0.3
Šioje versijoje atliktas praeitos versijos(v0.2) kodo refactoringas. Programa veikia tuo pačiu principu, tačiau yra išskaidyta į header, resource ir source failus.
1. Pagrindinis failas: *Source.cpp* savyje laiko header failus ir pagrindinę main funkcija kurioje atliktas exception handling skaitymui ir rašymui į failą.
2. Aplanke: *Headers* yra visi programai reikalingi header(.h) failai.
3. Aplanke: *Resources* yra visi programai reikalingi papildomi (.cpp) faila kuriuose aprašytos funkcijos.

# v0.4
Šioje versijoje sukurtas failu generatorius ir matuojami programos vykdymo laikai.
Vartotojas pasirenka generuoti failą automatiškai.
Vartotojas pasirenka naudoti failų generatorių.
Vartotojas iveda failo pavadinimą ir kiekį studentų kuriuos nori sugeneruoti.

Programos kodas yra isskaidytas į tris pagrindinius failus:
1. Pagrindinis failas *Source.cpp* laiko (header) antraštes ir main funkciją.
2. *functions.cpp* laiko savyje funkcijų aprašus.
3. *headers.h* laiko savyje funkcijų antraštes
4. Failo skaitymas vyksta iš ivesto failo. Pvz: studentai100000.txt.
5. Failo išvedimas vyksta į du skirtingus failus: *kietiakai.txt*(studentams kurių galutinis balas >= 5.0) ir *nuskriaustukai.txt* (studentams kurių galutinis balas < 5.0).

Testavimui generuojami 5 atsitiktiniai studentų pažymiai.
Programos laikas nustatomas šiems kriterijams:
1. Failo kūrimui ir jo uždarymui.
2. Duomenų nuskaitymui iš failo.
3. Studentų rušiavimui į grupes.
4. Surušiuotų studentų išvedimą į du failus.
5. Visos programos laikas.

VECTOR
1000
1. Failo sudarymas uztruko: 0.0263304 s
2. Failo nuskaitymas uztruko: 0.0062851 s
3. Failo skirstymas i grupes uztruko: 0.0001799 s
4.1 kietiakai.txt surasymas uztruko: 0.0010151 s
4.2 nuskriaustukai.txt surasymas uztruko: 0.0052932 s
5. Visa programa uztruko 0.0450208 s

10000
Failo sudarymas uztruko: 0.395983 s
Failo nuskaitymas uztruko: 0.0949548 s
Failo skirstymas i grupes uztruko: 0.0021033 s
kietiakai.txt surasymas uztruko: 0.0077206 s
nuskriaustukai.txt surasymas uztruko: 0.0415379 s
Visa programa uztruko 0.571244 s

100000
Failo sudarymas uztruko: 2.92119 s
Failo nuskaitymas uztruko: 0.675066 s
Failo skirstymas i grupes uztruko: 0.0210955 s
kietiakai.txt surasymas uztruko: 0.0866178 s
nuskriaustukai.txt surasymas uztruko: 0.389649 s
Visa programa uztruko 4.16463 s

1000000
Failo sudarymas uztruko: 38.2789 s
Failo nuskaitymas uztruko: 13.4123 s
Failo skirstymas i grupes uztruko: 0.267259 s
kietiakai.txt surasymas uztruko: 0.937183 s
nuskriaustukai.txt surasymas uztruko: 4.50081 s
Visa programa uztruko 58.4967 s


