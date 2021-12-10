---
## Front matter
lang: ru-RU
title: Элементы криптографии. Однократное гаммирование
author: |
	Гебриал Ибрам \inst{1}
	
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
	
date: 2021 Moscow, Russia

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Цель работы

## Цель работы

Освоить на практике применение режима однократного гаммирования.

# Результаты


## Результаты

1.Написал блок функции для расчетов. (рис. -@fig:001)

![Блок функции для расчетов](image/1.png){ #fig:001 width=100% }

## Результаты

Определил вид шифротекста при известном ключе и известном открытом тексте. (рис. -@fig:002)

![Задание 1. Получение шифротекста](image/2.png){ #fig:002 width=100% }

## Результаты

Определил ключ, с помощью которого шифротекст может быть преобразован в некоторый фрагмент текста, представляющий собой один из возможных вариантов прочтения открытого текста. (рис. -@fig:003)

![Один из вариантов прочения открытого текста:](image/3.png){ #fig:003 width=100% }


## Вывод


Освоил на практике применение режима однократного гаммирования.

## {.standout}

Спасибо за внимание 
