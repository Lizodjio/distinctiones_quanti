# Количественное исследование состава сборников _distinctiones_ 


Этот репозиторий содержит jupyter-ноутбуки, посвящённые подготовке, анализу и визуализации оглавлений сборников distinctiones. Эти данные легли в основу первой главы ВКР Елизаветы Романовской «Жанровые особенности сборников distinctiones: историко-филологический анализ дистинкций о смерти и количественное исследование состава сборников» (Москва, ВШЭ, 2025). Научный руководитель: Светлана Александровна Яцык. 

## Содержание

```text
project/
├── data/
│   ├── conllu/               # .conllu-файлы для подачи в модель evalatin
│   ├── csv/                  # таблицы с метаданными
│   ├── Distinguo-TEI/        # исходные TEI-файлы проекта Distinguo
│   ├── lemmas/               # *.csv с леммами по сборникам
│   └── txt/                  # текстовые версии извлечённых данных
│
├── output/
│   ├── for_gephi/            # рёбра и узлы для визуализации сети
│   ├── POS/                  # части речи
│   ├── shared_lemmas_txt/    # текстовые файлы общих для пар сборников лемм 
│   └── stats_tables/         # статистические таблицы (уникальность, Jaccard и т.д.)
│
├── notebooks/                # все Jupyter-ноутбуки
├── evalatin2024-latinpipe/  # внешний репозиторий с моделью EvaLatin
└── README.md
```

Все ноутбуки находятся в папке notebooks/ и организованы по шагам:

1. 01_Подготовка_Заголовков.ipynb — экспорт заголовков дистинкций из TEI файлов.
2. 02_Подготовка_CoNLL_U_файлов.ipynb — подготовка файлов в формате CoNLL-U, необходимом для лемматизатора. 
3. 03_Лемматизация.ipynb — автоматическая лемматизация заголовков.
4. 04_Стоп_слова.ipynb — удаление стоп-слов.
5. 05_Самые_частотные_слова.ipynb — частотный анализ.
6. 06_Части_речи.ipynb — морфосинтаксическая аннотация.
7. 07_Social_Network_Analysis.ipynb — экспорт таблиц узлов и ребер для анализа сетей в gephi.
8. 08_Гапаксы_для_каждой_коллекции.ipynb — выявление гапаксов в каждой коллекции.
9. 09_Общие_леммы.ipynb — перекрёстное сравнение лемм по сборникам.
10. 10_Уникальные_персечения_между_парами_и_коэффициент_Жаккара - выявление уникальных пересечений между парами коллекций и оценка сходства сборников.
11. 11_уникальные_и_неуникальные_леммы_статистика-2.ipynb - оценка оригинальности сборников через соотношение уникальных лемм (гапаксов) к неуникальным.


Эта работа стала возможной благодаря проекту [Distinguo](https://distinguo.huma-num.fr). 
