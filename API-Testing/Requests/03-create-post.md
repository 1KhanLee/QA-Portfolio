# POST - Create post

**Метод:** `POST`

**URL:** `https://jsonplaceholder.typicode.com/posts`

**Заголовки:** `Content-Type: application/json`

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
_Будет добавлен после выполнения запроса._

**Скриншот:**
_Будет добавлен после выполнения запроса._

**Статус:** не выполнен

[← Назад к API Testing](../README.md)
