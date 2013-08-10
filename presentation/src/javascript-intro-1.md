#Javascript-intro#



##Инструментарий##
- текстовый редактор (SublimeText, Notepad++)
- браузер


##Консоль##

* Firefox + firebug (однострочна по умолчанию)
* Chrome (webinspector)


##Консоль##

Для того, чтобы попробовать код
<pre><code>function alertHello () {
    alert('hello!');
}

alertHello();</code></pre>



##Стадии выполнения программы##
* Чтение
* Выполнение


##Ошбки##
* Этапа чтения (SyntaxError)
* Этапа выполнения — недопустимые действия программы


##Синтаксические ошибки##
Сообщения об ошибке могут быть абсолютно бесполезными
<pre><code>function alertHello ( {
    alert('hello!');
}

alertHello();</code></pre>


##Ошибки выполнения##
<pre><code>function alertHello () {
    alent('hello!');
}

alertHello();</code></pre>



##Литерал##
Строка в теле программы, описываюшая данные
<pre><code>function alertHello () {
    alert('hello!'); // строчный литерал
}

alertHello();</code></pre>


##Литерал##
Понятие необходимо, чтобы в будущем разделить данные, описанные литералами, и созданные конструкторами.



##Типы данных##
* Примитивы
* Объекты


##Отличие примитива от объекта##
- в присвоении
- в сравнении
<small>пока просто запомним</small>



##Примитивы##

* Числа
* Строки
* Булевы примитивы
* Специальные примитивы



##Числа##
Нет разделения на целые, числа с плавающей точкой.


##Числовые литералы##
	
	// js
	42;	// целое
	0.33;  // с плавающей точкой
	.99;   // с опущенной целой частью



##Строки##
Нет понятия «символ»  
Форма кавычек роли не играет (одинарные или двойные)  
Если строка заключена в одинарные кавычки, внутри можно использовать двойные. И наоборот


##Строковые литералы##

	'';	   // пустая строка
	"Строка"; // идиентичная строке ниже 
	'Строка'; // идиентичная строке выше
	"That's my code";
	'"White" night';
	'Г';	  // строка с одним символом



##Булевы##
Представление логического «правда» и «ложь»

	true;  // правда
	false; // ложь


##Булевы##
- работа с логическими операторами
- битовые оперторы


##Булевы эквиваленты данных##


##false##
false, 0, '', undefined, null, NaN


##true##
Все остальные



##Специальные##


##undefined##
Неопределенность  
- значение объявленной переменной
- возвращаемое значение функции, если не указан явно return  
- аккуратно со сравнением


##null##
Пустая ссылка



##Выражения##

	42   // → вычисляется в число 42
	"42" // → вычисляется в строку "42"
	'42' // → вычисляется в строку "42"
	0.3 + 77 // → вычисляется в число 77.3


##Выражения##
Литералы - выражения, вычисляющиеся в сами себя



##Переменные##
Именованные контейнеры для хранения и доступа к данным


##Объявление##

	var person;


##Имена переменных##
Не используйте зарезервированные имена  s
Использовать имена, намекающие, что в переменной хранится

	var div, myVar, num; // плохо
	var headerNavigation, personName, maxItems; // хорошо

Исключение - переменные циклов (i, j, k)


##Обращение к переменной##
Вычисляется в значение, хранимое в переменной


##Во что вычисляется выражение##

	var person; // → undefined
	person;	 // → undefined. Обращение к переменной
	person = 'Vasya';
	person; // → 'Vasya'
	person + ' рулит'; // → 'Vasya рулит'



##Операторы##
Операнд то, над чем проводится операция



##Операция присваивания##
Порядок работы оператора

1. вычисление выражения справа
2. присвоение результата в левую часть


##Пример выражения##
	var person;
	person = "Bob";
	person; // 'Bob'


##Пример выражения##
	var person = "Bob";
	person; // 'Bob'



##Логические операторы##
* Не
* Или
* И


##Не##
Вычисляется в булево  
Возвращает значение противоположное булевому эквиваленту операнда


##Не##

	// js
	!false;		 // true
	!"some string"; // false


##Приведение к булевому значению##

	// js
	!!true;	  // true
	!!9;		 // true
	!!undefined; // false
	!!' ';	   // true


##Или и И##
Вычисляется в один из операндов


##Или##

	// js
	0 || 10;			// 10
	"Sasha" || "Masha"; // "Sasha"
	true || false;	  // true


##И##

	// js
	10 && 20;		   // 20
	false && "konfeta"; // false
	1 && undefined;	 // undefined


##Ленивость##
Вычислится ровно столько выражений, сколько надо для получения результата.


##Комбинация логических операторов##

	// js
	10 && !false || 10;			   // true
	!(name || true) && undefined;	 // false
	42 || "Alter question" || 100500; // 42


##Применение при присвоении##

Обычный случай — значение переменных по умолчанию

	// js
	personName = name || "Noname";



##Операторы сравнения##
* Больше-меньше
* Равенство


##Больше-меньше##
Вычисляется в булево значение


##Пример выражения##

	var num = 10;
	num < 90;	// true


##Сравнение строк##

	'a' > 'e'; // false
	'б' < 'ю'; // true


##Крайне аккуратнее##
Со строками

	'а' > 'ё'; // true
	'я' > 'ё'; // true



##Оператор +##


##С числами##
Сложение


##Сложение##

	// js
	10 + 20;		   // 30
	1 + 1 + 2 + 3 + 5; // 12


##Внимательно с дробными##

	// js
	0.1 + 0.1 === 0.2; // true
	0.1 + 0.2 === 0.3; // false


##Внимательно с дробными##

	// js
	0.1 + 0.2; 0.30000000000000004


##Со строками##
Конкатенация	


##Конкатенация##
	
	// js
	"Mama " + "mila " + "ramu"; // "Mama mila ramu"


##Число + строка##
	
	// js
	10 + '10';	  // '1010'
	10 + 10 + '10'; // '2010'


##С вниманием к типам##
	
	var peopleInBoat;
	peopleInBoat = '3';

	peopleInBoat + " в лодке, не считая собаки";


##С вниманием к типам##
	
	var peopleInBoat;
	peopleInBoat = '3';

	(peopleInBoat + 1) + " в лодке, считая собаку";


##Побольше однозначности##
* Приводить получаемые значения к ожидаемому типу
* Хранить данные в ожидаемом типе


##Короткая запись##

	var name = "Bond";
	name = name + ", James Bond";
	name
	
	// equivalent to above
	var name = "Bond";
	name += ", James Bond";
	name


##Короткая запись##
Фокус не пройдет с литералом
	
	2 += 20; // Reference error


##Быстрый и неоднозначный##
Способ преобразовать строку в число
	
	// js
	+"42"; // 42



##Равенство##
* Строгое  
  ===, !==
* Нестрогое  
  ==, !=


##Строгое##

	"a" === "a"; // true
	1 === "1";   // false


##Нестрогое##

	"a" == "a"; // true
	1 == "1";   // true


##Нестрогое##
Никогда не используйте нестрогое  
<small>без явной на то необходимости</small>

	['1'] == true; // true
	'1' == 1;	  // true