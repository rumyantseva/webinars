# Документация Go кода

Есть мнение, что хороший код должен быть самодокументированным, т.е.
не требовать документации вообще. Названия функций и переменных должны быть точно
и недвусмысленно обяъснять что делает функция и что хранится в переменной.
В целом это хорошая практика в больших проектах, но в публичных библиотеках
все же стоит явно описать каждую важную функцию. Это намного упростит использование
вашей библиотеки, особенно в первый раз.

Где нужно размещать такое описание ? README.txt ? markdown ? Пафосный web сайт ?
В Go как и во многих других языках принято размещать документацию прямо в коде библиотеки
или приложения. Это упрощает ее написание и уменьшает шансы того, что документации
разойдется с кодом приложения. Далее из такой документации можно автоматически
сгенерировать простой текстовый файл с помощью вызова `godoc github.com/yourname/yourlib`
или даже HTML страничку, если использовать флаг `godoc --html`.  Кстати, утилита `godoc`
может работать как HTTP сервер и показывать документацию в виде Web-сайта. Документация
[стандартной библиотеки языка Go](https://golang.org/pkg/) именно так и генерируется.

Формат документации прост: для того что бы добавить документацию к фукнции, типу,
константе или даже пакету нужно написать простой комментарий перед соответствующим объявлением.
```
// ModSum adds a to b modulo m.
// Values of a and b may be greater than m
func ModSum(a, b, m int) int {
    return (a + b) % m
}
```
Важное соглашение: комментарий должен быть законченной фразой и должен начинаться с имени функции
или переменной к которой он относится. Документация которая относится к пакету целиком часто 
помещается в отдельный файл, например doc.go в этом пакете. 

При построении HTML или текстовой документации go doc следует простым правилам:
* Все параграфы в документации должны быть разделены пустой строкой
* Все URL найденные в тексте автоматически превращаются в гиперссылки, никакой специально разметки не нужно
* Если вы хотите отобразить текст преформатированным, сделайте отступ в начале каждой строки этого блока

```
/*
Go documentation example

Theese lines will be displayed as paragraph
as the don't have blank lines between them.
Below you can see preformated snippet:

  s := ModSum(a, b, 13)
  s2 := (a + b) % 13
  assert.Equal(s, s2, "should be the same")

*/
```