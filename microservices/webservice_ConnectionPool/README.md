## __Создание микросервиса по материалам статьи по ссылке.__  
https://alimbekov.com/machine-learning-flask-rest-api/  
На вход подаем customer_id в ответ получаем данные о клиенте      

### Работа в контейнере.  
> docker контейнер собирается командой __docker build -t connectionpool .__  
> docker контейнер запускается командой __docker run -d -p 5050:80 connectionpool__ или из docker терминала (при существующем контейнере и прописанных портах) 
> 5050 - порт на котором можно запустить из браузера прописывается в docker run, 80 порт в docker прописывается в теле .py файла !!!
> __docker run -d -p 5050:80 connectionpool__ :5050 порт хоста с которым устанавливается связь, :80 порт в контейнере с которым уст-ся связь
> бля мочему-то из докера локально работает только на :5000 !!! хз ??? разобрался бы что ль!!! РАЗОБРАЛСЯ!!!-все работает, любой порт порписывается "и там и там" 
> работает на адресе http://127.0.0.1:5050/query?id=10100 или http://localhost:5050/query?id=10100 
> host='172.17.0.2' (ip адрес докер контейнера на локальной машине) и port :5000 - прописывается в теле .py файла  
> __?id=10100__ - входные параметры для запроса    
> запрос в postman делается через POST

### Работа через терминал.  
> веб сервис запускается из командной строки __python rest_api.py__
> работает на адресе http://127.0.0.1:5070/query?id=10100 или http://localhost:5070/query?id=10100 
> http://127.0.0.1 и port :5070 - прописывается в теле .py файла  
> __?id=10100__ - входные параметры для запроса  
> запрос в postman делается через POST


### Содержание.  
> /logs - __рабочая__ папка с логами    
> compose.yaml - не задействован, может быть нужен для работы с множеством образов с docker-compose  
> dockerfile - __рабочий__ файл собирающий docker образ  
> flask_example.py - пример работы с flask  
> model.py - __рабочий__ модуль симулирующий ML модель   
> requirements.txt - __рабочий__ файл зависимостей, по нему подтягиваются библиотеки для python в dockerfile    
> research.ipynb - не задействован  
> rest_api.py - __рабочий__ основной исполняемый файл, он же может служить маршрутизатором API запросов  