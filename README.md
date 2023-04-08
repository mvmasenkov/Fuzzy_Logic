# Fuzzy_Logic
Задание: 
-	Выбрать объект управления/прогнозирования. Привести полное словесное описание выбранной модели. Входных переменных должно быть не менее трёх. 
-	Для каждой входной и выходной переменной подобрать функции принадлежности. 
-	Рассмотреть различные варианты функций принадлежности для каждой из переменных. Проанализировать полученный результат. 
-	Составить базу правил. База должна содержать не менее 15 и не более 
50 правил. 
-	Подобрать подходящий метод дефаззификации. Выбор обосновать. 
-	Реализовать модель в любой программной среде. 
-	Привести репрезентативное количество примеров работы построенной системы, отражающих различные отклики на выходе. 
-	Проанализировать результаты. 
-	Оформить отчёт, который должен содержать: 
•	описание задачи; 
•	для каждой переменной все рассмотренные варианты функций принадлежности;
•	обоснование конечного выбора функций принадлежности; 
•	база правил; 
•	скриншоты реализации в выбранной программной среде (не менее 
10 различных примеров); 
•	модель на внешнем носителе.

 
Ход работы: 
В качестве объекта управления/прогнозирования была выбрана «оценка вероятности выдачи кредитной карты». Это так называемая «скоринговая система», которая позволяет снизить издержки 
и минимизировать операционный риск за счет автоматизации принятия решения о выдачи кредитной карты заявителю. Система «оценки вероятности выдачи кредитной карты» является распространенным методом контроля рисков в финансовой индустрии. Данная система оценки использует личную информацию и данные, предоставленные заявителями, чтобы предсказать вероятность будущих неплатежей и оценить величину риска для банка. Банк оставляет за собой право одобрения выдачи кредитной карты заявителю. 
В качестве входных переменных будем рассматривать информацию, представленную заявителями:
-	годовой доход заявителя (низкий, средний, высокий) долларов/год;
-	категория получения дохода (низкая, средняя, высокая);
-	уровень образования (низкий, средний, высокий);
-	количество членов семьи (мало, средне, много). 
В качестве выходной переменной у нас будет:
-	одобрение выдачи кредитной карты (да, скорее всего да, скорее всего нет, нет).
Для каждой входной и выходной переменной подобрать функции принадлежности. Для входных переменных функции принадлежности диапазонов M (малых), D (больших) были стандартные, а точнее имели 
вид Z, S - функций. 
Для диапазонов S (средних) использовалась двухсторонняя гауссовская функция принадлежности.
-	годовой доход заявителя (низкий, средний, высокий) долларов/год
-	категория получения дохода (низкая, средняя, высокая);
-	уровень образования (низкий, средний, высокий);
-	количество членов семьи (мало, средне, много). 

Для выходной переменной функция принадлежности имеет линейный вид, одобрение выдачи кредитной карты (да, скорее всего да, скорее всего нет, нет).

Функция принадлежности нечёткого множества представляет степень принадлежности каждого объекта пространства рассуждения к определённому нечёткому множеству. Нечёткие методы предназначены для решения задачи классификации. По данным обучающей выборки для каждой переменной определяется количество объектов, которые попадают в заранее определённые интервалы. Для входных переменных рассмотрим различные варианты функций принадлежности:
-	годовой доход заявителя (низкий, средний, высокий) 
долларов/год. Если максимальное количество значений приходится на интервал «низкий» от 0 до 30 000 долларов/год, 
а интервалы «средний» и «высокий» являются пустыми, 
то считается, что переменная, описывающая заданный признак соответствует интервалу «низкий». Соответственно функция принадлежности имеет вид Z - функций. Если максимальное количество значений приходится на интервал «средний» 
от 31 000  долларов/год до 69000 долларов/год, а интервалы «низкий» и «высокий» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «средний». Соответственно функция принадлежности имеет вид двухсторонней гауссовской функции. Если максимальное количество значений приходится на интервал «высокий» от 70 000 долларов/год до 100000 долларов/год, 
а интервалы «низкий» и «средний» являются пустыми, 
то считается, что переменная, описывающая заданный признак соответствует интервалу «высокий». Соответственно функция принадлежности имеет вид S - функций.
-	категория получения дохода (низкая, средняя, высокая). Если максимальное количество значений приходится на интервал «низкая» от 0 до 30 (студент, пенсионер), а интервалы «средняя» и «высокая» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «низкая». Следовательно функция принадлежности имеет 
вид Z - функций. Если максимальное количество значений приходится на интервал «средняя» от 31 до 69 (пенсионер, рабочий, гос. служащий), а интервалы «низкая» и «высокая» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «средняя». Следовательно функция принадлежности имеет вид двухсторонней гауссовской функции. Если максимальное количество значений приходится на интервал «высокая» 
от 70 до 100 (гос. служащий, коммерсант), а интервалы «низкая» и «средняя» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «высокая». Следовательно функция принадлежности имеет 
вид S - функций.
-	уровень образования (низкий, средний, высокий). Если максимальное количество значений приходится на интервал «низкий» от 0 до 30 (неполное среднее, среднее / средне-специальное), а интервалы «средний» и «высокий» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «низкий». Следовательно функция принадлежности имеет вид Z - функций. Если максимальное количество значений приходится на интервал «средний» от 31 до 69 (среднее / средне-специальное, неполное высшее, высшее), а интервалы «низкий» и «высокий» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «средний». Следовательно функция принадлежности имеет вид двухсторонней гауссовской функции. Если максимальное количество значений приходится на интервал «высокий» от 70 до 100 (высшее, наличие учёной степени), а интервалы «низкий» и «средний» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «высокий». Следовательно функция принадлежности имеет вид S - функций.
-	количество членов семьи (мало, средне, много). Если максимальное количество значений приходится на интервал «мало» от 1-го до 2-х человек, а интервалы «средне» и «много» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «мало». Следовательно функция принадлежности имеет вид Z - функций. Если максимальное количество значений приходится на интервал «средне» от 3-х до 7-ми человек, а интервалы «мало» и «много» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «средне». Следовательно функция принадлежности имеет вид двухсторонней гауссовской функции. Если максимальное количество значений приходится на интервал «много» от 8-ми 
до 10-ти человек, а интервалы «мало» и «средне» являются пустыми, то считается, что переменная, описывающая заданный признак соответствует интервалу «много». Следовательно функция принадлежности имеет вид S - функций.


В качестве выходной переменной у нас будет:
-	одобрение выдачи кредитной карты (да, скорее всего да, скорее всего нет, нет). Если значение приходится на интервал от 0 до 0,2, то считается, что переменная, описывающая заданный признак соответствует интервалу «да». Функция принадлежности имеет линейный вид. Если значение приходится на интервал от 0,1 до 0,5, то считается, что переменная, описывающая заданный признак соответствует интервалу «скорее всего да». Функция принадлежности имеет линейный вид. Если значение приходится на интервал от 0,4 до 0,8, то считается, что переменная, описывающая заданный признак соответствует интервалу «скорее всего нет». Функция принадлежности имеет линейный вид. Если значение приходится на интервал от 0,7 до 0,9, 
то считается, что переменная, описывающая заданный признак соответствует интервалу «нет». Функция принадлежности имеет линейный вид.

База правил:
1.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «низкий», количество членов семьи «мало», то одобрение выдачи кредитной карты «нет».
2.	Если годовой доход заявителя «низкий», категория получения дохода «средняя», уровень образования «низкий», количество членов семьи «мало», то одобрение выдачи кредитной карты «нет».
3.	Если годовой доход заявителя «низкий», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «мало», то одобрение выдачи кредитной карты «нет».
4.	Если годовой доход заявителя «низкий», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «нет».
5.	Если годовой доход заявителя «низкий», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего нет».
6.	Если годовой доход заявителя «низкий», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего нет».
7.	Если годовой доход заявителя «низкий», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего нет».
8.	Если годовой доход заявителя «низкий», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего нет».
9.	Если годовой доход заявителя «средний», категория получения дохода «низкая», уровень образования «низкий», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
10.	Если годовой доход заявителя «средний», категория получения дохода «низкая», уровень образования «низкий», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего да».
11.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «низкий», количество членов семьи «мало», то одобрение выдачи кредитной карты «скорее всего да».
12.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «низкий», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
13.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
14.	Если годовой доход заявителя «средний», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
15.	Если годовой доход заявителя «средний», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
16.	Если годовой доход заявителя «средний», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «мало», то одобрение выдачи кредитной карты «скорее всего да».
17.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «мало», то одобрение выдачи кредитной карты «да».
18.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «высокий», количество членов семьи «мало», то одобрение выдачи кредитной карты «да».
19.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «да».
20.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «высокий», количество членов семьи «много», то одобрение выдачи кредитной карты «да».
21.	Если годовой доход заявителя «высокий», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «мало», то одобрение выдачи кредитной карты «да».
22.	Если годовой доход заявителя «высокий», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «да».
23.	Если годовой доход заявителя «высокий», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «много», то одобрение выдачи кредитной карты «да».
24.	Если годовой доход заявителя «высокий», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «мало», то одобрение выдачи кредитной карты «да».
25.	Если годовой доход заявителя «высокий», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «да».
26.	Если годовой доход заявителя «высокий», категория получения дохода «высокая», уровень образования «высокий», количество членов семьи «много», то одобрение выдачи кредитной карты «да».
27.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «мало», то одобрение выдачи кредитной карты «да».
28.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «да».
29.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «много», то одобрение выдачи кредитной карты «да».
30.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «низкий», количество членов семьи «мало», то одобрение выдачи кредитной карты «да».
31.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «низкий», количество членов семьи «средне», то одобрение выдачи кредитной карты «да».
32.	Если годовой доход заявителя «высокий», категория получения дохода «средняя», уровень образования «низкий», количество членов семьи «много», то одобрение выдачи кредитной карты «да».
33.	Если годовой доход заявителя «высокий», категория получения дохода «низкая», уровень образования «низкий», количество членов семьи «много», то одобрение выдачи кредитной карты «да».
34.	Если годовой доход заявителя «средний», категория получения дохода «высокая», уровень образования «средний», количество членов семьи «мало», то одобрение выдачи кредитной карты «скорее всего да».
35.	Если годовой доход заявителя «средний», категория получения дохода «низкая», уровень образования «высокий», количество членов семьи «мало», то одобрение выдачи кредитной карты «скорее всего да».
36.	Если годовой доход заявителя «средний», категория получения дохода «низкая», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
37.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «высокий», количество членов семьи «мало», то одобрение выдачи кредитной карты «скорее всего да».
38.	Если годовой доход заявителя «средний», категория получения дохода «низкая», уровень образования «высокий», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего да».
39.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «скорее всего да».
40.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «высокий», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего да».
41.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «мало», то одобрение выдачи кредитной карты «скорее всего да».
42.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего да».
43.	Если годовой доход заявителя «средний», категория получения дохода «средняя», уровень образования «средний», количество членов семьи «много», то одобрение выдачи кредитной карты «скорее всего да».
44.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «низкий», количество членов семьи «средне», то одобрение выдачи кредитной карты «нет».
45.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «низкий», количество членов семьи «много», то одобрение выдачи кредитной карты «нет».
46.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «средний», количество членов семьи «средне», то одобрение выдачи кредитной карты «нет».
47.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «средний», количество членов семьи «много», то одобрение выдачи кредитной карты «нет».
48.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «высокий», количество членов семьи «средне», то одобрение выдачи кредитной карты «нет».
49.	Если годовой доход заявителя «низкий», категория получения дохода «низкая», уровень образования «высокий», количество членов семьи «много», то одобрение выдачи кредитной карты «нет».

