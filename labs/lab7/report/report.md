---
## Front matter
title: "Отчёт по лабораторной работе 7"
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

Освоение основных инструментов построения разных типов графиков в Octave.

# Задание

- Параметрические графики
- Полярные координаты
- Графики неявных функций
- Комплексные числа
- Спеиальные функции

# Теоретическое введение

Помимо обычных 2D графиков, Octave позволяет строить графики параметрических функций, функций в неявном виде, а также функций в полярных координатах. Octave умеет работать с комплексными числами: производить вычисления и изображать их на координатной плоскости.

# Выполнение лабораторной работы

Построим график трех периодов циклоиды радиуса 2:
$$x = r(t-sin(t)), y=r(1-cos(t)).$$

![Рис.1](image\picture1.png)  

Построим улитку Паскаля:
$$y=1-2sin(\vartheta).$$

![Рис.2](image\picture2.png) 

Можно также построить эту функцию в полярных осях.

![Рис.3](image\picture3.png) 

Построим неявную функцию
$$-x^2-xy+x+y^2-y=1.$$

![Рис.4](image\picture4.png)  

Теперь построим окружность
&&(x-2)^2+y=25&&
и касательную к ней в точке (-1,4)

![Рис.5](image\picture5.png)  

Произведем основные арифметические операции с двумя комплексными числами.

![Рис.6](image\picture6.png)  


![Рис.7](image\picture7.png)  



Иногда Octave выдает неожиданные результаты для комплексных чисел.



![Рис.8](image\picture8.png)



Построим графики Гамма-функции и факториала.



![Рис.9](image\picture9.png)



Асимптоты в части графика отрицательного аргумента это дефекты вычислений. Уберем их.

![Рис.10](image\picture10.png)

# Выводы

Благодаря данной работе я освоила основные инструменты построения разных типов графиков в Octave.