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

1000 failas:
1. 0.0726 s
2. 0.0690 s
3. 0.0101 s
4. 0.0022 s || 0.0096 s
5. 0.1923 s

10000 failas:
1.  0.7242 s
2.  0.6130 s
3.  0.0906 s
4.  0.0193 s || 0.0753 s
5.  1.8647 s

100000 failas:
1.  7.8920 s
2.  6.0832 s
3.  1.0049 s
4.  0.1892 s || 0.7502 s
5.  19.416 s

1000000 failas:
1. 74.21 s
2. 60.95 s
3. 10.71 s
4. 1.8352 s || 7.5544 s
5. 205.31 s

10000000 failas:
1. 802.87 s
2. 766.69 s
3. 96.68 s
4. 43.26 s || 48.69 s
5. 1758.19 s
