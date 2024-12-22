# Лабораторная работа #8. RPC. gRPC. Protobuf

## Запуск и развёртывание

```bash
docker-compose up --build
```
![alt text](1.jpg)
![alt text](2.jpg)
## Демонстрация
### Swagger
![alt text](3.jpg)

### Получение списка всех терминов.

```
curl -X 'GET' \
  'http://localhost:8000/terms/?skip=0&limit=100' \
  -H 'accept: application/json'
```
![alt text](4.jpg)



### Получение информации о конкретном термине по ключевому слову.


``` 
curl -X 'GET' \
  'http://localhost:8000/terms/search/?keyword=api' \
  -H 'accept: application/json'
```
![alt text](5.jpg)

### Получение термина по id

```
curl -X 'GET' \
  'http://localhost:8000/terms/2' \
  -H 'accept: application/json'
```
![alt text](6.jpg)

### Добавление нового термина с описанием.
```
curl -X 'POST' \
  'http://localhost:8000/terms/' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "keyword": "keyw123",
  "description": "321desc"
}'
```
![alt text](7.jpg)
### Обновление существующего термина.

```
curl -X 'PUT' \
  'http://localhost:8000/terms/26' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "keyword": "api",
  "description": "update3333"
}'
```
![alt text](8.jpg)

### Удаление термина из глоссария.

``` 
curl -X 'DELETE' \
  'http://localhost:8000/terms/26' \
  -H 'accept: application/json'
```

![alt text](9.jpg)
