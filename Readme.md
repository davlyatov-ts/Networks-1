1.Работа c HTTP через телнет.<br>
Подключитесь утилитой телнет к сайту stackoverflow.com **telnet stackoverflow.com 80**<br>
отправьте HTTP запрос<br>
```
	GET /questions HTTP/1.0
	HOST: stackoverflow.com
	[press enter]
	[press enter]
```
В ответе укажите полученный HTTP код, что он означает?<br>

-	Ответ<br>
![telnet stackoverflow.com 80](https://github.com/davlyatov-ts/Networks-1/blob/master/telnet.png)
Ответ **HTTP/1.1 301 Moved Permanently**. Запращиваемый ресурс был redirect на
```
https://stackoverflow.com/questions<br>
```
___
2.Повторите задание 1 в браузере, используя консоль разработчика F12.<br>
