1) Запустила CouchDB в контейнере

   ![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/c720b71e-38d9-445a-a91e-875c1f3546df)

2) Открыла в браузере http://localhost:5984/_utils/

   ![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/a8733753-2ab9-4e9d-a341-ae166a4d9c85)

3) Вбила логин и пароль,которые указывала при запуске контейнера
   ![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/bd4c9329-5dad-4fe6-ac75-a67069e2edeb)

4) Создала базу ![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/59e45fbf-c3f4-4340-bae9-46bd09753fdb)

Добавила туда документ с фамилией, активировала CORS

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/023bf375-26d0-4cef-8fa2-de0251a5c5f1)

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/96601f6d-3975-4b30-b514-154083df3973)


5) Открыла html файл, изменила строку 25 под свою базу данных
   Remote: new PouchDB('http://admin:password@localhost:5984/hw3')
6) Открыла в браузере html-файл, нажала sync, как видим, фамилия там есть

![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/70668dd2-0269-4d5e-a495-a02bb01688a4)

7) Остановила контейнер

   ![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/0c80c25c-5804-4b26-a5fe-bd614be2cf52)


8) Снова открыла html файл, нажала sync, фамилия там осталась

   ![image](https://github.com/ilovethebeatles/SBT-DB/assets/106533857/7ae0aa7b-2ba7-4f65-b7fa-1709b10b45dc)









