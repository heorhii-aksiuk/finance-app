
# React Finance App

## Требования

Нам нужно, чтобы вы реализовали решение для отображения данных котировок в пользовательском интерфейсе в режиме реального времени.

Данные о ценах доступны в локальном сервисе (см. информацию ниже). Любые дополнительные визуализации, показывающие, как изменились цены, будут плюсом. Тестирование также является важной частью этого задания. 

Требования:
- приложение должно подключаться к локально работающему сервису (бекенд)
- приложение должно отображать изменения цен для некоторых тикеров в режиме реального времени

Вы можете получить представление о том, как может выглядеть ваше приложение, на странице [Google Финансы](https://www.google.com/finance/).

В качестве бонуса вы можете реализовать (пожалуйста, опишите реализованный бонусный функционал в этом файле):
- любые дополнительные визуальные эффекты для выделения положительных или отрицательных изменений цен
- возможность включать/выключать тикеры пользователем
- возможность указать время интервала пользователем ???
- возможность добавить/удалить бегущую строку из группы просмотра ???
- любые дополнительные функции, которые вы считаете полезными

Вы должны использовать следующие технологии:
- React (желательно с hooks)
- Redux (с Redux-Thunk или любими дргуими Redux прослойки с которыми вы знакомы) или любую другую библиотеку управления состоянием, которую вы хотите
- Socket.io - для подключения к сервису
- любая UI-библиотека, которую вы хотите, или вы можете использовать только чистый CSS
- Библиотека тестирования

Мы будем оценивать следующие части:
- работоспособность: как работает ваше приложение
- структура проекта: как вы структурируете свои файлы
- качество кода: как вы пишете чистый, читаемый код (не стесняйтесь устанавливать и использовать ESLint и Prettier)
- знания React и его экосистемы: как вы вместе составляете и используете библиотеки
- тестирование: как вы можете протестировать свой код

## Как выполнить задание
1. Клонировать или разветвить этот репозиторий
2. Изменить содержимое папки `client`
3. Изменить содержимое папки `server` - если вы хотите выполнять бонусные задания
4. Зафиксируйте и отправьте свой код в свой репозиторий
5. Отправьте нам ссылку на ваш репозиторий

## Running the local service
1. Open a new bash shell
2. ```cd server```
3. ```npm install``` or ```yarn install```
4. ```npm run start``` or ```yarn start```
5. You can visit [http://localhost:4000](http://localhost:4000) to check that the service is working correctly and inspect the data it produces.

## Run your application
1. Open a new bash shell
2. ```cd client```
3. ```npm install``` or ```yarn install```
4. ```npm run start``` or ```yarn start```

## Run the tests
1. Open a new bash shell
2. ```cd client```
3. ```npm run test``` or ```yarn test```

# Price Service Usage

URL:
```http://localhost:4000```

Price tickers are real-time via web-sockets.

## Example JSON Response from the Price Ticker service
```json
[
  {
    "ticker": "AAPL",
    "exchange": "NASDAQ",
    "price": 279.29,
    "change": 64.52,
    "change_percent": 0.84,
    "dividend": 0.56,
    "yield": 1.34,
    "last_trade_time": "2021-04-30T11:53:21.000Z"
  },
  {"ticker":"GOOGL","exchange":"NASDAQ","price":237.08,"change":154.38,"change_percent":0.10,"dividend":0.46,"yield":1.18,"last_trade_time":"2021-04-30T11:53:21.000Z"},
  {"ticker":"MSFT","exchange":"NASDAQ","price":261.46,"change":161.45,"change_percent":0.41,"dividend":0.18,"yield":0.98,"last_trade_time":"2021-04-30T11:53:21.000Z"},
  {"ticker":"AMZN","exchange":"NASDAQ","price":260.34,"change":128.71,"change_percent":0.60,"dividend":0.07,"yield":0.42,"last_trade_time":"2021-04-30T11:53:21.000Z"},
  {"ticker":"FB","exchange":"NASDAQ","price":266.77,"change":171.92,"change_percent":0.75,"dividend":0.52,"yield":1.31,"last_trade_time":"2021-04-30T11:53:21.000Z"},
  {"ticker":"TSLA","exchange":"NASDAQ","price":272.13,"change":158.76,"change_percent":0.10,"dividend":0.96,"yield":1.00,"last_trade_time":"2021-04-30T11:53:21.000Z"}
]
```

The tickers we use:
- **AAPL** - Apple
- **GOOGL** - Alphabet
- **MSFT** - Microsoft
- **AMZN** - Amazon
- **FB** - Facebook
- **TSLA** - Tesla
