# Interval Server Error на сторінці реєстрації при введенні 51+ символів у поле "Ім'я"
**ID**: BUG-001
**Priority**: High
**Severity**: High
**Status**: Open
**Enviroment**: Brave 1.91.180, Chromium: 149.0.7827.201
### Pre-conditions
1. Користувач не авторизований.
2. Відкрито сторінку реєстрації.
### Steps to reproduce
1. Ввести в поле "Ім'я" рядок із 51 символу (наприклад: OBraveNewWorldThatHasSuchPeopleInt!AVeryGoodLineFromShakespeare).
2. Заповнити поле "Email" валідними даними (наприклад: very_valid@gmail.com).
3. Заповнити поле "Пароль" валідними даними.
4. Натиснути кнопку "Зареєструватися".
### Expected Result
- Форма реєстрації не відправляється, користувач залишається на поточній сторінці.
- З'являється червоне повідомлення про помилку: "Перевищено ліміт символів. Максимальна довжина — 50".
### Actual Result
Сайт падає з помилкою Internal Server Error.
### Additional Info
- Відсутня клієнтська валідація.
- Відсутня серверна валідація моделі.
### Attachments
<img width="700" alt="image" src="https://github.com/user-attachments/assets/e4951769-3362-424e-b0f7-d3706795fa58" />
<img width="700" alt="image" src="https://github.com/user-attachments/assets/8ab79e31-f7aa-4571-8b85-88fe93a8e56a" />
<img width="700" alt="image" src="https://github.com/user-attachments/assets/e0032238-6aba-4f6c-8dd7-fde90bdf9dd5" />

