# API Testing

Мои практические работы по тестированию API в Postman.

**Автор:** Ulugbek Zinatov  
**Инструменты:** Postman, JavaScript (тесты в Postman)

## Проект: JSONPlaceholder API

**Тестируемый API:** https://jsonplaceholder.typicode.com (ресурс `/posts`)  
**Коллекция:** [JSONPlaceholder-API-Tests.postman_collection.json](postman/JSONPlaceholder-API-Tests.postman_collection.json)  
**Статус:** тесты написаны, результаты прогона добавляются

### Запросы и проверки

| Запрос | Метод и URL | Ожидаемый код | Проверки |
|---|---|---|---|
| Get all posts | `GET /posts` | 200 | код ответа, Content-Type, время ответа, массив из 100 постов, поля `userId`, `id`, `title`, `body` |
| Get post by ID | `GET /posts/1` | 200 | код ответа, Content-Type, время ответа, `id` равен 1, типы полей |
| Create post | `POST /posts` | 201 | код ответа, Content-Type, время ответа, есть `id`, данные совпадают с отправленными |
| Update post | `PUT /posts/1` | 200 | код ответа, время ответа, `id` равен 1, данные совпадают с отправленными |
| Partially update post | `PATCH /posts/1` | 200 | код ответа, время ответа, `title` обновился, остальные поля на месте |
| Delete post | `DELETE /posts/1` | 200 | код ответа, время ответа, тело — пустой объект |
| Get non-existent post (негативный) | `GET /posts/9999` | 404 | код ответа, время ответа, тело — пустой объект |

Всего 7 запросов и 29 проверок.

### Пример теста

```javascript
pm.test("Код ответа 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Ответ — массив из 100 постов", function () {
    const json = pm.response.json();
    pm.expect(json).to.be.an("array");
    pm.expect(json).to.have.lengthOf(100);
});
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
