# AFM_mutations
## Part 1
0. На сайте IntOGEN нет данных о том, в каких типа рака мутировал данный ген. 
1. Типы мутаций: 
  - 67% -- **missense** (= относятся к точечным), меняют нуклеиновые кислоты (НК)
  - 25% -- **synonymous** (=относятся к структурным), не меняют НК
  - 6% -- **truncating** (= относятся к cтруктурным), укорачивает белок
  - 2% -- **splice-site**, согласно определению "a genetic alteration in the DNA sequence that occurs at the boundary of an exon and an intron (splice site). This change can disrupt RNA splicing resulting in the loss of exons or the inclusion of introns and an altered protein-coding sequence." То есть здесь может произойти и deletion, и insertion, и change (структурные мутации) [ссылка на определение](https://www.cancer.gov/publications/dictionaries/genetics-dictionary/def/splice-site-mutation)
2. Самые частотные типы рака, где встречается AFM: 
  - **Skin cancer** (61.2%)
  - **Soft Tissue cancer** (43.28%)
  - **Melanoma** (41%)
  - **Uterine cancer** (20%)
  - **Biliary Tract cancer** (16.9%)

Остальные типы представлены в pdf-файле. \
Все скриншоты по поиску представлены в файле AFM_muts.pdf
## Part 2
Поиск мутаций осуществлялcя с помощью Python:
File | Gene | Found mutations? (Number)| Why chose
------------ | ------------- | ------------- | ------------- 
SSM_AFM-4.ipynb | PCDH15 (DO222481) | Yes (78) | AFM в основном есть в **Skin cancer**, поэтому был выбран геном, у которого данный тип рака + проект **MELA-AU**, он первый в [рейтинге](https://dcc.icgc.org/genes/ENSG00000079557/mutations) для AFM
SSM_AFM.ipynb| KCND2 (DO229217) | No | **Uterine cancer** + Проект **LMS-FR** второй по частотности, поэтому было интересно, находятся ли там похожие мутации
SSM_AFM-2.ipynb| SGCZ (DO228017)| Yes (1289) | **Melanoma** + Проект **SKCA-BR** третий по частотности
SSM_AFM-3.ipynb| MGAT4C (DO229545) | Yes (1) | **Soft Tussie cancer** + Проект **UTCA-FR** четвертый по частотности

Было ожидаемо, что мутации нашлись в **1**, **3** и **4** случаях, однако тот факт, что их не оказалось в **LMS-FR** показался странным, но в то же самое время мы не проверяли все геномы из **LMS-FR**, возможно, это могло повлиять. \
Интересно, что с **PCDH15** нашлось не так много похожего, это говорит о том, насколько гетерогенен рак (также, этот факт может объяснять и то, что ничего не нашлось в **LMS-FR**).
### Files
Таблицы для общих мутаций и python files лежат на github.
