# Домашнее задание к занятию «4.2. Заключительная лекция»
### Введение
Создание плана тестирования формы записи на обучения для понимания стратегия тестирования, целей, графика, оценки, результатов и ресурсов, необходимые для выполнения тестирования.

### Цель плана: 
Описание процесса автоматизации тестирования для всех участников процесса разработки продукта.

- ### Цель тестирования:
Выявить как можно больше недостатков программного обеспечения и убедиться, что тестируемый продукт не содержит ошибок.

- ### Виды тестирования:

1. Модульное тестирование
2. Тестирование черного/белого ящика
3. Граничные значения

- ### Перечень используемых инструментов 
    1. **IntelliJ IDEA** - Интегрированная среда разработки программного обеспечения. Предлагает эффективные встроенные инструменты.
    2. **Java JDK 11** - среда разработки программного обеспечения, 
    3. **Gradle** - система автоматической сборки для автотрестов система автоматической сборки, которую используют для упрощения работы с Java. С помощью (условно) стандартизированных средств помогает собрать требуемые автотесты с экономией времени на их реализацию.
    4. **Faker** - библиотека генерации случайных данных. Удобные настройки для генерации требуемых данных для тестирования.
    5. **JUnit 5** - инфраструктура модульного тестирования для Java. Содержит не только исчерпывающую документацию по фреймворку, но и множество примеров их реализации.
    6. **Selenide** - фреймворк для автоматизированного тестирования веб-приложений. Удобный инструмент для написания автотестов и дальнейшего их использования для регрессионного тестирования.
    7. **Allure Framework**  - получение подробно отчетности в удобном виде. Подойдет для анализа и информативности процесса тестирования для всей команды разработки.

- ### Перечень необходимых разрешений/данных/доступов
    1. Потребуется предоставление доступа к тестовой среде. С конфигурацией программного и аппаратного обеспечения с возможностью использовать бизнес-среду и пользовательскую среду. 
    2. Доступы для проверки формы по зарегистрированным пользователям.

- ###  Перечень и описание возможных рисков при автоматизации

| Риск | Краткое описание | 
|----:|:------|
|Изменения структуры сайта | Перенос ссылок для возможного попадания на форму |
|Изменение полей формы | Добавление или удаление данных требуемы для отправки формы |
| Изменение CSS- селекторов | Изменения данных на наименованию форм |
| Изменение названия | Смена наименования профессии. |
|Изменения HTML | Изменения текста отклика на правильные или неправильные действия пользователя|
| Удаление профессии | Отсутствие формы на сайте  |

- ###  Перечень необходимых специалистов для автоматизации
    Специалист по автоматизации тестирования

- ###  Перечень автоматизируемых сценариев
    1. Поиск курса "Тестировщик ПО";
    2. Поиск формы записи на курс обучения;

    Позитивные тесты:
        1. Запись на курс авторизированного пользователя;
        2. Запись на курс неавторизированного пользователя;
        3. Тестирование поля "Имя";
        4. Тестирование поля "Телефон";
        5. Тестирование поля "Электронная почта";
        6. Тестирование кнопки "Записаться";
        7. Тестирование кнопки "Получить консультацию";
        8. Тестирование ссылки "политики";
        9. Тестирование ссылки "пользовательское соглашение";

    Негативные тесты:
        1. Запись на курс авторизированного пользователя;
        2. Запись на курс неавторизированного пользователя;
        3. Тестирование поля "Имя" с неверными данными;
        4. Тестирование поля "Телефон" с неверными данными;
        5. Тестирование поля "Электронная почта" с неверными данными;

- ### Перечень автотестов
    1. Поиск курса "Тестировщик ПО":
        1. вариант: На главной страницы сайта Netology.ru, выпадающего меню "Каталог курсов" - Программирование - Тестировщик ПО;
        2. вариант: На главной страницы сайта Netology.ru, выпадающего меню "Каталог курсов" - Полный каталог - Тестировщик ПО;
        3. Вариант: На главной страницы сайта Netology.ru, раздел "Направления обучения" - Программирование - Тестировщик ПО;
        4. вариант: На главной страницы сайта Netology.ru, с помощью картинки с надписью "НЕО для начинающих" - Тестировщик ПО;
        5. вариант: На главной страницы сайта Netology.ru, после раздела "Раскройте свои сильные стороны", с помощью кнопки "Выбрать курс" - Тестировщик ПО;
        6. вариант: На главной страницы сайта Netology.ru, в подвале "Каталог курсов" - Тестировщик ПО;

    2. Поиск формы записи на курс обучения:
        1. вариант: На странице "Тестировщик ПО" - нажать на кнопку "Записаться";
        2. вариант: На странице "Тестировщик ПО" - прокрутить страницу до формы для записи на курс;

    3. **Позитивные тесты:**
        1. Запись на курс обучения авторизованного пользователя;
            <details>
            1. Авторизоваться на сайте Netology.ru;
            2. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            3. Поля "Имя" и "Телефон" заполнены автоматически;
            4. Нажать кнопку "Записаться";
            5. Появилось сообщение "Заявка принята. В ближайшее время с Вами свяжется наш менеджер";
            </details>
        2. Запись на курс обучения неавторизованного пользователя;
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. В поле "Имя" ввести валидные данные;
            3. В поле "Телефон" ввести валидные данные;
            4. В поле "Электронная почта" ввести валидные данные;
            5. Нажать кнопку "Записаться";
            6. Появилось сообщение "Заявка принята. В ближайшее время с Вами свяжется наш менеджер";
            </details>
        3. Запись на курс пользователя с буквой "Ё" в имени
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. В поле "Имя" ввести валидные данные с буквой "Ё";
            3. В поле "Телефон" ввести валидные данные;
            4. В поле "Электронная почта" ввести валидные данные;
            5. Нажать кнопку "Записаться";
            6. Появилось сообщение "Заявка принята. В ближайшее время с Вами свяжется наш менеджер";
            </details>
        4. Тестирование кнопки "Получить консультацию";
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. В поле "Имя" ввести валидные данные;
            3. В поле "Телефон" ввести валидные данные;
            4. В поле "Электронная почта" ввести валидные данные;
            5. Нажать кнопку "Получить консультацию";
            6. Появилось сообщение "Заявка принята. В ближайшее время с Вами свяжется наш менеджер";
            </details>
        5. Тестирование ссылки "политики";
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Клик на ссылку "политика;
            3. Открылась страница "Политика обработки персональных данных пользователя сайта"
            </details>
        6.  Тестирование ссылки "пользовательское соглашение";
             <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Клик на ссылку "пользовательское соглашение"
            3. Открылась страница "Пользовательское соглашение"
            </details>
    4. **Негативный тест:**
        1. Поле "Имя" с одним символом:
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" значение из одной буквы;
            3. Внести  в поле "Телефон" валидное значение;
            4. Поле "Имя" подсвечивается красным, текст ошибки "Должно быть не короче 2 символов";
            </details>
        2. Поле "Имя" с спецсимволами
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" значение с спецсимволами;
            3. Внести в поле "Телефон" валидное значение;
            4. Поле "Имя" подсвечивается красным, текст ошибки "Должно состоять из букв";
            </details>
        3. Поле "Имя" с цифрами
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" значение с цифрами;
            3. Внести в поле "Телефон" валидное значение;
            4. Поле "Имя" подсвечивается красным, текст ошибки "Должно состоять из букв";
            </details>
        4. Поле "Имя" пустое
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Телефон" валидное значение;
            3. Поле "Имя" подсвечивается красным, текст ошибки "Обязательное поле";
            </details>
        5. Поле "Телефон" пустое
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. Оставить поле "Телефон" пустым
            4. Поля "Телефон" подсвечивается красным, текст ошибки "Обязательное поле";
            </details>
        6. Поле "Телефон" с буквами
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. Внести в поле "Телефон" значение с буквами;
            4. Поле "Телефон" подсвечивается красным, текст ошибки "Номер в формате +9 (999) 999-99-99";
            </details>
        7. Поле "Телефон" с спецсимволами
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. Внести в поле "Телефон" значение с спецсимволами;
            4. Поле "Телефон" подсвечивается красным, текст ошибки "Номер в формате +9 (999) 999-99-99";
            </details>
        8. Поле "Телефон" граничные значений 1 символ
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. Внести в поле "Телефон" значение с одной цифрой;
            4. Поле "Телефон" подсвечивается красным, текст ошибки "Номер в формате +9 (999) 999-99-99";
            </details>
        9. Поле "Телефон" граничные значения 10 символом
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. Внести в поле "Телефон" значение в 10 цифр;
            4. Поле "Телефон" подсвечивается красным, текст ошибки "Номер в формате +9 (999) 999-99-99";
            </details>
        10. Поле "Телефон" граничные значения 12 символов
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. Внести в поле "Телефон" значение в 12 цифр;
            4. Поле "Телефон" подсвечивается красным, текст ошибки "Номер в формате +9 (999) 999-99-99";
            </details>
        11. Поле "Электронная почта" пустое, незарегистрированный пользователь
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. В поле "Телефон" ввести валидные данные;
            4. Поле "Электронная почта" оставить пустым;
            5. Поле "Электронная почта" подсвечивается красным, текст ошибки "Обязательное поле";
            </details>
        12. Поле "Электронная почта" без "@", незарегистрированный пользователь
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. В поле "Телефон" ввести валидные данные;
            4. Поле "Электронная почта" заполнить значением без @ 
            5. Поле "Электронная почта" подсвечивается красным, текст ошибки "Неверный email";
            </details>
        13. Поле "Электронная почта" без домена верхнего уровня, незарегистрированный пользователь
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. В поле "Телефон" ввести валидные данные;
            4. Поле "Электронная почта" заполнить значением без домена верхнего уровня;
            5. Поле "Электронная почта" подсвечивается красным, текст ошибки "Неверный email";
            </details>
        14. Поле "Электронная почта" с пустым значением до "@", незарегистрированный пользователь
            <details>
            1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;
            2. Внести в поле "Имя" валидное значение;
            3. В поле "Телефон" ввести валидные данные;
            4. Поле "Электронная почта" заполнить с пустым значением до символа @ 
            5. Поле "Электронная почта" подсвечивается красным, текст ошибки "Неверный email";


- ### Интервальная оценка с учётом рисков (в часах)
    Для написания тестов, тестирования, подготовки отчетности необходимо 30-50 часов. 
    В зависимости от квалификации специалиста по тестирования.