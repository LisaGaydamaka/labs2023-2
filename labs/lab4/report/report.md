---
## Front matter
title: "Отчёт по лабораторной работе 4"
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

Целью данной работы является ознакомление со сложными алгоритмы, встроенными в Octave для решения систем линейных уравнений.

# Задание

- Метод Гаусса
- Левое деление
- LU-разложение
- LUP-разложение

# Теоретическое введение

Octave содержит сложные алгоритмы, встроенные для решения систем линейных уравнений.

Алгоритм решения СЛАУ методом Гаусса подразделяется на два этапа.

- На первом этапе осуществляется так называемый прямой ход, когда путём элементарных преобразований над строками систему приводят к ступенчатой или треугольной
форме, либо устанавливают, что система несовместна.
- На втором этапе осуществляется так называемый обратный ход, суть которого заключается в том, чтобы выразить все получившиеся базисные переменные через небазисные
и построить фундаментальную систему решений, либо, если все переменные являются
базисными, то выразить в численном виде единственное решение системы линейных
уравнений.

LU-разложение — это вид факторизации матриц для метода Гаусса.

# Выполнение лабораторной работы

Для системы линейных уравнений построим расширенную матрицу. Можно её просматривать поэлементно. Мы также можем извлечь целый вектор строки или вектор столбца, используя оператор сечения. Реализуем теперь явно метод Гаусса. Матрица теперь имеет треугольный вид. Можно
отобразить больше десятичных разрядов.

![Рис.1](image\picture1.png)  

Встроенная операция для решения линейных систем вида
$$Ax = b$$
в Octave называется левым делением и записывается как A\b. Выделим из расширенной матрицы B матрицу A и вектор b. После найдём вектор x.

![Рис.2](image\picture2.png)  

Найдем LUP-разложение матрицы A.

![Рис.3](image\picture3.png) 

Найдем LU-разложение матрицы A.

![Рис.4](image\picture4.png)  


# Выводы

Благодаря данной работе я ознакомилась со сложными алгоритмы, встроенными в Octave для решения систем линейных уравнений.
