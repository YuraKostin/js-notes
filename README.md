# JS for beginners

* [Коротко и неполно о том, что происходит внутри](#about-invisible-jobs)

* [Окружение](#environment)

* [Типы данных](#simple-data-types)
    * [Числа](#numbers)
    * [Строки](#strings)
    * [Булев тип](#boolean)
    * ["Магия" JavaScript и NaN](#magic-and-nan)
    * [null - ничто](#null)
    * [undefined - неустановленное значение](#undefined)

## <a id="about-invisible-jobs">Коротко и неполно о том, что происходит внутри</a>

Языки программирования бывают разными, все они отдают команды процессору
компьютера, однако делают это по-разному.

Если проводить аналогию с реальным миром, то можно представить разные процессы:
приготовление блюда, строительство дома и прочие. А также, нужно представить,
что разрабатывая программы, мы выступаем в качестве руководителя. Мы даём языку 
программирования задачи разного уровня сложности:
 
* приготовить салат
* нарезать овощи, залить их маслом и перемешать
* открыть холодильник, достать овощи и положить их на стол, 
закрыть холодильник, положить овощи в раковину, помыть овощи,
достать доску, достать нож, положить овощи на доску, взять нож, нарезать
овощи, достать миску, сложить нарезанные овощи в миску, достать масло,
открутить крышку у масла, налить масло в миску с овощами, закрыть масло...
и так далее.
    
Что же мы видим? Мы видим, что команды могут быть очень разными, они могут быть
короткими и ёмкими, могут быть очень подробными и многословными.

Как ни странно, чем проще, компактнее и понятнее команда, тем более
сложные процессы протекают "под капотом", то есть незримо для программиста.

Что же это за процессы? Дело в том, что нельзя сказать компьютеру:

\- Эй, покажи на экране сообщение "Hello, World"

Нельзя потому, что компьютер не знает, что это за команда такая. Чтобы компьютер
понял эту команду, он должен получить команду на языке, который он понимает.
Таким языком является 
[машинный код](https://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D1%88%D0%B8%D0%BD%D0%BD%D1%8B%D0%B9_%D0%BA%D0%BE%D0%B4),
а иными словами - нули и единицы.

Как же команда `Показать сообщение "Hello, World"` превращается в нули и единицы?
Для этого существуют программы, они получают наш, понятный нам - людям - код,
и интерпретируют его в код, понятный для компьютера. Такие программы называются
[интерпретаторами](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B0%D1%82%D0%BE%D1%80)
и
[компиляторами](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%BC%D0%BF%D0%B8%D0%BB%D1%8F%D1%82%D0%BE%D1%80). 
Они занимаются большим объёмом работы, имеют
множество нюансов и этапов; и для каждого языка программирования эти программы
различны. 
Однако, в конце концов, весь написанный программистом код, превращается в машинный
код, пусть мы и не всегда об этом знаем и видим.

Языки 
[компилируемые](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%BC%D0%BF%D0%B8%D0%BB%D0%B8%D1%80%D1%83%D0%B5%D0%BC%D1%8B%D0%B9_%D1%8F%D0%B7%D1%8B%D0%BA_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F) и 
[интерпретируемые](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B8%D1%80%D1%83%D0%B5%D0%BC%D1%8B%D0%B9_%D1%8F%D0%B7%D1%8B%D0%BA_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F) языки, и ещё 
[здесь](https://tproger.ru/translations/programming-concepts-compilation-vs-interpretation/)
и [здесь](http://itmentor.by/articles/kompiliruemye-i-interpretiruemye-yazyki-programmirovaniya)

Что такое [компилятор](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%BC%D0%BF%D0%B8%D0%BB%D1%8F%D1%82%D0%BE%D1%80) и
[интерпретатор](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%82%D0%B5%D1%80%D0%BF%D1%80%D0%B5%D1%82%D0%B0%D1%82%D0%BE%D1%80).

## <a id="environment">Окружение</a>

### Где писать код
Чтобы начать писать код нужно понимать где его писать, как запускать, чтобы посмотреть
результат своих трудов.

1. [Самый быстрый способ](https://github.com/YuraKostin/mentor-room/tree/master/articles/introduction/how-to-begin-js-in-console)
 попробовать запустить кусочек кода в браузере 
 
2. Сервисы: 
     - [https://codepen.io/](https://codepen.io/),
     - [https://jsfiddle.net/](https://jsfiddle.net/)
     - etc
     
3. Создать html файл и написать js код в нём, или в отдельном файле и 
подключить его в html

    Про создание html файла можно почитать [здесь](https://github.com/YuraKostin/mentor-room/tree/master/articles/introduction/how-to-begin-with-html),
    а также на ресурсах типа [https://htmlacademy.ru/](https://htmlacademy.ru/).
    
    Для редактирования файлов с кодом существуют специальные программы.
    Их список довольно обширен, но здесь я приведу только часть:
    - WebStorm (платный)
    - VSCode
    - SublimeText (условно бесплатный)
    - Brackets
    - Atom
    
    Не буду рассказывать, в чём между ними отличия, также рекомендовать какой-то
    определённый редактор, так как это крайне субъективная оценка; нет лучшего
    способа найти свой редактор, чем перепробовать какое-то их количество и
    остановиться на том, в котором работать максимально приятно и удобно.
    
    Замечу только одно отличие между приведёнными в списке инструментами.
    Среди них есть IDE (интегрированная среда разработки), и просто редакторы.
    В IDE обычно уже предустановлено большое количество полезных функций,
    однако за это и другие удобства приходится платить - IDE более "прожорливы"
    к ресурсам компьютера, чем простые редакторы.
    В редакторы можно добавить необходимую функциональность, устанавливая
    плагины.
    
    Чтобы вывести на экран сообщение "Hello, World", необходимо добавить 
    в html файл из инструкции выше следующий код:
    ```html
       <script>
           alert('Hello, World');
       </script>
    ```
    
    **Важно**: код должен быть помещён между открывающим и закрывающим тегом
    `<body>` 

### Домашка
Б**о**льшую часть домашнего задания мы будем делать в git-е.
Прочитать про git можно [здесь](https://git-scm.com/book/ru/v2).

Для выполнения первой домашки будет сделан небольшой гайд, но чтобы не
отставать, рекомендуется узнать, что такое гит основные команды по работе с
ним.
Нам точно понадобятся:
- git pull
- git add
- git commit
- git push
- git merge


## <a id="simple-data-types">Простые типы данных</a>

### <a id="numbers">Числа</a>

javascript позволяет выполнять все основные операции над числами:
складывать, вычитать, умножать, делить, возводить в степень, и так далее.

Проверить это очень просто: открыть консоль в браузере и ввести соответствующую команду:
```javascript
1 + 1 // 2

10 - 5 // 5

10 * 5 // 50

4 / 2 // 2
```

#### Комментарии

Такая пара символов `//` указывает, что далее за ними следует комментарий.
Комментарии в некоторых случаях бывают удобны, мы рассмотрим их
применение позже.

```javascript
// Это однострочный комментарий. Здесь конструкция alert('Hello, World') не выполнится.
```

Также существует другая запись для создания комментариев:

```javascript
/*
    Это многострочный комментарий.
    Любой код, который будет здесь введён, никогда не выполнится 
*/
```

При выполнении различных операций над числами в javascript есть вероятность
столкнуться с очень странными результатами вычислений.

```javascript
0.1 + 0.2 // 0.30000000000000004
```

Вот так номер. Такой результат обусловлен представлением чисел с плавающей
точкой в процессорах, а это значит, что эта проблема характерна не только
для javascript.

Детальнее об этом можно почитать [здесь](https://pythoner.name/documentation/tutorial/floatingpoint)


### <a id="strings">Строки</a>

Программировать без такого типа данных как строки, было бы очень неудобно.
В первую очередь нужно помнить, что у символов(даже у тех, которые вы сейчас читаете),
есть [числовое представление](https://ru.wikipedia.org/wiki/%D0%A1%D1%82%D1%80%D0%BE%D0%BA%D0%BE%D0%B2%D1%8B%D0%B9_%D1%82%D0%B8%D0%BF).

Символу "a" из английского алфавита соответствует код 97 из таблицы 
[ascii](http://www.asciitable.com/). Подробнее об [ascii](https://ru.wikipedia.org/wiki/ASCII)

Это легко проверить, используя такой вызов
```javascript
'a'.charCodeAt(0) // 97
```

Вот вы и увидели, как описать строку в javascript: текст, обрамлённый кавычками.
Пока что не обращайте внимание на всё, что идёт, после закрывающей кавычки, это
мы рассмотрим позже.

Можно использовать три вида кавычек:
* 'одинарные'
* "двойные"
* `обратные`

Обратные кавычки используются для особых ситуаций, о которых мы поговорим позже.
Одинарные же использовать кавычки, или двойные - не велика разница, но лучше
придерживаться единого стиля. Я предпочитаю одинарные, однако бывают случаи,
когда без кавычек другого вида не обойтись.

Представим, что мы используем двойные кавычки, и нам нужно обрамить 
двойными кавычками какое-нибудь слово:

```javascript
"И Люсьен сказала "Нет""
```

Такой код выбросит ошибку (пока что не спрашивайте, что это значит) потому что
интерпретатор будет считать, что мы закончили одну строку, а дальше указали
неизвестный интерпретатору идентификатор `Нет`. В javascript нет такого
[зарезервированного слова](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Lexical_grammar).
В таком случае вариантов у нас есть несколько:

1. Использовать одинарные кавычки, а уже внутри них вкладывать двойные 
`'И Люсьен сказала "Нет"'`
2. Использовать [экранирующий символ](https://ru.wikipedia.org/wiki/%D0%AD%D0%BA%D1%80%D0%B0%D0%BD%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5_%D1%81%D0%B8%D0%BC%D0%B2%D0%BE%D0%BB%D0%BE%D0%B2)
 обратного слеша "\\".
`"И Люсьен сказала \"Нет\""` здесь мы просим использовать кавычки не как
способ указать на конец/начало строки, а как простой текст.


Со строками можно делать довольно много интересного, но пока что мы
научимся их "складывать".

```javascript
'Hello' + ', ' + 'World' // превратится в строку 'Hello, World'
```
 
Используя оператор `+` для строк, мы [конкатенируем](https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D0%BD%D0%BA%D0%B0%D1%82%D0%B5%D0%BD%D0%B0%D1%86%D0%B8%D1%8F#%D0%92_%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%82%D0%B8%D0%BA%D0%B5) 
их, то есть [соединяем](https://dic.academic.ru/dic.nsf/fin_enc/24101).

### <a id="boolean">`boolean`</a>

На русском языке это значение звучит как "булево".

Жил в XIX веке умный дядька [Джордж Буль](https://ru.wikipedia.org/wiki/%D0%91%D1%83%D0%BB%D1%8C,_%D0%94%D0%B6%D0%BE%D1%80%D0%B4%D0%B6).
Он придумал такую штуку как [булева алгебра](https://ru.wikipedia.org/wiki/%D0%91%D1%83%D0%BB%D0%B5%D0%B2%D0%B0_%D0%B0%D0%BB%D0%B3%D0%B5%D0%B1%D1%80%D0%B0).

`boolean` может принимать только одно из двух значений 
`true`(истина) или `false`(ложь).

Это тот тип данных, который помогает нам в программах принимать решения.
В нашей обычной жизни мы используем булеву алгебру постоянно.

Утром, выглядывая в окно, собираясь на улицу, 
у меня в голове есть следующие установки:

* если за окном идёт дождь - взять зонтик
* если за окном светит яркое солнце - взять солнечные очки

В данном случае утверждение "дождь идёт" это булево значение - 
дождь либо идёт(`true`), либо нет(`false`).

Кто-то может думать иначе "если дождя нет - 
зонт брать не буду, если идёт дождь - возьму зонт".
Тут `true`/`false` будут вставать в другом, инверсированном порядке:
выражение "дождя нет" - принимает значение `true`, если за нет дождя,
и значение `false`, если дождь идёт.

### <a id="magic-and-nan">Чудеса JavaScript и специальный тип данных `NaN`</a>

Мир программирования можно и нужно исследовать, а значит эксперименты
должны войти в привычку.

Что будет, если сложить число и строку? Давайте проверим.
Предупреждаю, здесь начинается магия, за которую JS не очень любят.

```javascript
20 + '20' // '2020'
```

Так, вместо выброса ошибки ввиду сложения разных типов данных, произошло
преобразование числа к строке и дальнейшая конкатенация строк.

Пойдём дальше.

```javascript
20 - '20' // 0
```

И ноль это число, а не строка.

Что на счёт умножения и деления?

```javascript
20 * '20' // 400
20 / '20' // 1
```

`400` и `1` здесь тоже числа.

Хм, ну ладно. Получается, что при подобных операциях все операторы, кроме
оператора сложения возвращают числа.
Здесь просматривается определённое поведение вида:

```javascript
если оператор это "+"
    тогда: сложить операнды, преобразовав каждый из них к строке
    иначе: выполнить математическую операцию (соответственно для операторов "-", "*" и "/")
```

Такие рассуждения недалеки от истины.
Существует [EcmaScript спецификация](https://www.ecma-international.org/ecma-262/10.0/index.html), 
описывающая как должна быть реализована так или иная функция, тот или иной тип данных, и прочие нюансы в языках.
Процедуры, выполняемые оператором "+", описаны в этой секции
[спецификации](https://www.ecma-international.org/ecma-262/10.0/index.html#sec-addition-operator-plus).

Ух, как много всего непонятного и нового.

Итак:
1. **EcmaScript**.
    EcmaScript это "правильное" название JavaScript.
    Об истории появления языка можно прочитать в [этом](https://habr.com/ru/company/livetyping/blog/324196/)
    цикле статей, а также найти на просторах интернета.
2. Что такое **спецификация**?
    Аналогия.
    Предположим, что есть такая спецификация:
    * _Дверь, это объект из какого-либо материала, как правило прямоугольной формы;_ 
    * _Дверь должна иметь ручку для открывания и закрывания;_
    * _и т д..._
    
    Прочитав такую спецификацию, можно сделать сколь угодно разные двери:
    * деревянную с круглой крутящейся ручкой
    * металлическую с г-образной ручкой, которую нужно нажимать сверху
    * дверь, которая могла бы быть описана в спецификации, как дверь без ручки - двери в ковбойский салун
    * дверь, характерная для нор хоббитов
    * и т д
    
    JavaScript в первую очередь выполняется в браузере. Для того, чтобы
    код, который мы пишем и запускаем в браузере, выполнялся, существуют
    движки, которые реализуют спецификацию.
    Одним из самых популярных движков является [v8](https://github.com/v8/v8) - 
    движок, компании Google.

    Сколько людей, столько и мнений: движков, реализующих javascript много
    и в этом заключается причина того, что поведение одного и того же кода
    в разных браузерах может отличаться.
    
    Существует очень [большая таблица](http://kangax.github.io/compat-table/es6/).
    Информация в ней позволит узнать, поддерживается та или иная возможность
    в том или ином браузере.

Вернёмся в реальность.

Мы не довели наш эксперимент до абсурда.

Что, если попытаться сложить строку и число?

```javascript
10 + 'abc' // '10abc'
```

Ладно, это, читай та же конкатенация строк.

Теперь умножим.

```javascript
10 * 'abc' // NaN
```

Вот так раз! В результате такого странного умножения мы тоже не 
получили никакой ошибки, но получили `NaN`.

`NaN` это числовой тип данных. Разшифровывается это значение как "Not a number", 
то есть "не число". Это значит, что в ходе вычислений невозможно было привести
аргументы к значению, которое можно считать валидным числом.

Подробнее про [NaN](https://ru.wikipedia.org/wiki/NaN).

### <a id="null">`null`</a>

`null` это значение, которого нет, иными словами - указатель на то, что
значения не существует.
Если обратиться к спеке(читай спецификакции), то можно найти
[следующее](https://www.ecma-international.org/ecma-262/10.0/index.html#sec-null-value):

> **4.3.12 null value**
>
> primitive value that represents the intentional absence of any object value

Примитивное значение, которое представляет отсутствие какого-либо значения у объекта.

Что есть объект мы узнаем немного позже, но пока что запомните `null` это
указание на то, что значения нет.

В сети гуляет любопытная картинка на эту тему:

![0-and-null](./images/0-null-paper.jpg)

* слева есть рулон и на нём нет бумаги, это `0`; при этом мы можем
"обратитсья" к рулону - потрогать его - и понять, что да, бумага 
кончилась

* справа рулона нет, это `null`; в этом случае "обратиться" к рулону
бумаги нет никакой возможности - рулона не существует;


### <a id="null">`undefined`</a>

`undefined` это тогда, когда значение не было установлено.

Вспомните математику. У нас были задачки с одной неизвестной.
Мы говорили "пусть `x` будет означать количество чего-либо".
В случае с `undefined` мы как бы говорим "пусть будет `x`". И всё.
Мы ещё не придумали, что этот `x` значит, но уже объявили всем, что он
есть.

#### Итог: простые типы данных

Мы рассмотрели:
* строки - `string`
* числа - `number`
* булев тип - `boolean`
* не число - NaN - `number`
* ничто - `null`
* неустановленное значение - `undefined`

Если что-то осталось непонятным - не страшно. Мы активно будем
использовать эти типы данных в наших программах, и вскоре узнаем
некоторые интересные нюансы работы с ними.
