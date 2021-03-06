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
-	откройте вкладку **Network**
-	отправьте запрос http://stackoverflow.com
-	найдите первый ответ HTTP сервера, откройте вкладку **Headers**
-	укажите в ответе полученный HTTP код.
-	проверьте время загрузки страницы, какой запрос обрабатывался дольше всего?
-	приложите скриншот консоли браузера в ответ.<br>
![](https://github.com/davlyatov-ts/Networks-1/blob/master/red.png)
В ответ получили код 307 (Temporary Redirect)<br>
![](https://github.com/davlyatov-ts/Networks-1/blob/master/11.png)
![](https://github.com/davlyatov-ts/Networks-1/blob/master/22.png)

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
___
8.Проверьте PTR записи для IP адресов из задания 7. Какое доменное имя привязано к IP? воспользуйтесь утилитой dig<br>
***dig -x 8.8.8.8 +noall +answer***<br>
```
8.8.8.8.in-addr.arpa.   6333    IN      PTR     dns.google.
```
___
