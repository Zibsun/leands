# Приоритизация ICE/RICE

## Какую проблему решаем

Бэклог заполнен интересными и ценными идеями (продуктовыми гипотезами). С какой из них имеет смысл начинать? Разумеется, с той, что принесет максимальное количество денег! Но как это определить?

Почему бы не спросить у бизнеса?

Вы приходите к самому важному руководителю и он методом пристального взгляда легко определяет ту, которая ему покажется максимально полезной. Предположим, он не ошибается и она действительно самая ценная. Действительно ли с нее нужно начинать?

Вообще говоря нет! Чтобы принять решение о приоритете, нужно знать еще и трудозатраты на реализацию гипотезы.

Предположим, наиболее ценная гипотеза способна принести $1млн, а следующие три только по $0.5 млн. Пусть трудозатраты на реализацию первой — 9 месяцев, а для каждой из трех других по три месяца. Получается, за 9 месяцев работы мы могли бы сделать три простых гипотезы и заработать $1.5 млн, а вместо этого потратим их на первую гипотезу и заработаем только $1млн.

Давайте теперь вспомним, что все идеи из нашего бэклога — гипотезы, и мы вообще можем не суметь их реализовать. Нам нужно каким-то образом учесть вероятность достижения успеха.

## Приоритизация методом ICE

Для гипотез из нашего бэклога нужно вычислить Score по следующей формуле:

![ICE Formula](../_images/prioritization-formula.png)

Чем выше получившийся Score, тем выше приоритет.

Давайте теперь рассмотрим множители нашей формулы.

## Impact

!> Impact — это мера влияния на итоговый результат с точки зрения бизнеса.

Очень часто мы не можем посчитать ее в конкретных деньгах — рублях или долларах:

* Недостаточно данных для более-менее точных расчетов
* Гипотеза сама по себе ценности не несет, но позволит открыть дорогу другим ценным гипотезам
* Ценность для бизнеса может быть не связана напрямую с доходом (например, цели связаны с захватом новых рынков или обеспечением требований со стороны регулятора)

Однако мы неплохо можем оценить ценность одной гипотезы относительно другой.

|     Категория   |     Impact     (value points)    |
|-----------------|----------------------------------|
|     Massive     |                 3                |
|     High        |                 2                |
|     Medium      |                 1                |
|     Low         |                0.5               |
|     Very low    |                0.25              |

Поэтому удобно оценивать ценность в относительных единицах.

Мы обычно используем набор фиксированных категорий с указанными оценками Impact как в таблице справа. Мы выбираем из бэклога среднюю по влиянию гипотезу в качестве эталонной. Она становится Medium и ее Impact равен 1. Если другая гипотеза в два раза более ценная, то ее Impact  равен 2. Если в два раза менее ценная, чем эталонная, то 0.5. Если гипотеза кажется очень ценной, ее Impact может достигать трех. И так далее.

## Effort

!> Effort — оценка трудозатрат на реализацию гипотезы.

Посчитать трудозатраты в человеко-часах или днях просто невозможно:

* Данных недостаточно для точного расчета
* Мы не знаем пока, с какими трудностями мы столкнемся по ходу реализации
* Трудозатраты окажутся разными для разных исполнителей: оценка опытного сайентиста будет отличаться в разы от оценки джуна

Точно также, как и в случае Impact, воспользуемся оценкой в относительных единицах. В литературе их называют Story Points.

Часто используют прогрессивные шкалы, например последовательность Фибоначчи или степеней двойки, чтобы не спорить, например, какова сложность гипотезы — 5 или 6 пойнтов.

Обычно выбирают одну простую в реализации гипотезу и обозначают ее за 1 SP (story points). Если гипотеза кажется в два раза сложнее эталонной, то ее оценка будет равна 2 SP. И так далее.

## Confidence

!> Confidence — это оценка вероятности (уверенности) в том, что гипотеза может быть реализована и окажет нужный бизнес эффект

Удобнее всего confidence измерять в процентах.

Очевидно, что confidence не может превышать 100%. Опять-таки, лучше использовать набор фиксированных категорий с соответствующими оценками Confidence.


|     Category    |     Confidence    |
|-----------------|-------------------|
|     High        |          100%     |
|     Medium      |           80%     |
|     Low         |           50%     |
|     Very low    |           10%     |

## Как провести сессию по приоритизации гипотез

У каждого из заинтересованных лиц и членов команды может быть свое представление о степени влияния на бизнес, трудозатратах и уверенности в результате для гипотез из бэклога. Лучше всего провести совместную сессию и согласовать свои представления.

Один из интересных вариантов — использовать Planning Poker. Давайте рассмотрим это на примере оценки трудозатрат.

![Planning Poker Cards](../_images/prioritization-pokercards.png)


* Сначала участники совместно выбирают эталонную гипотезу. Она должна быть простой и понятной. Мы обозначаем ее за 1 Story Point.
* Каждый участник получает колоду карт с последовательностью Фибоначчи
* Ведущий представляет следующую гипотезу
* Участники выбирают из своей колоды предполагаемую оценку (во сколько раз гипотеза больше эталонной) и выкладывают карту рубашкой вверх
* По команде ведущего карты вскрываются
* Те, кто выкинул максимальную и минимальную оценку, аргументируют их
* Процедура повторяется, пока мы не сойдемся достаточно близко.
* Итоговое значение записывается, мы двигаемся к следующей гипотезе

Аналогичным образом можно оценивать и Impact и Confidence. После этого мы считаем скоры и получаем финальную оценку приоритета.


## Приоритезация при помощи RICE

В некоторых случаях удобно разделить Impact на два множителя — Reach и Impact. Тогда формула будет выглядеть так:

![RICE](../_images/prioritization-rice.png)

!> Reach — оценка охвата гипотезы.

В зависимости от контекста конкретного бизнеса, она может быть выражена в количестве пользователей, заказах, транзакциях и так далее.

Impact — мера влияния на итоговый бизнес-результат для одной единицы в reach.

Например, вы продаете Data Products банкам. Тогда Impact — оценка влияния гипотезы на конкретный банк. Например, одна гипотеза может быть очень нужна условному усредненному банку и ее Impact = 3. Ценность другой гипотезы равна 1. Однако рынок (пропорциональный количеству банков, способных потенциально заинтересоваться соответствующим продуктом) для первой гипотезы большой и равен 3, а для другой гипотезы рынок в три раза меньше и равен 1.

## Особенности проведения приоритизации

* Приглашайте DS команду участвовать в сессии приоритизации. Обсуждение Impact и Confidence заинтересованных лиц дает им огромное количество контекста, тем самым вовлекает в работу и помогает принимать решения лучше
* Члены DS команды могут не хотеть участвовать. Объясните, что без оценки Effort приоритизация будет ошибочной, а оценку трудозатрат могут сделать только они
* Оценка Score не является абсолютно верной и финальной. Постфактум можно убедится, что мы часто ошибаемся в оценках и, как следствие, приоритетах. Однако наличие правил приоритизации позволяет выигрывать в среднем, на большом количестве гипотез
* В оценке трудозатрат участвуют только непосредственные исполнители то есть те, кто будет делать работу руками. Обычно у представителей бизнеса слишком заниженные оценки трудозатрат

## Как развивать подход к приоритизации

В вашей организации подход к приоритизации будет развиваться со временем. Вот несколько идей, как и куда его можно улучшать:

* Confidence можно разделить отдельно на два множителя — вероятность успеха с точки зрения бизнеса и техническую реализуемость
* Шкалу Confidence можно стандартизировать с помощью набора критериев. Например, наличие аналогичного кейса в вашей стране, проведенный A/B-тест, посчитанная бизнес модель и т.д. повышает уверенность
* Точно также можно ввести шкалу критериев для Impact

В процесс приоритизации может вмешаться высокое руководство и внезапно повысить приоритет каких-то гипотез и тем самым обесценить вклад участников процесса.

Очень хорошо работает приглашение руководства на следующую сессию приоритизации.

Волюнтаристски изменить приоритет будет невозможно. Вместо этого они будут стараться убедить в более высоком импакте или уверенности.

![Prioritization](../_images/prioritization-meme.png)

## Зачем нужна приоритизация

Давайте перечислим несколько преимуществ приоритизации

* Позволяет максимизировать доход для бизнеса
* Отсекает ненужные и малоперспективные работы
* Позволяет договариваться различным заинтересованным лицам о приоритетах

## Когда не надо использовать ICE/RICE

* ICE/RICE предназначен для приоритизации исключительно продуктовых гипотез. Дата- и метод- гипотезы не имеют отдельной от продуктовой гипотезы ценности. Подход к приоритизации таких гипотез описан в главе о декомпозиции продуктовых гипотез
* Если у вашей команды небольшое количество продуктовых гипотез (скажем, 1-3), использовать сложный метод приоритизации, очевидно, не имеет смысла.

## Когда использовать ICE/RICE

* На уровне команды — если у вашей команды много продуктовых гипотез в бэклоге
* На уровне организации — можно иметь один общий бэклог из продуктовых гипотез на нескольких команд и приоритизировать его перед передачей конкретной команде на реализацию

?> Подход ICE был предложен Шоном Эллисом (Sean Ellis), автором термина growth hacking