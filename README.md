# 1. Перечень автоматизируемых сценариев.
## 1.1 Тестируем переход с главной страницы сайта "Нетология" на страницу курса "Тестировщик"

1. Меню в шапке сайта "Каталог курсов":
* поиск по названию курса в поисковой строке,
* поиск через направление обучения, раздел "Программирование",
* поиск через список всех курсов.

2. Блок на главной странице "Направление обучения":
* поиск через раздел "Программирование",
* поиск через раздел "Курсы для новичков",
* поиск через полный каталог курсов.

3. Поиск через меню в футере сайта:
* поиск через раздел "Каталог курсов",
* поиск через раздел "Популярные курсы",
* поиск через раздел "Программирование".

**Ожидаемый результат раздела 1.1:** открывается страница курса "Тестировщик"

## 1.2 Тестируем отправку формы записи со страницы курса "Тестировщик"

**1.** Тестируем кнопку "Записаться" на первом экране страницы курса. *Ожидаемый результат:* переход к форме записи.

**2.** Тестируем кнопку "Записаться" в шапке страницы курса. *Ожидаемый результат:* переход к форме записи.

**3.** Тестируем отправку форму записи (кнопки "Записаться" и "Получить консультацию") на валидных и невалидных значениях.

**Позитивные сценарии:**
* Пользователь не авторизирован на сайте. Поля "Имя", "Телефон" и "Электронная почта" заполняем валидными данными. Нажимаем кнопку "Записаться".
*Ожидаемый результат:* "Ваша заявка успешно отправлена. Подробная информация будет выслана на вашу электронную почту".
* Пользователь не авторизирован на сайте. Поля "Имя", "Телефон" и "Электронная почта" заполняем валидными данными. Нажимаем кнопку "Получить консультацию".
*Ожидаемый результат:* "Ваша заявка успешно отправлена. Скоро с вами свяжется наш менеджер".
* Пользователь авторизирован на сайте. Поля "Имя" и "Телефон" заполняем валидными данными. Нажимаем кнопку "Записаться".
*Ожидаемый результат:* "Ваша заявка успешно отправлена. Подробная информация будет выслана на вашу электронную почту".
* Пользователь авторизирован на сайте. Поля "Имя" и "Телефон" заполняем валидными данными. Нажимаем кнопку "Получить консультацию".
*Ожидаемый результат:* "Ваша заявка успешно отправлена. Скоро с вами свяжется наш менеджер".

**Негативные сценарии:**
* Пользователь не авторизован на сайте. Поле "Имя" оставляем пустым, остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Имя" обведено красным, под ним появляется красная надпись "Обязательное поле". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь не авторизован на сайте. Поле "Имя" заполняем одной буквой, остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Имя" обведено красным, под ним появляется красная надпись "Должно быть не короче 2 символов". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь не авторизован на сайте. Поле "Имя" заполняем цифрой, остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Имя" обведено красным, под ним появляется красная надпись "Должно состоять из букв". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь не авторизован на сайте. Поле "Телефон" оставляем пустым, остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Телефон" обведено красным, под ним появляется красная надпись "Обязательное поле". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь не авторизован на сайте. Поле "Телефон" заполняем невалидными данными (буквы, спецзнаки, цифры в количестве меньше 9 и больше 15), остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Телефон" обведено красным, под ним появляется красная надпись "Номер в формате +9 (999) 999-99-99". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь не авторизован на сайте. Поле "Электронная почта" оставляем пустым, остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Электронная почта" обведено красным, под ним появляется красная надпись "Обязательное поле". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь не авторизован на сайте. Поле "Электронная почта" заполняем невалидными данными, остальные поля заполняем валидными значениями.
*Ожидаемый результат:* поле "Электронная почта" обведено красным, под ним появляется красная надпись "Неверный email". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь авторизован на сайте. Поле "Имя" оставляем пустым, другое поле заполняем валидными значениями.
*Ожидаемый результат:* поле "Имя" обведено красным, под ним появляется красная надпись "Обязательное поле". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь авторизован на сайте. Поле "Имя" заполняем одной буквой, другое поле заполняем валидными значениями.
*Ожидаемый результат:* поле "Имя" обведено красным, под ним появляется красная надпись "Должно быть не короче 2 символов". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь авторизован на сайте. Поле "Имя" заполняем цифрой, другое поле заполняем валидными значениями.
*Ожидаемый результат:* поле "Имя" обведено красным, под ним появляется красная надпись "Должно состоять из букв". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь авторизован на сайте. Поле "Телефон" оставляем пустым, другое поле заполняем валидными значениями.
*Ожидаемый результат:* поле "Телефон" обведено красным, под ним появляется красная надпись "Обязательное поле". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.
* Пользователь авторизован на сайте. Поле "Телефон" заполняем невалидными данными (буквы, спецзнаки, цифры в количестве меньше 9 и больше 15), другое поле заполняем валидными значениями.
*Ожидаемый результат:* поле "Телефон" обведено красным, под ним появляется красная надпись "Номер в формате +9 (999) 999-99-99". При нажатии кнопок "Записаться"/"Получить консультацию" форма не отправляется.


*Ожидаемый результат раздела 1.2 для валидных значений:* 
* при тестировании кнопки "Записаться" на указанный email приходит письмо с информацией о курсе.
* при нажатии кнопки "Получить консультацию" появление заявки в базе данных с отметкой о необходимости звонка менеджера.

# 2. Перечень используемых инструментов с обоснованием выбора.

1. Язык написания тестов - Java, включая следующие библиотеки:
* Faker для генерирования случайных пользователей
* Selenide для тестирования веб-интерфейсов
* REST Assured для тестирования отправки email
2. Среда разработки - IntelliJ IDEA 2022.3 (Community Edition)
3. Docker Compose для запуска контейнера с базой данных
4. Клиент для работы с БД - DBeaver
5. Appveyour для использования CI
6. Allure для формирования отчета об ошибках

# 3. Перечень необходимых разрешений, данных и доступов.

1. Разрешение от владельца сайта на тестирование веб-страницы.
2. Доступ к базе данных.
3. Доступ к API сайта.
4. Захардкоренный логин и пароль валидного юзера.

# 4. Перечень и описание возможных рисков при автоматизации.

1. Изменение верстки страницы курсов: может привести к изменению селекторов и падению тестов.
2. Изменение архитектуры сайта: может привести к появлению неохваченных сценариев.
3. Изменение формы записи, добавление или удаление полей: может привести к падению тестов.

# 5. Перечень необходимых специалистов для автоматизации.
QA engineer с навыками автоматизации (написание и поддержание тестов) - 1 человек.

QA Lead - анализ результатов, решение о поддержании/прекращении автоматизированного тестирования.

# 6. Интервальная оценка с учётом рисков в часах.
Написание автоматизированных тестов - 8-12 часов.

Поддержание актуальности автоматизированных тестов - 2 часа в неделю/8-10 часов в месяц.







