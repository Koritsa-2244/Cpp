Лабоpатоpная pабота №1
Линейные списки

1.cpp - файл с предаставлением очереди и стека в виде массива
Sourse1.cpp - файл с представлением очереди и стека в виде динамического списка

Выполнить задания, используя для пpедставления очеpедей и стеков:
а) массивы; б) динамические списки.
Требования к программам:
1. Количество элементов исходных линейных списков заранее не определено
и задается случайным образом. При дальнейшей обработке считается, что
количество элементов списка не известно, т.е. обработка производится, пока
не достигнут конец списка.
2. Программа должна сформировать исходные линейные списки, вывести их содержимое
на экран (при этом данные из списков не должны быть потеряны), произвести
обработку и вывести содержимое итогового списка на экран.

13 вариант

13. Даны два стека целых чисел. Сфоpмиpовать очередь из элементов пеpвого стека, кpатных максимуму втоpого.

а) массивы;

Алгоритм:

Создается структура Queue1, в ней содержатся указатель на нулевой элемент массива элементов очереди, четыре элемента типа int – указатели на начало и конец очереди, количество элементов очереди.
Функция add добавляет элемент в очередь, обновляя указатель на конец очереди, добавляя элемент в массив и увеличивая количество элементов в очереди.
Функция ShowQueue если очередь пуста выводит соответствующее сообщение. Если очередь не пуста создается временный указатель на первый элемент очереди и с его помощью через next проходим по всем элементам очереди, на каждом элементе выводится значение поля data.
Удаление элементов из очереди происходит путем сдвига указателя начала очереди и уменьшения количества элементов функцией del.
Создается структура Stack1, в ней содержатся указатель типа int, массив, который будет использоваться для хранения данных в стеке, переменная int top, которая указывает на вершину (последний добавленный элемент) стека.
Функция InitStack инициализирует стек, выделяя место для массива и устанавливая вершину стека
Функция push добавляет элемент в стек, увеличивая вершину стека и помещая значение в массив.
Функция pop удаляет элемент из стека, возвращая значение и уменьшая вершину стека.
NullStack Эта функция "стирает" стек, устанавливая вершину стека (переменную top) в значение -1. Это действие позволяет "очистить" стек, установив его в начальное состояние без каких-либо элементов.
Функция empty проверяет, пуст ли стек, возвращая значение true в случае, если вершина стека (top) имеет значение -1, что означает, что стек пуст. Если стек не пуст, функция возвращает false.
В функции main случайным образом генерируются значения для размера и элементов стеков. Добавление элементов происходит путем вызова push для стеков и add для очереди. Далее идет обращение поочередно ко всем элементам стека, значение элементов выводятся и ищется максимальный. После выводится максимальный элемент. Соответственно выводятся элементы первого стека ищутся и считаются кратные максимуму второго. Инициализируем очередь размером по количеству кратных элементов. Еще раз проходим по первому стеку на этот раз записываем кратные в очередь. Выводим очередь поочередно обращаясь к каждому элементу.
б) динамические списки.

Алгоритм: 
InitStack эта функция инициализирует стек, устанавливая указатель top в NULL.
Функция push добавляет элемент в стек. Создается новый узел, в который помещается значение, затем этот узел становится вершиной (top) стека.
Функция pop извлекает элемент из стека. Значение из вершины (top) копируется в переменную d, затем освобождается память, выделенная для вершины, и вершина перемещается на следующий элемент. Значение d возвращается как результат.
Функция empty проверяет пуст ли стек, возвращая true если top равно NULL, иначе возвращается false.
Функция nullStack "стирает" стек, удаляя все его элементы. Она продолжает удалять элементы, пока стек не будет пустым, используя функцию empty для проверки.
 
Класс Queue. Сначала идет описания структуры Node, которая представляет узел в связанном списке. Каждый узел содержит два поля: data: Поле, которое содержит данные узла, next: Указатель на следующий узел в связанном списке. После идут два указателя на начало и конец очереди head и tail соответственно.
Метод empty проверяет, пуста ли очередь, возвращая true, если head равен NULL.
Метод add добавляет элемент в очередь. Если очередь пуста, создается новый узел и он становится её началом и концом. В противном случае новый узел добавляется в конец очереди.
Метод ShowQueue если очередь не пуста создается временный указатель tmp с помощью которого проходим по всем элементам очереди и выводим значение поля data.
Метод del удаляет элемент из начала очереди и возвращает его значение. Если очередь пуста, выводится сообщение "Queue is empty" и возвращается 0.

Далее идет функция main, где программа создает два стека (st1 и st2) и один объект класса очереди que. Стеки заполняются случайными числами. Далее идет обращение поочередно ко всем элементам стека, значение элементов выводятся и ищется максимальный. После выводится максимальный элемент. Соответственно выводятся элементы первого стека ищутся и считаются кратные максимуму второго. Еще раз проходим по первому стеку на этот раз записываем кратные в очередь. Выводим очередь поочередно обращаясь к каждому элементу.
