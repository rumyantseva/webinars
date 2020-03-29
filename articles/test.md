1. Выберите некорректное объявление:
* `var c, python, java = true, false, "no!"`
* `var x := 23` (верно)
* `t := false`
* `var x int`

2. Нулевое значение для типа "map":
* `0`
* `nil` (верно)
* `interface{}`

3. Имена, экспортируемые из модуля:
* начинаются с `_`
* объявляются с ключевым словом `export`
* начинаются с заглавной буквы (верно)

4. Найдите некорректное объявление:
* `func add(x int, y int) int`
* `func swap(x, y string) (string, string)`
* `func split(sum int) (x, y int)`
* `func div(x int, y int) int, float` (верно)

5. функция recover(): 
* необходимая для реализации интерфейса Error
* используется в "отложенных" функциях для обработки паники (верно)
* используется для выхода из блока try ... except

6. Что выведет на экран следующая программа?
```
primes := [6]int{2, 3, 5, 7, 11, 13}
var s []int = primes[1:4]
fmt.Println(len(s), cap(s))
```
* 4 5
* 3 5 (верно)
* 3 6
* 4 6

7. горутина (goroutine) - это 
* базовый интерфейс
* легковесный тред (верно)
* другое название для POSIX thread-ов
* замыкание функции

8. Программисты на Go очень хотят видеть в языке
* множественное наследование
* дженерики (верно)
* динамическую типизацию

9. Может ли Go автоматически определять тип переменных
* Нет, Go статически типизирован, поэтому тип нужно всегда указывать явно
* Да, в Go есть система вывода типов Хиндли-Милнера, поэтому типы указывать вообще не нужно
* Да, для этого есть ключевое слово `auto`
* Да, для этого есть специальный оператор `:=`   (верно)

10. С помощь какого типа данных в Go представляются строки ?
* `[]char`
* `\*byte`
* `string`   (верно)
* `String`

11. Каким значением инициализируется переменная `res` в коде
```
func Concat(parts ...string) string {
    var res string  // вот 
}
```
* `nil`
* `""`  (верно)
* компилятор сообщит об ошибке
* поведение не определено, компилятор покажет предупреждение

12. Возможно ли стравнивать между собой (`==`) переменные типов `float32` и `int32`
* Да, Go преобразует тип и сравнит значения
* Да, Go автоматически округлит значение с плавающей точкой
* Нет, переменные разных типов нельзя сравнивать  (верно)

13. Как в Go выглядит преобразование типа `int32` в `int64`
* `a := (int64)b`
* `a := cast(b to int64)
* `a := int64(b)`    (верно)
* `a := b.(int64)`

14. Константы в Go объявляются
* С помощью ключевого слова `const`, например `const x = 3`  (верно)
* C помощью модификатора `const`, например `const var x = 3`
* С помощью модификатора `final`, наприме `final var x = 3`
* C помощью макроса `#define`, например `#define x 3`

15. Для создания сложных типов данных (содержащих значения разных элементарных типов) в Go используется
* Структуры, ключевое слово `struct`   (верно)
* Классыы, ключевое слово `class`
* Интерфейсы, ключевое слово `interface`
* Перечисления, ключевое слово `enum`

16. Какое из указанных слов НЕ является ключевым в Go
* `while`   (верно)
* `import`
* `go`
* `package`

17. CGO это
* Механизм вызова функций на языке C из Go кода (верно)
* Компилятор из языка Go в С
* Препроцессор, позволяющий использовать макросы в Go

18. Каналы в языке Go это
* Тип для чтения и записи данных в файл
* Тип данных для синхронизации и передачи данных между горутинами (верно)
* Библиотека для работы с TCP протоколом

19. В чем отличие буферизованных и небуферизованных каналов ?
* Буферизованные каналы обладают большей производительностью
* Запись в буферизованный канал никогда не блокирует горутину
* Запись в буферизованный канал не блокирует горутину, если есть место в буфере (верно)  

20. Есть ли в языке Go мьютексы (mutex) ?
* Есть, но это внутренний механизм, он не доступен в стандартной библиотеке
* Есть, тип sync.Mutex (верно)
* Нет, вместо них в Go используются каналы

21. Для чего используется контекст (context) в Go ?
* Для расширения синтаксиса языка 
* Для ограничения времени (или отмены) выполнения горутин (верно)
* Для создания совместного доступа к глобальным переменным из разных горутин

22. Как определяется что тип данных реализует некоторый интерфейс в Go ?
* С помощью ключевого слова implements
* С помощью ключевого слова extends
* Автоматически, если в типе реализованы все нужные методы (верно)

23. Что дает рефлексия (reflect) в Go ?
* Возможность определить тип данных скрывающийся за интерфейсом (верно)
* Возможность создавать функции, которые вызывают сами себя
* Возможность создавать типы данных, ссылающиеся на себя, например связанные списки.

24. В процессе получения данных (по протоколу TCP) с удаленного сервера у него пропало питание. Как обработать это в языке Go ?
* Метод Read немедленно вернет сетевую ошибку, нужно ее обработать
* Метод Read немедленно вернет ошибку EOF, нужно ее обработать
* Необходимо заранее установить таймаут на получение данных и обработать ошибку по его наступлению (верно)

25. REST это
* Протокол удаленного вызова процедур, работающий поверх UDP
* Протокол удаленного вызова процедур, работающий поверх TCP
* Архитектурный подход, позволяющий строить API на основе протокола HTTP (верно)

26. Что дает кеширование HTTP соединений ?
* Существенно уменьшается объем сетевого трафика
* Существенно уменьшается нагрузка на Application сервер, т.к. не нужно каждый раз запускать новые процессы
* Сокращается задержка (latency) запросов, т.к. не нужно осуществлять TCP/TLS handshake (верно)

27. Docker это
* Виртуальная машина, позволяющая одну операционную систему внутри другой
* Сиcтема контейнеризации, позволяющая запускать хорошо изолированные процессы в рамках одной ОС (верно)
* Система управления конфигурацией для деплоя сложных Web приложений

28. При развертывании Web приложения на Go вам необходимо установить на сервер
* Копилятор Go и исходный код вашего приложения
* Виртуальную машину Go (runtime) и скомпилированный код вашего приложения
* Скомпилированный код вашего приложения, больше ничего не нужно (верно)

29. Что такое Service Discovery ?
* Механизм обнаружения endpoint-ов (ip:port) ваших сервисов при развертывании в облаке (верно)
* Механизм публикаци спецификации API ваших приложений
* Публикация вашего сервиса в каком-либо магазине, например AppStore

30. Логотип языка Go это
* Хомяк
* Бурундук
* Суслик (верно)
* Морская свинка