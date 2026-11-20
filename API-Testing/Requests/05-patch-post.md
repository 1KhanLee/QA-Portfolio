# PATCH - Partially update post

**Метод:** `PATCH`

**URL:** `https://jsonplaceholder.typicode.com/posts/1`

**Заголовки:** `Content-Type: application/json`

**Тело запроса (Body → raw → JSON):**

```json
{
  "title": "patched title"
}
```

**Ожидаемый результат:**
Статус 200. В ответе пост с обновлённым `title`, остальные поля сохранены.

**Фактический результат:**
Статус 200 OK. В ответе вернулся объект:
```
{
    "userId": 1,
    "id": 1,
    "title": "patched title",
    "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```

**Статус:** Выполнен

[← Назад к API Testing](../README.md)
