# Переводчик

Это веб-приложение для тестового задания в Финтех Т-банка 2024. Данный веб-сервис будет полезен для перевода как отдельных слов, так и целых предложений. На вход принимается 3 параметра: язык исходного сообщения, язык, на который сообщение должно быть переведено, и само сообщение.

## Инструкция по запуску

1. **Склонируйте репозиторий:**
    ```bash
    git clone https://github.com/21MokseM12/Translator_T-bank_2024_Web_App
    ```

2. **Подготовьте базу данных:**
    1. В директории `bd` лежат SQL скрипты, которые необходимо выполнить в новой базе данных. Эти скрипты создадут необходимые таблицы и зависимости.

3. **Откройте проект в среде разработки Intellij IDEA.**

4. **Откройте файл `./src/main/resources/application.properties` и измените поля `db.url`, `db.username`, `db.password` в соответствии с вашим URL базы данных, именем пользователя и паролем соответственно.**

5. **Запустите `main` метод класса `App`.**

6. **Веб-сервис работает по адресу:**
    ```
    http://localhost:8080/
    ```

7. **Заходите в браузер по указанному выше адресу и наслаждайтесь!**

## Немного о проекте

Проект реализован на стеке Java, HTML5, JavaScript, Spring Framework и PostgreSQL. База данных сохраняет IP пользователя при его переходе на сайт, а также каждый его запрос и ответ сервера. Перевод осуществляется через Yandex Translate API, которому в несколько потоков (до 10 одновременно) отправляются запросы, содержащие каждое слово введенного предложения. Также присутствует валидация введенных пользователем данных: если пользователь ошибся или не ввел какое-либо из полей, уведомление на странице сообщит ему об этом.
