---
## Front matter
title: "Отчёт по лабораторной работе 5"
author: "Елизавета Александровна Гайдамака"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью данной работы является ознакомление с более сложными графическими функциями Octave такими как подгонка полиномиальной кривой и матричные преобразования (вращение, отражение, дилатация).

# Задание

- Подгонка полиномиальной кривой
- Матричные преобразования
  - Вращение
  - Отражение
  - Дилатация

# Теоретическое введение

В статистике часто рассматривается проблема подгонки прямой линии
к набору данных. Решить ее можно например по методу наименьших
квадратов. Процесс подгонки может быть автоматизирован встроенными функциями Octave.

Есть несколько способов построить матрицу коэффициентов в Octave. Один из подходов состоит в том, чтобы использовать команду ones для создания матрицы единиц соответствующего размера, а затем перезаписать первый и второй столбцы необходимыми данными.

Матрицы и матричные преобразования играют ключевую роль в компьютерной графике. Существует несколько способов представления изображения в виде матрицы. Подход, который мы здесь используем, состоит в
том, чтобы перечислить ряд вершин, которые соединены последовательно,
чтобы получить ребра простого графа.
Вращения
могут быть получены с использованием умножения на специальную матрицу. Дилатация (то есть расширение или сжатие) также может быть выполнено
путём умножения матриц.

# Выполнение лабораторной работы

Введём матрицу данных в Octave и извлечём вектора x и y. Нарисуем точки на графике.

![Рис.1](image\picture1.png)  

Построим уравнение вида
$$y = ax^2+bx+c.$$
Подставляя данные, получаем систему линейных уравнений. Построим матрицу коэффициентов А. Решение по методу наименьших квадратов получается из решения уравнения $$A^TAb = A^Ty,$$ где b – вектор коэффициентов полинома. Используем
Octave для построения уравнений.

![Рис.2](image\picture2.png)  

Решим задачу методом Гаусса и найдем коэффициенты.

![Рис.3](image\picture3.png) 

Построим соответствующий график параболы.

![Рис.4](image\picture4.png)  

Процесс подгонки может быть автоматизирован встроенными функциями Octave. Воспользуемся функцией polyfit, затем построим график.

![Рис.5](image\picture5.png)  

Закодируем граф-домик. Для этого заданим матрицу упорядоченных точек и нарисуем граф.

![Рис.6](image\picture6.png)  

Рассмотрим различные способы преобразования изображения. Вращения
могут быть получены с использованием умножения на специальную матрицу.

![Рис.7](image\picture7.png)  

Отразим граф дома относительно прямой
$$y = x.$$

![Рис.8](image\picture8.png)  

Теперь увеличим граф дома.

![Рис.9](image\picture9.png)

# Выводы

Благодаря данной работе я ознакомилась с более сложными графическими функциями Octave такими как подгонка полиномиальной кривой и матричные преобразования (вращение, отражение, дилатация).