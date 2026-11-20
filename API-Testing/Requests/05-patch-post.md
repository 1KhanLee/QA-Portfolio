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
_Будет добавлен после выполнения запроса._

**Скриншот:**
_Будет добавлен после выполнения запроса._

**Статус:** не выполнен

[← Назад к API Testing](../README.md)
