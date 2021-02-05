В наше время много open source  проектов зависят от node. Поэтому нам задают много вопросов о том «Как установить node.js?».Что же нам делать если мы хотим разработать и протестировать node приложение на нашем компьютере c Windows, прежде чем залить его на сервер?
На официальном сайте есть инсталляторы для Windows и Mac OS, так же есть бинарники для Linux пользователей. Мы опишем установку на Windows, но общий процесс одинаков для других ОС.
[Node.js](https://nodejs.org/en/download/)
Выберите установщик который вы хотите скачать и установить. Мы будем использовать 64-bit Windows Installer. Вам следует использовать пакет исходя от вашей конфигурации.
![Страница загрузки](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_1.png)
После загрузки файла, кликаем по нему и запускаем мастер установки.
![Setup](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_2.png)
Проходим по шагам  и ждем пока мастер завершит установку.
![Setup2](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_3.png)

После установки node.js платформы, следующий шаг который следует сделать, это запустить node приложение с вашего компьютера. Мы создадим простое приложение для демонстрации.

Создайте папку для вашего приложения. Я создал папку project на диске C:/ внутри которой создал еще каталог myapp.
![project](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_5.png)
Внутри каталога myapp создайте файл hello.js и напишите в нем следующий код:
var http = require('http');

http.createServer(function (request, response) {
  response.writeHead(200, {'Content-Type': 'text/plain'});
  response.end('Hello World\n');
}).listen(3000);

console.log('Server running at http://localhost:3000/');

Представленный выше код слегка модифицированная версия кода с официального сайта node, который создает HTTP web server на вашем компьютере.

Теперь мы готовы запустить наше первое Node.js приложение.

Откройте Node.js командную строку она находится в меню Пуск Windows, или воспользуйтесь поиском.
![command](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_6.png)
Командная строка node использует интерфейс (CLI). С помощью командной строки войдите в каталог myapp

cd C:\project\myapp

Далее давайте запустим файл hello.js. Пишем команду

node hello.js
Если все прошло отлично, вы увидите следующее сообщение в командной строке.
![hello](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_7.png)
В своем любимом браузере введите URl:
http://localhost:3000/
Вы должны увидеть сообщение Hello word в окне браузера, которое означает что все работает отлично.
![localhost](http://webupblog.ru/wp-content/uploads/2015/06/Screenshot_8.png)