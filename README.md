# VladimirProjectJava
Проект написан на языке программирования Java с иcпользованием Maven для внедрения зависимостей.
Подключение к БД выполняется с помощью интерфейса Connection.
Запросы же к БД выполняются с помощью интерфеса Statement.
После запуска проекта пользователь должен ввести абсолютный путь к csv-файлу c данными и указать были ли эти данные заранее подгружены в нашу SQLite.

После выполнения вышеописанных действий в дело вступает сочетание классов Game и GameController.

Класс Game выступает как вспомогательный для хранения данных из нашего датасета.

-

Все поля данного класса совпадают со столбцами нашему исходного файла, а так же для каждого из полей прописаны геттеры и сеттеры и переопределен метод toString() для корректного отображения данных.

Класс GameController необходим для манипулирования этими данными.
Все методы данного класса направлены на взаимодействие с нашей базой данных.
Метод firstTask() занимается построением графика для первого задания, предварительно сделав запрос на необходимую выборку данных из нашей БД.

Метод secondTask() так же выполняет запрос к нашей БД с использование вышеописанных интерфесов. Полученная выборка формаируется на основе выбранного из задания года.

Далее просиходит поиск максимального значения продаж и выводится объект класса Game с полями, сформированными на основе полученной выборки данных.

Метод thirdTask() ищет строку с макимальными продажами в Японии в оперделенном диапазоне (оператор BETWEEN).

Остальные методы в классе занимаются подрузкой данных из нашего csv-файла в БД.

В каждом из методов подключен Logger из стандартной библиотке java.util для контроля ошибок, возникающих в ходе работе нашей программы.

Первое задание:
![1](https://user-images.githubusercontent.com/122276928/211313652-be407b50-4d01-43e6-8765-f96c30b8d30e.jpg)

Второе задание:
![2](https://user-images.githubusercontent.com/122276928/211313727-42a5d923-669c-485e-ac87-f8851da26d0d.jpg)

Третье задание:
![3](https://user-images.githubusercontent.com/122276928/211313920-9d906cdd-1582-45ff-ba51-a96164a0befb.jpg)


