# Вопросы (Questions)

## Story questions

1. Как будет работать сервис, когда модель выйдет в прод?
2. Какие технические ограничения существуют для сервиса?
3. Какие системы и команды зависят от сервиса?
4. Как проводить валидацию модели в проде (А/Б-тест, ...)? Как валидация должна быть устроена?
5. Что будет, если сервис откажет?
6. Насколько быстро меняются данные, Как часто нужно повторно обучать модель?
7. Как будет производится мониторинг работы модели и сервиса в проде?

## Data questions

1. Достаточно ли данных для обучения модели?
2. Есть ли в данных для обучения предсказательная сила для решаемой задачи?
3. Качество данных достаточно для использования в модели?
4. Есть ли разметка?
5. Можно ли купить дополнительные данные?
6. Можно ли использовать публично доступные данные?
7. Заражены ли данные предрассудками (biased)?
8. Как модель будет получать данные в проде?
9. Совпадают ли данные в трейне и проде?
10. Как контролировать качество данных в проде?
11. Как сохранить качество данных после выхода в прод?
12. Какие юридические риски связаны с использованием данных?
13. Есть ли какие-то требования к данным, связанные с законодательным регулированием?

## Method questions

1. Есть ли SOTA (State of the Art) для задачи? Какие у нее значения мер качества?
2. Как эту работу делают эксперты (Subject Matter Expert) сейчас?
3. Требуется ли интерпретируемость модели?
4. Требуется ли внешняя независимая валидация модели?

## Примеры использования вопросов

Давайте рассмотрим несколько примеров применения этих вопросов при декомпозиции продуктовой гипотезы.

**Как будет работать сервис, когда модель выйдет в прод?**

> Модель должна как-то взаимодействовать с окружением. Понимаем ли мы как модель будет интегрирована с существующими продуктами? Например, у нас есть пользовательская история “Интерфейс для выбора подсказки”. Такой интерфейс не может работать без того, чтобы текущая система обращалась к модели, передавала туда запрос и получала сгенерированные подсказки. Есть ли задача на такую интеграцию на доске? Если такой задачи нет, ее нужно добавить в виде Technical Task.

**Требуется ли интерпретируемость модели?**

> Если требуется интерпретируемость модели, то мы скорее всего не сможем использовать CNN или LSTM для реализации модели и нам нужно убрать эти гипотезы из декомпозиции и добавить вместо них другие, более интерпретируемые модели.

**Достаточно ли данных для обучения модели?**

> Если данных не достаточно, то вся наша декомпозиция теряет смысл! Нам прежде всего нужно ответить на этот вопрос. Это супер критический риск и мы поместим его в самый центр в RAT.

**Как эту работу делают эксперты (Subject Matter Expert) сейчас?**

> При декомпозиции мы набросали много довольно сложных моделей, подготовка которых займет заметное время. Знаем ли мы как решается задача сейчас? Может быть есть простой набор правил, которые хорошо работают и которые можно использовать как бейзлайн для нашей задачи.

**Можно ли использовать публично доступные данные?**

> В задачах работы с текстами могут помочь внешние публично доступные наборы данных. Их добавление в процессе обучения может заметно повысить качество работы. Знаем ли мы о таких наборах данных? Где их достать? Как использовать? Эти вопросы тоже можно добавить на доску.
