## __Создание микросервиса по материалам статьи по ссылке.__  
https://alimbekov.com/machine-learning-flask-rest-api/  

### Работа.  
> docker контейнер собирается командой __docker build -t iris .__  
> docker контейнер запускается командой __docker run -d -p 5000:5000 iris__ или из терминала !!!!  
> кроме того возможен запус не в контейнере, а "просто на машине" через __python rest_api.py__ , при таком запуске в последней строке необходимо поменять "коменты"

### В текущей версии веб сервис рабочий.   
> работает на адресе http://127.0.0.1:5000/iris/api/v1.0/getpred?sepal_length=5.1&sepal_width=3.5&petal_length=1.4&petal_width=0.2 или http://localhost:5000/iris/api/v1.0/getpred?sepal_length=5.1&sepal_width=3.5&petal_length=1.4&petal_width=1000    
> http://127.0.0.1 и port :5000 - прописывается в теле .py файла  
> __?sepal_length=5.1&sepal_width=3.5&petal_length=1.4&petal_width=0.2__ - входные параметры для запроса  
> запрос в postman делается через GET  
> веб сервис работает по адресу http://127.0.0.1:5000 (localhost) будучи запущенным и из контейнера и из командной строки !!!

### Содержание.  
> /logs - __рабочая__ папка с логами    
> compose.yaml - не задействован, может быть нужен для работы с множеством образов с docker-compose  
> dockerfile - __рабочий__ файл собирающий docker образ  
> flask_example.py - пример работы с flask, к работе веб сервиса не имеет отношения  
> model.py - __рабочий__ модуль симулирующий ML модель   
> requirements.txt - __рабочий__ файл зависимостей, по нему подтягиваются библиотеки для python в dockerfile    
> research.ipynb - не задействован, к работе веб сервиса не имеет отношения    
> rest_api.py - __рабочий__ основной исполняемый файл, он же может служить маршрутизатором API запросов   