# 10.5 Балансировка нагрузки. HAProxy/Nginx - НиконоровДА FOPS-6

## Задание 1

*Что такое балансировка нагрузки и зачем она нужна?*

*Приведите ответ в свободной форме.*

**Балансировка нагрузки - это процесс распределения нагрузки на кластер  серверов, она нужна для улучшения отказоустойчивости и упрощения масштабируемости**

## Задание 2

*Чем отличаются алгоритмы балансировки Round Robin и Weighted Round Robin?  В каких случаях каждый из них лучше применять?*

*Приведите ответ в свободной форме.*

**Алгоритмом Weighted round robin можно указать какое количество трафика отправлять на определенный сервер,  так можно лучше сбалансировать нагрузку**

## Задание 3

*Установите и запустите Haproxy.*

*Приведите скриншот systemctl status haproxy, где будет видно, что Haproxy запущен.*

![alt text](https://github.com/mxssclxck/hw-10.5/blob/main/img/1.png)

## Задание 4

*Установите и запустите Nginx.*

*Приведите скриншот systemctl status nginx, где будет видно, что Nginx запущен.*

![alt text](https://github.com/mxssclxck/hw-10.5/blob/main/img/2.png)

## Задание 5

*Настройте Nginx на виртуальной машине таким образом, чтобы при запросе:*

*curl http://localhost:8088/ping*

*он возвращал в ответе строчку:*

*"nginx is configured correctly".*

*Приведите конфигурации настроенного Nginx сервиса и скриншот результата выполнения команды curl http://localhost:8088/ping.*

![alt text](https://github.com/mxssclxck/hw-10.5/blob/main/img/3.png)

![alt text](https://github.com/mxssclxck/hw-10.5/blob/main/img/4.png)

## Задание 6

*Настройте Haproxy таким образом, чтобы при ответе на запрос:*

*curl http://localhost:8080/*

*он проксировал его в Nginx на порту 8088, который был настроен в задании 5 и возвращал от него ответ:*

*"nginx is configured correctly".*

*Приведите конфигурации настроенного Haproxy и скриншоты результата выполнения команды curl http://localhost:8080/.*

![alt text](https://github.com/mxssclxck/hw-10.5/blob/main/img/5.png)

![alt text](https://github.com/mxssclxck/hw-10.5/blob/main/img/6.png)
