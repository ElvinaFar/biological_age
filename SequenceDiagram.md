...

sequenceDiagram
  Пользователь  ->>  Сайт: Авторизацияю
  Сайт ->>  API: Отправка логин и пароля
  API ->> Сайт: 
  Сайт ->> Сайт: Вход в личный кабинет
  Пользователь  ->>  Сайт: Загружает данные пульсоксиметр
  Сайт ->>  API: Обработка полученных данных
  API  ->>  БД: Отправка запроса на сравнение полученных данных
  БД- ->>  API: Возвращает результат
  API  ->>  Сайт: Формирует результат
  Сайт ->>  Сайт: Показывает результат
...

[![](https://mermaid.ink/img/pako:eNqVksFKw0AQhl9l2XN9gRwKgh68CV5zCc2qRZNqmhykFNKUIqIXi-BNEXyANjYmtU37CjNv5L-bSIuHojkkM7sz3_z5d3uy1XGVtGRXXUfKb6mDtnMWOJ7tCzz0Sita8APl-KY04YQynYu9ZlPQG01ozoklaMwjFMwEpYIWVPAtlXxPc0FfKJlSQSVlnPyP-Yzog2Me0icitAuaISgNOhO0xg7aeADMUu9zXA-oGZq3f3wE1AtNOTZKVpgGTeg2IoZQmlVIHm3xeVSh0F7JeqQnzUH32pDSipIj1AsrqEBa4sWDuqA05MJI_dMwPWSjeYyenFIN47vaACQZ5fV_J9q6XzI37r1DUwxfCuPgruZtu7YA-pT06eVwO90xX0NkQ3oq8Jy2i4vU0yu2DM-Vp2xpIXSd4MKWtt9HXXTlOqE6dNthJ5DWqXPZVQ3pRGHn5MZvSSsMIvVTVN_Euqr_DfTJgXw)](https://mermaid-js.github.io/mermaid-live-editor/edit/#pako:eNqVksFKw0AQhl9l2XN9gRwKgh68CV5zCc2qRZNqmhykFNKUIqIXi-BNEXyANjYmtU37CjNv5L-bSIuHojkkM7sz3_z5d3uy1XGVtGRXXUfKb6mDtnMWOJ7tCzz0Sita8APl-KY04YQynYu9ZlPQG01ozoklaMwjFMwEpYIWVPAtlXxPc0FfKJlSQSVlnPyP-Yzog2Me0icitAuaISgNOhO0xg7aeADMUu9zXA-oGZq3f3wE1AtNOTZKVpgGTeg2IoZQmlVIHm3xeVSh0F7JeqQnzUH32pDSipIj1AsrqEBa4sWDuqA05MJI_dMwPWSjeYyenFIN47vaACQZ5fV_J9q6XzI37r1DUwxfCuPgruZtu7YA-pT06eVwO90xX0NkQ3oq8Jy2i4vU0yu2DM-Vp2xpIXSd4MKWtt9HXXTlOqE6dNthJ5DWqXPZVQ3pRGHn5MZvSSsMIvVTVN_Euqr_DfTJgXw)

# Предусловия
* Пользователь должен быть зарегистрирован и авторизован
* У пользователя должен быть пульсоксиметр

# Постусловия
* Заключение на основе диагнозов сгенерировано

# Сценарий
* Пользователь заходит в личный кабинет
* Загружает данные пульсоксиметра
* Сайт обрабатывает полученные данные
* API отправляет запрос БД на сравнение полученных данных
* БД возвращает полученный результат
* API формирует результат
* Сайт отображает полученный результат
