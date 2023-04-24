---
## Front matter
title: "Отчёт по лабораторной работе 8"
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

Целью данной работы является ознакомление с инструментами Octave, позволяющими решать задачи на собственные значения.

# Задание

- Собственные значения и собственные векторы
- Марковские цепи

# Теоретическое введение

Це́пь Ма́ркова — последовательность случайных событий с конечным или счётным числом исходов, где вероятность наступления каждого события зависит только от состояния, достигнутого в предыдущем событии. Характеризуется тем свойством, что, говоря нестрого, при фиксированном настоящем будущее независимо от прошлого. Названа в честь А. А. Маркова (старшего), который впервые ввёл это понятие в работе 1906 года.

# Выполнение лабораторной работы

Найдем собственные значения и собственные вектора матрицы.

![Рис.1](image\picture1.png)

Чтобы получить матрицу с действительными собственными значениями, создадим симметричную матрицу путем умножения матрицы на транспонированную матрицу.

![Рис.2](image\picture2.png)  

Пусть у нас есть цепь Маркова, состоящая из пяти состояний. Из состояний 2-4 можно двигаться илбо вправо, либо влево, а из состояний 1 и 5 - только в одну сторону. Найдем векторы вероятностей после 5ти шагов для нескольких разных начальных векторов.

![Рис.3](image\picture3.png) 

Теперь найдем вектор равновесного состояния.

![Рис.4](image\picture4.png)  

Сделаем проверку.

![Рис.5](image\picture5.png)  

# Выводы

Благодаря данной работе я ознакомилась с инструментами Octave, позволяющими решать задачи на собственные значения.