# тау

# Лекция 1

## Введение

Бирюков Игорь ИвановичСидит на спецухе всисав меме с 69 года

> "чета умею, чета знаю, чета не умею" (с) Бирюков

На семах отмечает посещаемость
За опоздания вставляет пизды
Экзамен: до него лучше не доходить, и его очнь сложно сдать (со слов Бирюкова)
Условия для автомата и формулу разошлет позже
~~За одну активу можно получить от 0.02 до 0.1, за ошибку проебывается -1 (он сказал, что это прикол)~~
**2 хардкорных проеба на семинаре или 4 пропуска по неуважительной - минус автомат**
Контрольная на шестом семинаре
В конце апреля будет дз до конца мая
**Дз в день дедлайна сдавать нельзя**
Никакой дополнительной литературы по предмету нет
Есть учебник савельева, но он не советует даже лезть в это, лучше ходить на лекции

# Теория

Схемы с памятью **- последовательностные**Схемы без памяти **- комбинационные****В качестве памяти используются триггеры**, их исполнение нас не волнуетЧасто будем использовать метод Квайна-Маккласки и диаграммы ВейчаВ проектировании есть шаг минимизации, там это все применяется в обязательном порядке

> "100 грамм лишних не нужно, нужно откинуться" (с) Бирюков

## 1 этап проектирования - от словесного описания к табличному

> Определение: одноразрядным полусумматором называется устройство, которое работате в следующей арифметике:
> 0+0=0
> 0+1=1
> 1+0=1
> 1+1=10

### Табличное представление полусумматора


| a | b | P | S |
| :-- | :-- | :-- | :-- |
| 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 |

## 2 этап проектирования - переход к аналитической (СДНФ и СКНФ) форме представления переключательных функций от табличного представления

## 3 этап проектирования - минимизация аналитической формы представления

## 4 этап проектирования - возможное проектирование схемы в определенном базисе (с одним видом логических элементов)

## 5 этап проектирования - нарисовать функциональную схему того, что получается в конечном итоге

## Булева алгебра и ее основные законы

> Определение 1: логической переменной булевой алгебры называется величина, которая принимает значение 0 или 1.

> Определение 2: переключательная функция (или функция алгебры логики) - такая функция, которая так же, как и ее аргументы, принимает значение 0 или 1.

> Определение 3: запись вида $a_1, a_2, a_3, ..., a_n$, где каждая $a_i$принимает значение 0 или 1, называется набором.

> Определение 4: переключательная функция называется полностью определенной, если на всех наборах данной функции она определена.

> Определение 5: переключательная функция называется неполностью определенной, если на некоторых наборах функция не определена.


| a | b | c | A | B |
| :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 0 | 1 | X |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 | X |
| 1 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 | 1 |

В этой таблице функция A полностью определенная, B - неполностью определенная.
Все наборы имеют свои номера. Чтобы получить номер набора, нужно перевести его значение из двоичной системы в десятеричную. Так, набор


| 0 | 1 | 1 |
| :-: | :-: | :-: |

имеет номер 3.
При n аргументов количество наборов всегда равно $2^n$. Количество переключательных функций для n аргументов определяется по формуле $2^{2^n}$.
Все переключательные функции также имеют свой номер. Чтобы получить номер переключательной функции, ее двоичное значение надо перевести в десятичную:

$$
01100010_2 = 98

$$

> Все переключательные функции мы будем записывать в виде
> $f_{98_{(3)}} = 1(1, 2, 6)$
> Для неполностью определенной:
> $f_{(3)} = 1(0, 3, 7)$
> $H = 2, 5$
> Неполностью определенные функции **не нумеруются.**

### Кол-во аргументов n = 1


| a | $f_0$ | $f_1$ | $f_2$ | $f_3$ |
| :-: | :-----: | :-----: | :-----: | :-----: |
| 0 |   0   |   0   |   1   |   1   |
| 1 |   0   |   1   |   0   |   1   |

$f_0 = const0,$
$f_1 = a,$
$f_2 = not(a),$
$f_3 = const1$

Функция $f_2$ реализуется с помощью инвертора (логическое НЕ)

### Кол-во аргументов n = 2


| a | b | $f_0$ | $f_1$ | $f_2$ | $f_3$ | $f_4$ | $f_5$ | $f_6$ | $f_7$ | $f_8$ | $f_9$ | $f_A$ | $f_B$ | $f_C$ | $f_D$ | $f_E$ | $f_F$ |
| :-: | :-: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| 0 | 0 |   0   |   0   |   0   |   0   |   0   |   0   |   0   |   1   |   1   |   1   |   1   |   1   |   1   |   1   |   1   |   1   |
| 0 | 1 |   0   |   0   |   0   |   0   |   1   |   1   |   1   |   1   |   0   |   0   |   0   |   0   |   1   |   1   |   1   |   1   |
| 1 | 0 |   0   |   0   |   1   |   1   |   0   |   0   |   1   |   1   |   0   |   0   |   1   |   1   |   0   |   0   |   1   |   1   |
| 1 | 1 |   0   |   1   |   0   |   1   |   0   |   1   |   0   |   1   |   0   |   1   |   0   |   1   |   0   |   1   |   0   |   1   |

Епта...
Уж простите, но функции тут пронумерованы в шестнадцатеричной системе, отсюда и функции с номерами А, B и так далее, хотя Бирюков диктовал их как 10, 11 и так далее, как нормальный человек.

$f_0 = const0$
$f_F = const1$
$f_3 = a$
$f_5 = b$
$f_C = \overline{a}$
$f_A = \overline{b}$
$f_1 = a \cdot b$ - функция конъюнкции. Для n аргументов она принимает значение 1, когда все аргументы в наборе принимают значение 1. Ее инверсия $f_E = \overline{a \cdot b} = a / b$- штрих Шеффера.
$f_7 = a+b$- функция логического сложения. Для n аргументов принимает значение 1, если хотя бы один аргумент в наборе принимает значение 1. Ее инверсия $f_8 =\overline{a+b} = a↓b$ - стрелка Пирса.
$f_9 = a ≣ b$
$f_6 = a ⊕ b$
$f_D = a → b$
$f_2 = \overline{a→b}$
$f_B = b→a$
$f_4 = \overline{b→a}$

# Лекция 2

## Общий вид правила де Моргана

Если есть инверсия над сколь угодно сложным логическим выражением, то для его преобразования необходимо

1. все знаки логического умножения заменить на знаки логического сложения;
2. все знаки логического сложения заменить на знаки логического умножения;
3. взять инверсию над каждым аргументом.

## Минтермы и макстермы

Минтермом (m) называется логическое произведение всех переменных, входящих туда в прямом или инверсном виде.
Макстермом (M) называется логическая сумма всех переменных, входящих в макстерм в прямом или инверсном виде.


| a | b | m                          | M                             |
| --- | :-- | :--------------------------- | ------------------------------- |
| 0 | 0 | $\overline{a}\overline{b}$ | $\overline{a} + \overline{b}$ |
| 0 | 1 | $\overline{a}b$            | $\overline{a} + b$            |
| 1 | 0 | $a\overline{b}$            | $a + \overline{b}$            |
| 1 | 1 | $ab$                       | $a+b$                         |

Все минтермы и макстермы имеют свои номера. Минтермы нумеруются по порядку от 0, макстермы - в обратном порядке до 0.

## Свойства минтермов и макстермов

### Логические суммы/произведения всех минтермов/макстермов

$$
\vee^{2^{n-1}}_{i=0}m_i = 1 \newline
\wedge^{2^{n-1}}_{i=0}M_i = 0

$$

### Произведения/суммы различных минтермов/макстермов

$m_i \cdot m_j = 0$ при $i \neq j$.

$M_i + M_j = 1$ при $i \neq j$.

### Корреляция номеров минтермов и макстермов

$\overline{m_i} = M_{2^{n}-1-i}$

$\overline{ab\overline{c}} (m_6)= \overline{a} + \overline{b} + c (M_1)$

## СДНФ и СКНФ

> Для получения СДНФ (совершенной дизъюнктивной нормальной формы) переключательной функции необходимо:
>
> 1. Рассмотреть наборы, где функция принимает значение 1.
> 2. Если в наборе аргумент принимает значение 1, он записывается без инверсии, если значение 0 - то с инверсией. Между собой аргументы объединяются знаком логического умножения ($\cdot$).
> 3. Все полученные в пункте 2 формы записи объединяются между собой знаком логического сложения (+).

> Для получения СКНФ (совершенной конъюнктивной нормальной формы) переключательной функции необходимо:
>
> 1. Рассмотреть наборы, где функция принимает значение 0.
> 2. Если в наборе аргумент принимает значение 1, он записывается с инверсией, если значение 0 - то без инверсии. Между собой аргументы объединяются знаком логического сложения (+).
> 3. Все полученные в пункте 2 формы записи объединяются знаком логического умножения ($\cdot$).

### Пример


| a | b | c | f |
| --- | :-- | --- | --- |
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 0 |

Пусть есть переключательная функция $f_{106}.$ Тогда для нее

- СДНФ: $f_{106} = \overline{a}\overline{b}c + \overline{a}b\overline{c}+a\overline{b}\overline{c}+ab\overline{c} = m_1 + m_2 + m_4 + m_6$
- СКНФ: $f_{106} = (a+b+c)(a+\overline{b}+\overline{c})(\overline{a} + b + \overline{c})(\overline{a}+\overline{b}+\overline{c}) = M_7 + M_5 + M_3 + M_0$

Реализация любых совершенных форм всегда содержит максимум 3 уровня логических элементов.

## Запись переключательной функции в разных нормальных формах

> Дизъюнктивной НФ называется форма записи переключательной функции, которая содержит минтермы переменного ранга.
>
> Конъюнктивной НФ называется форма записи переключательной функции, которая содержит макстермы переменного ранга.

Переменный ранг - это когда вот так: $f = abcd + \overline{a}bc + \overline{c}\overline{d}$

Все совершенные формы обязательно содержат минтермы/макстермы одного ранга.

> Минимальной ДНФ называется форма записи переключательной функции, которая содержит минимальное количество минтермов минимального ранга.
>
> Минимальной КНФ называется форма записи переключательной функции, которая содержит минимальное количество макстермов минимального ранга.

## Методы минимизации

Основное условие при проектировании - минимальное количество логических элементов, за исключением случаев, когда требуется минимизировать задержку.

Существуют следующие основные методы минимизации переключательных функций:

1. Метод проб и ошибок
2. Метод Квайна
3. Метод Маккласки (или метод Квайна-Маккласки)
4. Метод диаграмм Вейтча

Первый метод неалгоритмичен и основан только на знании законов булевой алгебры. Он не гарантирует, что минимальная форма абсолютно минимальна.

Остальные методы дают полную гарантию получения минимальной формы и реализуются в машинах (в частности метод Квайна и метод Маккласки).

Метод диаграмм Вейтча прост, но не применим при большом (>5) количестве аргументов. Метод так же, как первый, основан на ручных вычислениях и обычно не встречается в машинах.

### Метод проб и ошибок

Пусть дана $f = abc + \overline{a}bc + a\overline{b}c+ ab\overline{c}.$

Записываем $abc$ 3 раза, потому что нам так позволяет закон повторения:

$f = abc + abc + abc + \overline{a}bc + a\overline{b}c+ ab\overline{c}$

Склеиваем эти $abc$ с каждым минтермом:

$abc + \overline{a}bc = bc$

$abc + a\overline{b}c = ac$

$abc + ab\overline{c} = ab$

Следовательно, $f = bc + ac + ab.$

### Метод Квайна

Этот метод строится на основном законе склеивания:

- $Ab + A\overline{b} = A$, где $A$ - сколь угодно сложное логическое выражение.
- $(A + b)(A + \overline{b}) = A$

Сам метод (для МДНФ):

1. Записываем переключательную функцию в СДНФ
2. Попарно проверяем минтермы на предмет склеивания. Склеиваем, где это возможно, и получаем минтермы на ранг ниже.
3. После первого перебора идет перебор полученных минтермов нижнего ранга. Если склеивать не получается, мы получаем простые импликанты, которые в дальнейших шагах не участвуют. Если есть что склеивать - склеиваем и идем дальше.
4. Продолжаем столько, сколько возможно.
5. Строим импликантную матрицу.
6. Из импликантной матрицы выбираем минимальное количество простых импликант, чтобы импликантная матрица перекрывалась полностью.

### Метод Маккласки

Это по факту дальнейшая оптимизация метода Квайна. Для сокращения количества переборов минтермы разбиваются на группы с отличием по одному аргументу. Дальше сравнение идет как в методе Квайна, но по группам.

Такое упрощение дает нам сокращение вычислительных затрат примерно на 30-40%.

# Лекция 3

## Метод Квайна-Маккласки

$f_{(4)} = 1(0, 1, 2, 3, 4, 6, 7, 8, 9, 11, 15)$

Найти МДНФ.

Группа 0: $m_0 = 0000$

Группа 1: $m_1 = 0001, m_2 = 0010, m_4 = 0100, m_8 = 1000$

Группа 2: $m_3 = 001, m_6 = 0110, m_9 = 1001$

Группа 3: $m_7 = 0111, m_{11} = 1011$

Группа 4: $m_{15}=1111$

Сравниваем группы 0-1:

```
000- (0-1) 
00-0 (0-2)
0-00 (0-4)
-000 (0-8)
```

Группы 1-2:

```
00-1 (1-3)
-001 (1-9)
00-1 (2-3)
0-10 (2-6)
01-0 (4-6)
100- (8-9)
```

Группы 2-3:

```
0-11 (3-7)
011- (6-7)
-011 (3-11)
10-1 (9-11)
```

Группы 3-4:

```
-111 (7-15)
1-11 (11-15)
```

0-1-1-2 группы:

```
00-- (0-1-2-3)
-00- (0-1-8-9)
00-- (0-2-1-3)
0--0 (0-2-4-6)
0--0 (0-4-2-6)
-00- (0-8-1-9)
```

1-2-2-3 группы:

```
-0-1 (1-3-9-11)
-0-1 (1-9-3-11)
0-1- (2-3-6-7)
0-1- (2-6-3-7)
```

2-3-3-4 группы:

```
--11 (3-11-7-15)
--11 (3-7-11-15)
```

Импликантная матрица:


|      | $m_0$ | $m_1$ | $m_2$ | $m_3$ | $m_4$ | $m_6$ | $m_7$ | $m_8$ | $m_9$ | $m_{11}$ | $m_{15}$ |
| ------ | ------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | ------- | ---------- | ---------- |
| 00-- | v     | v     | v     | v     |       |       |       |       |       |          |          |
| -00- | v     | v     |       |       |       |       |       | v     | v     |          |          |
| 0--0 | v     |       | v     |       | v     | v     |       |       |       |          |          |
| -0-1 |       | v     |       | v     |       |       |       |       | v     | v        |          |
| 0-1- |       |       | v     | v     |       | v     | v     |       |       |          |          |
| --11 |       |       |       | v     |       |       | v     |       |       | v        | v        |

Итого получили: $f = \overline{b}\overline{c} + \overline{a}\overline{d} + cd$

# Лекция 4

## Диаграммы Вейтча

Если количество переменных >6, метод практически неприменим. Диаграмма просто становится слишком большая.

Количество клеток в диаграмме всегда равно $2^n$.

На диаграмму Вейтча наносятся только дизъюнктивные формы.

Если имеется функция n аргументов, то минтерм $n$-ого ранга наносится на диаграмму одной единицей, минтерм $n-1$ ранга - двумя единицами, минтерм $n-2$ ранга - четырьмя и так далее: $N_{единиц}(n-k) = 2^k$.

## Правила склеивания минтермов

На диаграмме Вейтча склеиваются 2, 4, 8, 16 и так далее минтермов, **расположенных строго определенным образом.** Другое количество минтермов на диаграмме Вейтча никогда не склеивается.

Два минтерма объединяются на диаграмме Вейтча, если они расположены:

1. рядом в одной строке
2. рядом в одном столбце
3. на концах одной строки (то есть первый и последний)
4. на концах одного столбца (аналогично)

Если два минтерма расположены иным образом, их нельзя склеивать (кто еще не понял).

Четыре минтерма объединяются на диаграмме Вейтча, если они расположены:

1. одной строкой
2. одним столбцом
3. на концах двух **соседних (смежных)** строк
4. на концах двух **соседних (смежных)** столбцов
5. в любом месте диаграммы в виде квадрата
6. в углах диаграммы

Восемь минтермов объединяются на диаграмме Вейтча, если они расположены:

1. в виде двух **соседних** строк в любом месте диаграммы
2. в двух крайних строках
3. в виде двух **соседних** столбцов в любом месте диаграммы
4. в двух крайних столбцах

## Получение минимальных НФ

Если необходимо получить МДНФ, надо:

1. нанести переключательную функцию на диаграмму Вейтча
2. склеить нанесенные на диаграмму минтермы по известным правилам, при этом:
   - один и тот же минтерм может входить в несколько склеиваний
   - при склеивании необходимо выбирать минимальное количество склеиваний с максимальным количеством минтермов
   - если минтерм не склеивается, он входит в минимальную форму самостоятельно.
3. выписать в результат минтермы после объединения (просто написать МДНФ)

Если необходимо получить МКНФ, надо:

1. нанести инверсию исходной переключательной функции на диаграмму Вейтча
2. склеить нанесенные на диаграмму минтермы по известным правилам, при этом:
   - один и тот же минтерм может входить в несколько склеиваний
   - при склеивании необходимо выбирать минимальное количество склеиваний с максимальным количеством минтермов
   - если минтерм не склеивается, он входит в минимальную форму самостоятельно.
3. записать минимальную ДНФ для инверсии исходной функции
4. по правилу де Моргана преобразовать правую часть полученной записи и получить МКНФ исходной функции

### Неполностью определенная функция

Для получения МДНФ неполностью определенной переключательной функции необходимо:

1. нанести функцию на диаграмму там, где она принимает значение 1 и не определена, причем неопределенные значения отмечаются на диаграмме как $\times$
2. доопределить неопределенные значения или 0, или 1 так, чтобы выполнялось основное правило: количество склеиваний должно быть минимально, количество минтермов в каждом склеивании должно быть максимально
3. получить МДНФ и записать ее

Для получения МКНФ неполностью определенной переключательной функции необходимо:

1. нанести на диаграмму минтермы, где функция принимает значение 0 (инверсию исходной функции)
2. нанести на диаграмму минтермы, в которых функция не определена, обозначив их $\times$
3. доопределить неопределенные значения 0 или 1 так, чтобы выполнялось основное правило: количество склеиваний должно быть минимально, количество минтермов в каждом склеивании должно быть максимально
4. получить МДНФ инверсии исходной функции
5. по правилу де Моргана преобразовать правую часть полученной записи и получить МКНФ исходной функции

# Лекция 5

Минимальные формы не гарантируют построения самой оптимальной логической схемы.

## Пример

Берем базис из простых элементов И, ИЛИ, НЕ.

МДНФ $f_{(3)} = ab + ac + \overline{a}\overline{b}\overline{c}$.

3 - НЕ, 3 - И, 1 - ИЛИ

Всего получается 7 элементов, но можно преобразовать еще:

$f_{(3)} = ab + ac + \overline{a}\overline{b}\overline{c} = a(b+c) + \overline{a}\overline{b}\overline{c} = a(b+c) + \overline{(a+b+c)}$

Теперь у нас 1 - НЕ, 3 - ИЛИ, 1 - И. Всего 5 элементов.

## Еще пример для МКНФ

$f_{(3)} = (a + b)(a+c)(\overline{a}+\overline{b}+\overline{c})$

3 - НЕ, 3 - ИЛИ, 1 - И. Всего 7. Преобразуем:

$f_{(3)} = (a + b)(a+c)(\overline{a}+\overline{b}+\overline{c}) = (a+bc)(\overline{a}+\overline{b}+\overline{c}) = (a+bc)\overline{(abc)}$

## Канонические формы переключательных функций алгебры логики

Всего их 8.

$f_{(3)} = 1(0, 3, 6, 7)$

СДНФ: $f = \overline{a}\overline{b}\overline{c} + \overline{a}bc + ab\overline{c}+abc$

Начинаем страдать:

1. $f = \overline{\overline{\overline{a}\overline{b}\overline{c} + \overline{a}bc + ab\overline{c}+abc}}$ - базис И, ИЛИ, НЕ
2. $f = \overline{\overline{(\overline{a}\overline{b}\overline{c})}\cdot\overline{(\overline{a}bc)}\overline{(ab\overline{c})}\cdot\overline{(abc)}}$ - базис И-НЕ
3. $f = \overline{(a+b+c)(a+\overline{b}+\overline{c})(\overline{a}+\overline{b}+c)(\overline{a}+\overline{b}+\overline{c})}$ - базис И-НЕ, ИЛИ
4. $f = \overline{(a+b+c)}+\overline{(\overline{a}+\overline{b}+\overline{c})}+\overline{(\overline{a}+\overline{b}+c)}+\overline{(\overline{a}+\overline{b}+\overline{c})}$ - базис ИЛИ-НЕ, ИЛИ

Если необходимо проектировать устройство в одном из четырех заданных базисов, надо:

1. получить МДНФ
2. взять над полученным выражением двойную инверсию и с помощью правила де Моргана прийти к требуемому варианту реализации

А теперь берем СКНФ: $f_{(3)} = (a+b+\overline{c})(a+\overline{b}+c)(\overline{a}+b+c)(\overline{a}+b+\overline{c})$

Погнали страдать еще раз:

5. $f = \overline{\overline{(a+b+\overline{c})(a+\overline{b}+c)(\overline{a}+b+c)(\overline{a}+b+\overline{c})}}$ - базис И, ИЛИ, НЕ
6. $f = \overline{\overline{(a+b+\overline{c})}+\overline{(a+\overline{b}+c)}+\overline{(\overline{a}+b+c)}+\overline{(\overline{a}+b+\overline{c})}}$ - базис ИЛИ-НЕ
7. $f = \overline{(\overline{a}\overline{b}c)+(\overline{a}b\overline{c})+(a\overline{b}\overline{c})+(a\overline{b}c)}$ - базис ИЛИ-НЕ, И, **не всегда оптимален для МКНФ**
8. $f = \overline{(\overline{a}\overline{b}c)}\cdot\overline{(\overline{a}b\overline{c})}\cdot\overline{(a\overline{b}\overline{c})}\cdot\overline{(a\overline{b}c)}$ - базис И-НЕ, И

### Что когда брать

МДНФ брать для базисов

1. И, ИЛИ, НЕ
2. И-НЕ
3. И-НЕ, ИЛИ
4. ИЛИ-НЕ, ИЛИ

А МКНФ брать для базисов

1. И, ИЛИ, НЕ
2. ИЛИ-НЕ
3. ИЛИ-НЕ, И
4. И-НЕ, И

> И еще ремар(очка) от деда: И, ИЛИ-НЕ и ИЛИ-НЕ, И - это одно и то же; И-НЕ, ИЛИ и ИЛИ, И-НЕ - тоже одно и то же.

## Задача

$f_{(4)} = 1(0, 1, 2, 3, 6, 7, 8, 9, 14, 15)$ реализовать в И-НЕ, ИЛИ.

Берем МДНФ: $f_{(4)} = bc + \overline{b}\overline{c}+\overline{a}\overline{b}$

Еще есть вариант $f_{(4)} = bc + \overline{b}\overline{c}+\overline{a}с$, но пока мы поработаем с первым.

$\overline{\overline{bc + \overline{b}\overline{c}+\overline{a}\overline{b}}} = \overline{\overline{(bc)}\cdot\overline{(\overline{b}\overline{c})}\cdot(\overline{a}\overline{b})} = \overline{(\overline{b}+\overline{c})(b+c)(a+b)} = \overline{\overline{(bc)}(b+c)(a+b)}$

Сейчас у нас 2 элемента И-НЕ, 2 элемента ИЛИ. Теперь второй вариант:

$\overline{\overline{bc + \overline{b}\overline{c}+\overline{a}с}} = \overline{\overline{(bc)}\cdot\overline{(\overline{b}\overline{c})}\cdot\overline{(\overline{a}c)}} = \overline{(\overline{b}+\overline{c})(b+c)(a+\overline{c})} = \overline{\overline{(bc)}(b+c)(a+\overline{c})}$

А тут получилось 3 И-НЕ, 2 ИЛИ. Этот варик нас не устраивает, потому что мы уже нашли вариант с четырьмя элементами.

## Общий алгоритм проектирования устройства в заданном базисе логических элементов

1. Получить все минимальные формы
2. Прийти к требуемой канонической форме, используя двойную инверсию
3. Используя законы алгебры логики, упростить полученное выражение
4. Выбрать вариант с минимальным количеством логических элементов
5. Синтезировать графическое изображение проектируемого устройства

## Проектирование схем с несколькими выходами

Есть устройство с двумя входами и тремя выходами, которое надо спроектировать в классическом базисе И, ИЛИ. НЕ.

Пусть

$y_1 = a+b, y_2 = \overline{a}\cdot\overline{b}, y_3 = (a+\overline{b})(\overline{a}+b)$

Если требуется спроектировать максимально надежное устройство, то каждый выход проектируется отдельной схемой. Но если требуется спроектировать устройство с минимальным количеством элементов, мы делаем следующее:

$$
y_1 = a + b \\
y_2 = \overline{a+b} = \overline{a}\cdot\overline{b} = \overline{y_1} \\
y_3 = (a+\overline{b})(\overline{a}+b) = (\overline{a}\overline{b})(ab) = y_2 \cdot (ab)

$$

И так из схемы из 9 элементов мы получаем схему из четырех.

# Лекция 6

## Проектирование схем без памяти и двоично-десятичное кодирование

Когда нужно построить схему с несколькими выходами, все переключательные функции наносятся на диаграмму Вейтча. Затем выделяются их общие части.

*(дальше я немного проспал)*

Логическое вычитание можно заменить логическим умножением, если взять от него инверсию.

## Двоично-десятичное кодирование

> Система, в которой каждая десятичная цифра кодируется четырьмя двоичными разрядами, называется двоично-десятичной.

Необходимо, чтобыкоды имели свойства:

1. единственности
2. упорядоченности
3. четности
4. самодополняемости
5. взвешенности


| Код/цифра | 8421 | 8421+3 | 8421+6 | 2421 | 5421 | 5121 | 753-6 |
| ------------------- | ------ | :------- | -------- | ------ | ------ | ------ | :------ |
| 0                 | 0000 | 0011   | 0110   | 0000 | 0000 | 0000 | 0000  |
| 1                 | 0001 | 0100   | 0111   | 0001 | 0001 | 0001 | 1001  |
| 2                 | 0010 | 0101   | 1000   | 0010 | 0010 | 0010 | 0111  |
| 3                 | 0011 | 0110   | 1001   | 0011 | 0011 | 0011 | 0010  |
| 4                 | 0100 | 0111   | 1010   | 0100 | 0100 | 0111 | 1011  |
| 5                 | 0101 | 1000   | 1011   | 1011 | 1000 | 1000 | 0100  |
| 6                 | 0110 | 1001   | 1100   | 1100 | 1001 | 1001 | 1101  |
| 7                 | 0111 | 1010   | 1101   | 1101 | 1010 | 1010 | 1000  |
| 8                 | 1000 | 1011   | 1110   | 1110 | 1011 | 1011 | 0110  |
| 9                 | 1001 | 1100   | 1111   | 1111 | 1100 | 1111 | 1111  |

Все написанные коды, кроме последнего, используются в вычислительной технике. Последний код используется крайне редко.

Название каждого кода состоит из весов.

Разберем это все.

### Взвешенность

В коде 7 записывается как 0111: $0\cdot8 + 1\cdot4 + 1\cdot2 + 1\cdot1 = 7$. Числа, на которые мы домножаем, и являются весами.

### Упорядоченность

Это когда в коде каждый последующий код отличается на 1 от предыдущего.

### Четность

У четных цифр - четная комбинация (заканчивается на 0), у нечетных - нечетная (заканчивается на 1).

# Лекция 7

Пусть дан код 8-4-2-1. На примере этого кода рассмотрим **алгоритм выполнения домашки.**

$$
T(A) = \alpha_1\alpha_2\alpha_3\alpha_4 \\
T(B) = \beta_8\beta_4\beta_2\beta_1 \\
---------------------------\\
T(C) = \gamma_8\gamma_4\gamma_2\gamma_1\\

$$

Вводим коррекцию:

![](assets/20250228_131533_IMG_7492.png)

> Если величина сложения меньше 10, коррекция не нужна. Если больше или равна 10, то нужно вводить коррекцию.

> В коде 8421 существует 10 используемых и 6 неиспользуемых комбинаций. Все комбинации 1010...1011 в данном случае не используются и называются **запрещенными.**

Если от сложения двух одноразрядных чисел получается запрещенная комбинация или единица переноса, то нужна коррекция, равная здесь по величине 0110. Иначе коррекция не нужна.

Получается, что результат первого вычисления правилен не всегда. Правильно (с коррекцией) делать так:

$$
T(A) = \alpha_1\alpha_2\alpha_3\alpha_4 \\
T(B) = \beta_8\beta_4\beta_2\beta_1 \\
---------------------------\\
T(C) = \gamma'_8\gamma'_4\gamma'_2\gamma_1\\

+ 0 1 1 0 \\
---------------------------\\
T(C) = \gamma_8\gamma_4\gamma_2\gamma_1\\

$$

По факту сложение имеет две ступени: получение некорректированной величины и корректировка (при необходимости).

Схема первой ступени выглядит так:

![](assets/20250228_133057_IMG_7495.png)

Мистический элемент по центру - схема коррекции. Она возвращает 1, если требуется коррекция, и 0, если она не требуется. Далее подключением к правильным сумматорам формируется дополнительный код, который прибавляется при коррекции.

Функция коррекции основана на функции запрещенных комбинаций: $F_к = F_{зк} + \prod'_i$. Строится она следующим образом:

![](assets/20250228_133813_IMG_7496.png)

$$
F_к=\gamma'_8(\gamma'_2+\gamma'_4) + \prod'_i \\
\prod_i
$$

Корректирующая величина может возникать, если
1. получается запрещенная комбинация
2. получается запрещенная комбинация в совокупности с промежуточным результатом
3. внутри полученной тетрады возникает сочетание определенных сигналов

Как правило, бывает **не более двух корректирующих комбинаций.** Если их больше - значит, что-то идет капитально не так.

В домашке понадобится
1. спроектировать одноразрядный двоичный сумматор в определенном базисе согласно критериям проектирования
2. собрать схему преобразователя и схему, фиксирующую перевыполнение


При проектировании двоично-десятичных устройств практически всегда берется обратный код для более простой работы с отрицательными числами.