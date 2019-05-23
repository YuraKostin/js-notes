# JS for beginners

[Коротко и неполно о том, что происходит внутри](#about-invisible-jobs)


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

Как ни странно, чем на первый взгляд проще, компактнее и понятнее команда, тем
сложные процессы протекают "под капотом", то есть незримо для программиста.

Что же это за процессы? Дело в том, что нельзя сказать компьютеру:

\- Эй, покажи на экране сообщение "Hello, World"

Нельзя потому, что компьютер не знает, что это за команда такая. Чтобы компьютер
понял эту команду, он должен получить команду на языке, который он понимает.
Таким языком является 
[машинный код](https://ru.wikipedia.org/wiki/%D0%9C%D0%B0%D1%88%D0%B8%D0%BD%D0%BD%D1%8B%D0%B9_%D0%BA%D0%BE%D0%B4),
а это, как известно, нули и единицы.

Как же команда `Показать сообщение "Hello, World"` превращается в нули и единицы?
Для этого существуют программы, они получают наш, понятный нам - людям - код,
и интерпретируют его в код, понятный для компьютера. Такие программы называются
интерпретаторами и компиляторами. Они занимаются большим объёмом работы, имеют
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

