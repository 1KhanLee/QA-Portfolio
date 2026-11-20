# PUT - Update post

**Метод:** `PUT`

**URL:** `https://jsonplaceholder.typicode.com/posts/1`

**Заголовки:** `Content-Type: application/json`

**Тело запроса (Body → raw → JSON):**

```json
{
  "id": 1,
  "title": "updated title",
  "body": "updated body",
  "userId": 1
}
```

**Ожидаемый результат:**
Статус 200. В ответе пост с `id` = 1 и обновлёнными полями.

**Фактический результат:**
_Будет добавлен после выполнения запроса._

**Скриншот:**
_Будет добавлен после выполнения запроса._

**Статус:** не выполнен

[← Назад к API Testing](../README.md)
