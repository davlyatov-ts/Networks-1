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

___
3.Какой IP адрес у вас в интернете?<br>
```
dig +short myip.opendns.com @resolver1.opendns.com
94.29.8.191
выводе видно мой внешний адрес
```
___
4.Какому провайдеру принадлежит ваш IP адрес? Какой автономной системе AS? Воспользуйтесь утилитой ***whois***<br>
![my ip](https://github.com/davlyatov-ts/Networks-1/blob/master/my%20ip.png)
___
5.Через какие сети проходит пакет, отправленный с вашего компьютера на адрес 8.8.8.8? Через какие AS?<br>
Воспользуйтесь утилитой traceroute<br>
![traceroute](https://github.com/davlyatov-ts/Networks-1/blob/master/traceroute.png)
___
6.Повторите задание 5 в утилите mtr. На каком участке наибольшая задержка - delay?
![mtr](https://github.com/davlyatov-ts/Networks-1/blob/master/mtr.png)
___
7.Какие DNS сервера отвечают за доменное имя dns.google? Какие A записи? воспользуйтесь утилитой dig<br>

***pi@ca:~$ dig +short NS dns.google***<br>
```
ns2.zdns.google.
ns4.zdns.google.
ns1.zdns.google.
ns3.zdns.google.
```
