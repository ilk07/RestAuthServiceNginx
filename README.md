# Разворачивание Spring Boot приложений
## Прокси на NGINX. REST-сервис авторизации 

![Сервис авторизации](https://tehnikaarenda.ru/wp-content/uploads/8/3/7/8379fe4514f0786d302083044eb294a9.jpeg "Сервис авторизации")

Сервис авторизации пользователей по логину и паролю с обратным прокси на Nginx

## Настройка
1. Установить Nginx 
2. Перенести или скопировать в папку "html" файл "signin.html" из папки "src/main/resources/"
3. Сделать настройки конфигурации Nginx как указано в файле "nginx.conf" папки "src/main/resources/"
4. Запустить NGINX
5. Запустить Java приложение

## Как работает
При обращении по адресу http://localhost/signin NGINX вернет форму ввода логина и пароля из файла signin.html.  
После отправки данных формы, NGINX проксирует запрос на порт 8080 и пользователю вернется ответ Java-приложения
