# API Testing

Мои практические работы по тестированию API в Postman.

**Автор:** Ulugbek Zinatov  
**Инструменты:** Postman

## Проект: JSONPlaceholder API

**Тестируемый API:** https://jsonplaceholder.typicode.com (ресурс `/posts`)  
**Коллекция:** [JSONPlaceholder-API-Requests.postman_collection.json](postman/JSONPlaceholder-API-Requests.postman_collection.json)  
**Статус:** в работе

### Запросы

Каждый запрос описан в отдельном файле: метод, URL, заголовки, тело, ожидаемый результат, фактический результат и скриншот.

| Запрос | Метод и URL | Ожидаемый результат |
|---|---|---|
| [GET - Get all posts](Requests/01-get-all-posts.md) | `GET /posts` | Статус 200 |
| [GET - Get post by ID](Requests/02-get-post-by-id.md) | `GET /posts/1` | Статус 200 |
| [POST - Create post](Requests/03-create-post.md) | `POST /posts` | Статус 201 |
| [PUT - Update post](Requests/04-update-post.md) | `PUT /posts/1` | Статус 200 |
| [PATCH - Partially update post](Requests/05-patch-post.md) | `PATCH /posts/1` | Статус 200 |
| [DELETE - Delete post](Requests/06-delete-post.md) | `DELETE /posts/1` | Статус 200 |
| [GET - Get non-existent post (негативный)](Requests/07-get-nonexistent-post.md) | `GET /posts/9999` | Статус 404 |

## Структура папки

```
API-Testing/
├── README.md
├── Requests/       # описание каждого запроса отдельным файлом
├── postman/        # экспорт Postman-коллекции (.json)
└── screenshots/    # скриншоты запросов и прогона коллекции
```

## Как запустить коллекцию

1. Скачать файл коллекции из папки `postman/`.
2. В Postman нажать **Import** и выбрать файл.
3. Открыть нужный запрос и нажать **Send**.

Адрес API хранится в переменной коллекции `baseUrl`.

## Результаты

Будут добавлены после выполнения запросов: скриншоты ответов и найденные отличия от ожидаемого результата. Баг-репорты по API оформляю в формате [Bug-Reports](../Manual-Testing/Bug-Reports.md), в шагах указываю метод, URL, тело запроса и фактический статус-код.

> JSONPlaceholder — учебный сервис: запросы на изменение (POST, PUT, PATCH, DELETE) имитируются, реально данные на сервере не меняются.
