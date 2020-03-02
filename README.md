# POSTWORK2

USER@HP MINGW64 ~/desktop
$ cd Mi_Proyecto

USER@HP MINGW64 ~/desktop/Mi_Proyecto
$ cd Mis_datos

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ head cwurData.csv
world_rank,institution,country,national_rank,quality_of_education,alumni_employment,quality_of_faculty,publications,influence,citations,broad_impact,patents,score,year
1,"Harvard University",USA,1,7,9,1,1,1,1,,5,100,2012
2,"Massachusetts Institute of Technology",USA,2,9,17,3,12,4,4,,1,91.67,2012
3,"Stanford University",USA,3,17,11,5,4,2,2,,15,89.5,2012
4,"University of Cambridge",United Kingdom,1,10,24,4,16,16,11,,50,86.17,2012
5,"California Institute of Technology",USA,4,2,29,7,37,22,22,,18,85.21,2012
6,"Princeton University",USA,5,8,14,2,53,33,26,,101,82.5,2012
7,"University of Oxford",United Kingdom,2,13,28,9,15,13,19,,26,82.34,2012
8,"Yale University",USA,6,14,31,12,14,6,15,,66,79.14,2012
9,"Columbia University",USA,7,23,21,10,13,12,14,,5,78.86,2012

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ tail cwurData.csv
991,"Xidian University",China,81,367,542,218,830,974,812,984,434,44.03,2015
992,"Federal University of Bahia",Brazil,17,367,540,218,962,865,645,969,774,44.03,2015
993,"Southwest Jiaotong University",China,82,367,327,218,937,962,812,998,861,44.03,2015
994,"Ryerson University",Canada,33,367,567,218,811,969,511,975,756,44.03,2015
995,"King Abdulaziz University",Saudi Arabia,4,367,449,218,595,430,645,994,839,44.03,2015
996,"University of the Algarve",Portugal,7,367,567,218,926,845,812,969,816,44.03,2015
997,"Alexandria University",Egypt,4,236,566,218,997,908,645,981,871,44.03,2015
998,"Federal University of Ceará",Brazil,18,367,549,218,830,823,812,975,824,44.03,2015
999,"University of A Coruña",Spain,40,367,567,218,886,974,812,975,651,44.02,2015
1000,"China Pharmaceutical University",China,83,367,567,218,861,991,812,981,547,44.02,2015
USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -a USA cwurData.csv | head
1,"Harvard University",USA,1,7,9,1,1,1,1,,5,100,2012
2,"Massachusetts Institute of Technology",USA,2,9,17,3,12,4,4,,1,91.67,2012
3,"Stanford University",USA,3,17,11,5,4,2,2,,15,89.5,2012
5,"California Institute of Technology",USA,4,2,29,7,37,22,22,,18,85.21,2012
6,"Princeton University",USA,5,8,14,2,53,33,26,,101,82.5,2012
8,"Yale University",USA,6,14,31,12,14,6,15,,66,79.14,2012
9,"Columbia University",USA,7,23,21,10,13,12,14,,5,78.86,2012
10,"University of California, Berkeley",USA,8,16,52,6,6,5,3,,16,78.55,2012
11,"University of Chicago",USA,9,15,26,8,34,20,28,,101,73.82,2012
12,"Cornell University",USA,10,21,42,14,22,21,16,,10,73.69,2012

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -a USA cwurData.csv | wc
    573    2170   46954

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -a USA cwurData.csv > USA-Universities.csv

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ echo universidad,pais,rankin_nacional,calidaddelaeducacion,alumnosconemple,calidadde la facultad,publicaciones,influencia,citas,impacto,patentes,puntuacion,año | cat - cwurData.csv > rankin_universidades.csv

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ ls
cwurData.csv                                   school_and_country_table.csv
education_expenditure_supplementary_data.csv   shanghaiData.csv
educational_attainment_supplementary_data.csv  timesData.csv
rankin_universidades.csv                       USA-Universities.csv

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ head rankin_universidades.csv
universidad,pais,rankin_nacional,calidaddelaeducacion,alumnosconemple,calidadde la facultad,publicaciones,influencia,citas,impacto,patentes,puntuacion,año
world_rank,institution,country,national_rank,quality_of_education,alumni_employment,quality_of_faculty,publications,influence,citations,broad_impact,patents,score,year
1,"Harvard University",USA,1,7,9,1,1,1,1,,5,100,2012
2,"Massachusetts Institute of Technology",USA,2,9,17,3,12,4,4,,1,91.67,2012
3,"Stanford University",USA,3,17,11,5,4,2,2,,15,89.5,2012
4,"University of Cambridge",United Kingdom,1,10,24,4,16,16,11,,50,86.17,2012
5,"California Institute of Technology",USA,4,2,29,7,37,22,22,,18,85.21,2012
6,"Princeton University",USA,5,8,14,2,53,33,26,,101,82.5,2012
7,"University of Oxford",United Kingdom,2,13,28,9,15,13,19,,26,82.34,2012
8,"Yale University",USA,6,14,31,12,14,6,15,,66,79.14,2012

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ echo rank,university,score,year | cat timesData.csv > timesdata-1.csv

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep USA cwurData.csv | grep ,*,*,*,*,*,*,*,*,*,18, timesData.CVS
grep: timesData.CVS: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep USA cwurData.csv | grep ,*,*,*,*,*,*,*,*,*, ^11000,* timesData.CVS
grep: ^11000,*: No such file or directory
grep: timesData.CVS: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep USA cwurData.csv | grep .,*.,*.,*.,*.,*.,*.,*.,*.,*., ^11000,*
grep: ^11000,*: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep USA cwurData.csv | grep .,*.,*.,*.,*.,*.,*.,*.,*.,*., ^11...,*
grep: ^11...,*: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep USA cwurData.csv | grep .,*.,*.,*.,*.,*.,*.,*.,*.,*., ^11...,*
grep: ^11...,*: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -E USA cwurData.csv | grep .,*.,*.,*.,*.,*.,*.,*.,*.,*., ^11...,*
grep: ^11...,*: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep ^11..., timesData.csv | head

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep ^11..., timesData.csv | wc
      0       0       0

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -E ".*,.*,.*,.*,.*,.*,.*,.*,.*,^11...," timesData.csv | grep -E ".*,.*,USA,.*" | wc
      0       0       0

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -E ".*,.*,.*,.*,.*,.*,.*,.*,.*,^11...," timesData.csv | grep -E ".*,.*,USA,.*"

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -aE ^1., cwurData.csv | wc                                                    40     136    2863

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -aE ^1., cwurData.csv | head
10,"University of California, Berkeley",USA,8,16,52,6,6,5,3,,16,78.55,2012
11,"University of Chicago",USA,9,15,26,8,34,20,28,,101,73.82,2012
12,"Cornell University",USA,10,21,42,14,22,21,16,,10,73.69,2012
13,"University of Pennsylvania",USA,11,31,16,24,9,10,8,,9,73.64,2012
14,"University of Tokyo",Japan,1,32,19,31,8,19,23,,3,69.49,2012
15,"Johns Hopkins University",USA,12,34,77,20,11,9,9,,7,66.94,2012
16,"Swiss Federal Institute of Technology in Zurich",Switzerland,1,26,66,11,40,51,44,,34,66.69,2012
17,"Kyoto University",Japan,2,42,38,19,25,36,43,,23,65.76,2012
18,"Weizmann Institute of Science",Israel,1,4,101,22,101,67,101,,29,65.09,2012
19,"University of California, Los Angeles",USA,13,62,59,23,3,11,6,,13,64.05,2012

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -aE ^tech, cwurData.csv | head

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -aE ^Tec, cwurData.csv | head

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -aE ^Tec , cwurData.csv | head
grep: ,: No such file or directory

USER@HP MINGW64 ~/desktop/Mi_Proyecto/Mis_datos
$ grep -aE ^Institute, cwurData.csv | head
