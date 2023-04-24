---
## Front matter
title: "Отчёт по лабораторной работе 6"
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

Целью данной работы является ознакомление с инструментами работы с пределами, последовательностями и интегралами в Octave.


# Задание

- Частичные суммы
- Сумма ряда
- Вычисление интегралов
- Аппроксимирование суммами

# Теоретическое введение

Octave - полноценный язык программирования поддерживающий
множество типов циклов и условных операторов. Однако поскольку
это векторный язык, многие вещи, которые можно было бы сделать
с помощью циклов, можно векторизовать. Под векторизованным ко-
дом мы понимаем следующее: вместо того чтобы писать цикл для
многократной оценки функции мы сгенерируем вектор входных зна-
чений а затем оценим функцию с использованием векторного ввода.
В результате получается код который легче читать и понимать и он выполняется быстрее благодяря эффективным алгоритмам для матричных операций.

# Выполнение лабораторной работы

Посчитаем предел функции
$$f(x) = (1+\frac1n))^n.$$

![Рис.1](image\picture1.png)  

Посчитаем сумму от 2 до бесконечности для функции, а так же последовательность ее частичных сумм
$$a_n = \frac{1}{n(n+2)}.$$

![Рис.2](image\picture2.png)  

Найдем сумму от 1 до 1000 функции
$$\frac1n.$$

![Рис.3](image\picture3.png) 

Вычислим определенный интеграл
$$\int_{0}^{\pi /2}e^{x^{2}}cos(x)dx.$$
Будем использовать команду quad.

![Рис.4](image\picture4.png)  

Теперь вычислим этот же интеграл по правилу средней точки, напишем скрипт.

![Рис.5](image\picture5.png)

Изменим код так, чтобы он был векторизированный.

![Рис.6](image\picture6.png)  

Сравним время выполнения двух вариантов скриптов.

![Рис.7](image\picture7.png)  

# Выводы

Благодаря данной работе я ознакомилась с с инструментами работы с пределами, последовательностями и интегралами в Octave.
