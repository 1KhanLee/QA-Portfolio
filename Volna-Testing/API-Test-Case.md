# API-тест-кейс: сайт volna.tj

**Проект:** Виджет JivoSite на сайте volna.tj  
**Тип тестирования:** Ручное API-тестирование (Postman)  
**Автор:** Ulugbek Zinatov

---

## API-TC-01: Проверка статуса виджета JivoSite

**Предусловие:**  
Postman открыт

**Шаги:**

1. Выбрать GET
2. Вставить URL:
   `https://node-sber1-az3-20.jivosite.com/widget/status/1218690/uGFRehn690?rnd=0.8253012259249709`
3. Нажать Send
4. Проверить Status Code
5. Проверить JSON Response Body

**Ожидаемый результат:**

1. Сервер возвращает успешный HTTP-ответ.
2. Ответ имеет формат JSON.
3. Присутствуют поля premium, maintenance, config_updated_ts, agents.
4. Типы данных соответствуют ожидаемым.

**Статус:** Пройден
