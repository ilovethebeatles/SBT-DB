# Отчет по базе данных Yellowbrick DataWarehouse

a.История развития

Yellowbrick Data Warehouse была создана в 2014 году в Калифорнии Нилом Карсоном, Джимом Доусеном и Марком Бриникомбе. Основной идеей было создание СУБД, оптимизированной для аналитических запросов на больших объемах данных с высокой скоростью обработки. Система быстро нашла своих пользователей среди крупных компаний благодаря своей способности обрабатывать транзакции и аналитические запросы в режиме реального времени. С течением времени компания привлекла значительные инвестиции(в числе ее инвесторов есть такие крупные компании как Samsung и BMW) и расширила свои возможности, добавив поддержку облачных технологий.

b.Инструменты для взаимодействия с СУБД
С Yellowbrick можно взаимодействовать через вэб-интерфейс, в нем можно смотреть на состояние таблиц и кластеров, создавать их, писать и выполнять sql-запросы и многое другое:
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/2bf790f2-ed85-41ce-a17f-227bc500f0a6)
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/a59832a3-eab8-406e-af3b-ce47c065cadb)
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/345b25f3-835d-4316-9957-31969098a41f)
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/ea1bf536-92f7-44c2-8b35-87af2357ce10)
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/77e2328f-9716-418a-b832-df87d06fa66f)


c. Какой database engine используется в вашей СУБД?

d. Как устроен язык запросов в вашей СУБД? Разверните БД с данными и выполните ряд запросов. 
Для написания запросов в Yellowbrick используется такой же синтаксис как в PostgreSQL. 

Yellowbrick Data Warehouse - это платное программное обеспечение, однако можно запросить бесплатный период:
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/74da6cc4-2414-4310-96a7-7b1748c392c0)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/beeefc06-0bb6-4a64-b464-1e95730fdbdb)
Переходим на сайт из таблички со скрина выше и вводим логин и пароль из таблички
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/52c885d3-ea5c-4dc7-a622-a3cbf7e5a012)
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/a90be4c2-8c87-496b-9057-9a422c59bc5e)
В пробном аккаунте уже есть примеры баз данных
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/0340c3c7-bbc2-4f8f-9640-55b8e2f0f1bd)

Выполним запрос выборки в специальном окне:
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/07d8db7e-f3d4-4422-9e1a-58ff0958f713)

Вот его результат:
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/7a3f4f72-ce51-41dc-b72d-c37979ea6c26)

Учитывая сложность запроса, отработал он довольно быстро

Выполним запрос на создание таблицы

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/837bc06c-7cd7-48a1-bc55-7362bda75900)

Как видим, у нас появилась таблица student
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/f6688a52-8398-496a-ae52-a20d7ac98776)

Вставим в нее что-нибудь

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/0ca4a2ec-6015-4056-8e4b-83006e64f36a)

Посмотрим, что в нашей таблице

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/bcffe520-fe3f-43b2-8552-91478fc4c41b)

Удалим эту запись из таблицы

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/3d4229a9-9c8c-4dfb-a91d-acec02fa24c9)


e. Распределение файлов БД по разным носителям?
f. На каком языке/ах программирования написана СУБД?
Yellowbrick написана на С++.
g. Какие типы индексов поддерживаются в БД? Приведите пример создания индексов.


h. Как строится процесс выполнения запросов в вашей СУБД?
i. Есть ли для вашей СУБД понятие «план запросов»? Если да, объясните, как работает данный этап.
j. Поддерживаются ли транзакции в вашей СУБД? Если да, то расскажите о нем. Если нет, то существует ли альтернатива?
k. Какие методы восстановления поддерживаются в вашей СУБД. Расскажите о них.
