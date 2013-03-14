#Javascript-intro#



##Javascript – это##
Встреваемый интерпретируемый объектно-ориентированный (с прототипным уклоном) язык с динамической типизацией


##Встраеваемый##
- Оперирует высокоуровневыми сущностями
- Бедная стандартная библиотека


##Интерпретируемый##
- Код не требует компиляции <small>(предварительной обработки перед запуском)</small>


##Объектно-ориентированный##
- Оперирует объектами
- Прототипная модель наследования


##Динамически типизированный##
- Переменные может хранить любой тип данных



##Разберемся в названиях##


##Реализации##
JavaScript™, jScript, liveScript


##Стандарт##
ECMAScript


##Ничего общего с Java##



##Как его потрогать##


##Консоль##

* Firefox + firebug
* Chrome (webinspector)



##Работа интерпретатора##


##Стадии выполнения программы##
* Чтение
* Выполнение


##Ошибки##
* Чтение — синтаксические ошибки
* Выполнение — ошибки выполнения



##Литерал##
Описанные специальным образом данные



##Типы данных##
* Примитивы
* Объекты


##Отличие примитива от объекта##
Способ хранения и сравнения <small>пока просто запомним</small>



##Примитивы##

* Числа
* Строки
* Логические
* Специальные



##Числа##
Нет разделения на целые, числа с плавающей точкой.


##Числовые литералы##
	
	// js
	42;    // целое
	0.33;  // с плавающей точкой
	.99;   // с опущенной целой частью
<small>есть и другие формы и значения</small>



##Строки##
Нет понятия «символ»  
Форма кавычек роли не играет (одинарные или двойные)


##Строковые литералы##

	'';       // пустая строка
	"Строка"; // идиентичная строке ниже 
	'Строка'; // идиентичная строке выше
	'Г';      // строка с одним символом



##Логические##
Представление логического «правда» и «ложь»

	true;  // правда
	false; // ложь



##Специальные##


##undefined##
Неопределенность


##null##
Пустая ссылка



##Приведение типов##
Преобразование значение одного типа в другой


##Приведение типов##
* Явное
* Неявное (бич и причина многих багов)



##Javascript выражение##
Любой валидный js код  
Вычисляется во что-то (!)


##Литералы - это валидные javascript выражения##

	42   // → вычисляется в число 42
	"42" // → вычисляется в строку "42"
	'42' // → вычисляется в строку "42"



##Переменные##
Именованные контейнеры для хранения и доступа к данным


##Объявление##

	var person;


##Имена переменных##
Не используйте зарезервированные имена


##Обращение к переменной##
Вычисляется в значение, хранимое в переменной


##Во что вычисляется выражение##

	var person; // → undefined
	person;     // → undefined. Обращение к переменной



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



##Операторы сравнения##
* Больше-маньше
* Равенство


##Больше-меньше##
Вычисляется в булево значение


##Пример выражения##

	var num = 10;
	num < 90;    // true


##Сравнение строк##

	'a' > 'e'; // false
	'б' < 'ю'; // true


##Крайне аккуратнее##
Со строками

	'а' > 'ё'; // true
    'я' > 'ё'; // true



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

	['1'] == true; // true
	'1' == 1;      // true


##Сравнение по типам данных##
* Примитивы — по значению
* Объекты по ссылке
	