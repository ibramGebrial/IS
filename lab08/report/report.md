---
# Front matter
lang: ru-RU
title: "Отчёт по лабораторной работе 8"
subtitle: "Элементы криптографии. Шифрование (кодирование) различных исходных текстов одним ключом"
author: "Гебриал Ибрам Есам Зекри НПИ-01-18"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Освоить на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом.



# Теоретические сведения

Простейшей и в то же время наиболее надёжной из всех схем шифрования является так называемая схема однократного использования (см. рисунок 1), изобретение, которое чаще всего связывают с именем Г.С. Вернама [1]. 

Гаммирование – это наложение (снятие) на открытые (зашифрованные) данные криптографической гаммы, т.е. последовательности элементов данных, вырабатываемых с помощью некоторого криптографического алгоритма, для получения зашифрованных (открытых) данных. С точки зрения теории криптоанализа, метод шифрования случайной однократной равновероятной гаммой той же длины, что и открытый текст, является невскрываемым (далее для краткости будем употреблять термин "однократное гаммирование", держа в уме всё сказанное выше). Кроме того, даже раскрыв часть сообщения, дешифровщик не сможет хоть сколько-нибудь поправить положение – информация о вскрытом участке гаммы не даёт информации об остальных её частях [1]. 

Допустим, в тайной деловой переписке используется метод однократного наложения гаммы на открытый текст. "Наложение" гаммы – не что иное, как выполнение операции сложения по модулю 2 (xor) её элементов с элементами открытого текста. Эта операция в языке программирования С++ обозначается знаком , а в математике – знаком [1]. 

Гаммирование является симметричным алгоритмом. Поскольку двойное прибавление одной и той же величины по модулю 2 восстанавливает исходное значение, шифрование и дешифрование выполняется одной и той же программой [1].

 
# Выполнение лабораторной работы

1. Написал блок функции для расчетов. (рис. -@fig:001)

![Блок функции для расчетов](image/1.png){ #fig:001 width=100% }


2. Написал блок обработки данных. (рис. -@fig:002)

![Блок данных и вывод результата](image/2.png){ #fig:002 width=100% }


# Контрольные вопросы

1. Как, зная один из текстов (P1 или P2), определить другой, не зная при этом
ключа?

Сложить по модулю 2 оба шифротекста и декодировать первый текст используя полученное значение и известный второй текст.

2. Что будет при повторном использовании ключа при шифровании текста? 

Оба текста, шифрованные одним ключем будут подвержены риску взлома.

3. Как реализуется режим шифрования однократного гаммирования одним
ключом двух открытых текстов?


Шифруем оба текста одним ключем.

4. Перечислите недостатки шифрования одним ключом двух открытых
текстов.

Подверженость риску взлома.

5. Перечислите преимущества шифрования одним ключом двух открытых
текстов.

Используется меньше ключей.



# Выводы

Освоил на практике применение режима однократного гаммирования на примере кодирования различных исходных текстов одним ключом.

# Список литературы


1. Гаммирование. Моделирование работы скремблера// URL: https://ami.nstu.ru

/~gultyaeva/pszi/Materials/lab1.pdf (дата обращения: 10.12.2021).