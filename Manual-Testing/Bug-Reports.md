# Manual Testing

Мои практические баг-репорты.

# Bug Reports: Форма регистрации

**Project:** Регистрация пользователя  
**Type:** Manual Testing  
**Author:** Ulugbek Zinatov

---

## BUG-001: Система позволяет зарегистрироваться без Email

**Environment:**
- OS: Windows 11
- Browser: Google Chrome
- Test Type: Manual Testing

**Preconditions:**
- Открыта страница регистрации.
- Пользователь не зарегистрирован.

**Steps to Reproduce:**
1. Открыть страницу регистрации.
2. Заполнить все обязательные поля, кроме Email.
3. Нажать кнопку Register.

**Expected Result:**
Система должна запретить регистрацию и показать сообщение о том, что поле Email обязательно.

**Actual Result:**
Система успешно регистрирует пользователя без Email.

**Severity:** High

**Priority:** High

---

## BUG-002: Система принимает Email без символа @

**Environment:**
- OS: Windows 11
- Browser: Google Chrome
- Test Type: Manual Testing

**Preconditions:**
- Открыта страница регистрации.

**Steps to Reproduce:**
1. Открыть страницу регистрации.
2. Заполнить обязательные поля.
3. Ввести в поле Email значение `muslim.gmail.com`.
4. Нажать кнопку Register.

**Expected Result:**
Система должна отклонить некорректный Email и показать сообщение об ошибке.

**Actual Result:**
Система принимает некорректный Email и завершает регистрацию успешно.

**Severity:** Medium

**Priority:** High

---

## BUG-003: Пароль отображается открытым текстом

**Environment:**
- OS: Windows 11
- Browser: Google Chrome
- Test Type: Manual Testing

**Preconditions:**
- Открыта страница регистрации.

**Steps to Reproduce:**
1. Открыть страницу регистрации.
2. Перейти к полю Password.
3. Ввести пароль `Test12345`.

**Expected Result:**
Пароль должен отображаться скрытыми символами, например точками или звёздочками.

**Actual Result:**
Пароль отображается обычным открытым текстом.

**Severity:** High

**Priority:** High


---

# Bug Reports: Регистрация на VOLNA.TJ

**Project:** Сайт volna.tj  
**Type:** Manual Testing  
**Author:** Ulugbek Zinatov

---

## BUG-004: Ошибка при регистрации на сайте volna.tj

**Environment:**
- OS: Windows 11
- Browser: Google Chrome 157
- Test Type: Manual Testing

**Preconditions:**
- Открыта главная страница сайта https://volna.tj/.

**Steps to Reproduce:**
1. На главной странице нажать кнопку «Регистрация».
2. Ввести в поле «Имя»: Муслим.
3. Ввести в поле «Фамилия»: Алиев.
4. Ввести в поле «Логин»: Aliev1900.
5. Ввести в поле «Почта»: nttmmv4b@mail.ru.
6. Ввести проверочный код.
7. Нажать кнопку «Зарегистрироваться».

**Expected Result:**
Открывается страница личного кабинета с сообщением об успешной регистрации.

**Actual Result:**
Открывается страница с ошибкой: `DB query error. Please try later.`

**Severity:** Medium

**Priority:** High
