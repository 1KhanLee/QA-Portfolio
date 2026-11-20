# API Testing

Мои практические работы по тестированию API в Postman.

**Автор:** Ulugbek Zinatov  
**Инструменты:** Postman

## Проект: JSONPlaceholder API

**Тестируемый API:** https://jsonplaceholder.typicode.com (ресурс `/posts`)  
**Коллекция:** [JSONPlaceholder-API-Requests.postman_collection.json](postman/JSONPlaceholder-API-Requests.postman_collection.json)  
**Статус:** в работе

### Запросы

| Запрос | Метод и URL | Ожидаемый результат |
|---|---|---|
| Get all posts | `GET /posts` | статус 200, в ответе список постов |
| Get post by ID | `GET /posts/1` | статус 200, пост с `id` = 1 |
| Create post | `POST /posts` | статус 201, в ответе есть `id` нового поста |
| Update post | `PUT /posts/1` | статус 200, `title` изменён |
| Partially update post | `PATCH /posts/1` | статус 200, `title` изменён |
| Delete post | `DELETE /posts/1` | статус 200, пустой объект `{}` |
| Get non-existent post (негативный) | `GET /posts/9999` | статус 404, пустой объект `{}` |

Для каждого запроса сравниваю фактический статус-код и тело ответа с ожидаемыми.

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
3. Открыть нужный запрос и нажать **Send**.

Адрес API хранится в переменной коллекции `baseUrl`.

## Результаты

Будут добавлены после выполнения запросов: скриншоты ответов и найденные отличия от ожидаемого результата. Баг-репорты по API оформляю в формате [Bug-Reports](../Manual-Testing/Bug-Reports.md), в шагах указываю метод, URL, тело запроса и фактический статус-код.

> JSONPlaceholder — учебный сервис: запросы на изменение (POST, PUT, PATCH, DELETE) имитируются, реально данные на сервере не меняются.
