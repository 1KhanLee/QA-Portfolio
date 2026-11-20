# API Testing

Мои практические работы по тестированию API в Postman.

**Автор:** Ulugbek Zinatov  
**Инструменты:** Postman, JavaScript (тесты в Postman)

## Проект: JSONPlaceholder API

**Тестируемый API:** https://jsonplaceholder.typicode.com (ресурс `/posts`)  
**Коллекция:** [JSONPlaceholder-API-Tests.postman_collection.json](postman/JSONPlaceholder-API-Tests.postman_collection.json)  
**Статус:** тесты написаны, результаты прогона добавляются

### Запросы и проверки

| Запрос | Метод и URL | Проверки |
|---|---|---|
| Get all posts | `GET /posts` | статус 200, ответ — список |
| Get post by ID | `GET /posts/1` | статус 200, `id` равен 1 |
| Create post | `POST /posts` | статус 201, в ответе есть `id` |
| Update post | `PUT /posts/1` | статус 200, `title` обновился |
| Partially update post | `PATCH /posts/1` | статус 200, `title` обновился |
| Delete post | `DELETE /posts/1` | статус 200 |
| Get non-existent post (негативный) | `GET /posts/9999` | статус 404 |

Всего 7 запросов и 12 проверок.

### Пример теста

```javascript
pm.test("Статус 200", () => pm.response.to.have.status(200));
pm.test("id равен 1", () => pm.expect(pm.response.json().id).to.eql(1));
```

## Структура папки

```
API-Testing/
├── README.md
├── postman/        # экспорт Postman-коллекции (.json)
└── screenshots/    # скриншоты запросов и прогона коллекции
```

## Как запустить коллекцию

1. Скачать файл коллекции из папки `postman/`.
2. В Postman нажать **Import** и выбрать файл.
3. Открыть коллекцию и запустить через **Run collection** (Collection Runner).

Адрес API хранится в переменной коллекции `baseUrl`.

## Результаты

Будут добавлены после прогона в Collection Runner: сколько проверок пройдено и не пройдено, найденные дефекты. Баг-репорты по API оформляю в формате [Bug-Reports](../Manual-Testing/Bug-Reports.md), в шагах указываю метод, URL, тело запроса и фактический статус-код.

> JSONPlaceholder — учебный сервис: запросы на изменение (POST, PUT, PATCH, DELETE) имитируются, реально данные на сервере не меняются.
