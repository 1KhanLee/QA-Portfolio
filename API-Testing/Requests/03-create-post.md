# POST - Create post

**Метод:** `POST`

**URL:** `https://jsonplaceholder.typicode.com/posts`

**Тело запроса (Body → raw → JSON):**

```json
{
  "title": "test title",
  "body": "test body",
  "userId": 1
}
```

**Ожидаемый результат:**
Статус 201. В ответе данные отправленного поста и новый `id`.

**Фактический результат:**
Статус 201 Created. В ответе вернулся объект:
```json
{
    "title": "test title",
    "body": "test body",
    "userId": 1,
    "id": 101
}
```

**Статус:** Выполнен

[← Назад к API Testing](../README.md)
