# TransferMoneyService
Курсовой проект «Сервис перевода денег»


#### Перевод с карты на карту
## Описание проекта
Разработка backend API для Сервиса перевода денег. [Техническое задание проекта](https://github.com/serp-ya/card-transfer).

## Запуск
Для **запуска** приложения, необходимо склонировать репозиторий, подключить приложение [Docker](https://www.docker.com/products/docker-desktop/) 
к Intellij Idea Ultimate и запустить файл docker-compose, либо найти файл TransferMoneyServiceApplication и запустить его напрямую.

## Описание проекта
Проект предоставляет UI для перевода денег с карты на карту. В видимой части приложения присутствуют две карты (откуда и куда переводить), 
поле ввода суммы перевода и кнопка "отправить".


Логгирование всех операция производится в [файл](https://github.com/maxroker22/transfermoneyservice/blob/main/transferMoney.log).


## Запросы
Запросы поступают на сервер http://localhost:5500

Эндпоинты:
`/transfer` - принимает объект с данными формы
`/confirmOperation` - принимает объект с айди операции и секретным кодом

При возникновении ошибки на стороне сервера, будет отображено модальное окно с текстом ошибки, которую сервер прислал в поле `message` ответа.

Весь API FRONT был описан в соответствии [YAML](https://github.com/netology-code/jd-homeworks/blob/master/diploma/MoneyTransferServiceSpecification.yaml).

