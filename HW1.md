# Отчет по домашнему заданию №1

Для запуска MongoDB я использовала docker, он уже есть у меня на компьютере.

Выполняю в терминале команду (вначале я забыла, что нужно все скринить, но я выполнила вот такую команду: docker run -it -v mongodata:/data/db --name mongodb -d mongo)

Контейнер запущен:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/2a5df68d-c7ab-4639-9c6b-0f5c4e02868c)


Далее выбираю датасет, мною был выбран датасет Титаник, скачиваю его себе на компьютер.

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/b245381e-b9a9-4705-9a80-eaa19ee7413b)


Копирую файл с датасетом в контейнер
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/cfcdcdd0-85cb-49fa-a450-b89727dc96f0)

Открываю консоль контейнера и выполняю mongoimport для того, чтобы данные из csv стали коллекцией

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/5606679b-134c-48cd-a0ed-af6cea67b9bf)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/06070a3a-87b5-44ac-9edb-32c196e321c9)

Теперь захожу в Mongo Shell и проверяю, что все получилось:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/8c7bda8b-c1fd-4aec-a0e1-5d416a74c327)

Как видим, данные вставились успешно

Посмотрим, какие у нас есть колонки в таблице:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/170a82d5-d5d8-4c22-b17e-19abc281656c)

Выполним теперь CRUD-операции:

-Create:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/ba6852e5-bcde-418b-afdc-e65e09140b51)

-Read:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/cd914fb6-bced-4204-830a-2621d9da0c16)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/fe038c16-91be-47a6-8cbe-7f6678c047b6)



-Update:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/43b5df6d-e5bf-4249-9172-c8f964859eaf)



-Delete:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/5a77ca04-057b-4e7a-b38c-a6981e55a75f)

Индексы:

Найдем число данных в таблице

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/a558c89a-87d0-40d0-b863-a8ed87376b76)

Время выполнения запроса выборки до добавления индексов 1мс(поле executionTimeMillis)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/0eb2201b-74fa-4d76-bad0-fe557d4fe049)

После введения индекса ничего не изменилось

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/80a7cb09-e14a-4138-be6d-b70eebbb6b98)

Я предположила,что в моем датасете слишком мало данных, чтобы заметить влияние индексов, и запросы выборки и так происходят быстро.

Скачала датасет побольше, сделала из него collection

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/f0f14e28-9bf6-4e0a-a619-3b70403f47f7)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/620c065b-f4a3-4d1b-8a1e-0fcc21bc12b3)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/11ce7a05-b6d6-486a-a354-1aa035acf1a7)

Посмотрела информацию о датасете

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/a6d3b874-f4b5-4519-aeec-20b619ab0480)

Замерила время запроса без индексов
![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/38a50234-f76b-4f37-939b-8d85ee84e43e)

Завела индекс и повторила запрос с инддексом:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/27ca8a65-977b-416b-bdb3-86430177b3ba)

Время запроса ожидаемо уменьшилось. Но 1мс на фоне 3 и 2 мс это не очень показательно, поэтому я решила взять датасет еще больше

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/c5093130-36af-45d4-b737-64f6772b0aeb)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/4ea9a6c6-b1e7-472f-b891-f4b545150fbf)


![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/06fd3aa1-5902-4063-ac31-b8f96a96fc70)

Смотрю информацию о БД

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/68256403-e659-4a00-8918-bac278315d1f)

Запрос без индекса

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/34efba76-12fe-45e2-a9cb-f95d7605e2a4)

Делаем индекс, снова выполняем:

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/856391a9-1423-4354-81de-2a6ce345365d)
На этом датасете польза от индексов гораздо нагляднее



























