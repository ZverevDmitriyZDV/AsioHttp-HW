#Скрипт выполняет задание описанное в файле [ReadMe.md](ReadMe.md)
В запросах через API сервера в качестве ответа приходит Json 
Некоторые значения являются ссылками на новые запросы API.
ПО заданию необходимо выгрузить в БД занчения в формате String, через запятую, если будут несколько ссылок на запрос

Данные Внутренние запросы создаются в асинхронном режиме
Подобными полями содержащими запросы являются:
```
add_request_key': ['homeworld', 'films', 'species', 'vehicles', 'starships']
```
Далее данные, полученные в качестве результата запроса отправляются в базу данных.
Запроса создаются через API и асинхронные запросы, с использованием инструментов asiohttp

Для запуска и корректной работы скрипта необходимо выполнить следующие этапы
<h4> Развернуть docker:</h4>
```
docker-compose up
```
убедитесь, что все порты свобоны. нужные : 8080 / 8081 / 5342


<h4>Запуск приложения</h4>
```
запустите файл upload-data-url-character в папке client_request
```