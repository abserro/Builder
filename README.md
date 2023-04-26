# Порождающие паттерны проектирования
Абстрагируют процесс инстанцирования 
объектов. Они позволяют сделать код независимым от способа создания, композиции и 
представления используемых в его работе объектов.
## Builder
Отделяет конструирование сложного объекта от его представления, так что в результате 
одного и того же процесса конструирования могут получаться разные представления.  
Класс каждого конвертора принимает механизм создания и сборки сложного объекта и 
скрывает его за абстрактным интерфейсом. Конвертор отделен от загрузчика, который 
отвечает за синтаксический разбор RTF-документа.  
В паттерне строитель абстрагированы все эти отношения. В нем любой класс конвертора 
называется _строителем_, а загрузчик – _распорядителем_.

Структура:

![image](https://user-images.githubusercontent.com/107203406/234675621-5958636b-a787-4031-a3b0-68f33d1c9535.png)

### Задание
Обеспечить контроль загрузки и готовности к отправлению автобусов и такси.  
Водитель такси и автобуса имеют права разной категории. Без водителя машина не 
поедет. Два водителя в одну машину сесть не могут. Без пассажиров машины не 
поедут. Есть лимит загрузки машин. Для автобуса 30 чел. Для такси - 4 чел.
Есть разница между пассажирами автобуса и такси.  
Для автобуса: три категории пассажиров - взрослый, льготный, ребенок - разная 
стоимость билета.  
Для такси: взрослый и ребенок. Необходимо детское кресло.

### Решение
Диаграмма классов:

![image](https://user-images.githubusercontent.com/107203406/234682219-88f9ee6f-ca11-4e26-a765-9876a93c3fc1.png)

