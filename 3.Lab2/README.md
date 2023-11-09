# Лабораторная работа № 2. Параметры команды docker run. 

1. Узнать, какие номера портов выставлены в контейнер:

```
docker ps
```
![](img/1.png)

2. Узнать, какие номера портов выставлены на хосте:

```
docker ps
```
![](img/2.png)

3. Запустить контейнер с тегом с сопоставлением портов на хосте и контейнере:

```
docker run -p hostport:containerport containername:tag
```
![](img/3.png)
---
![](img/4.png)

4. Пересоздать контейнер с названием и необходимыми портами:

```
docker stop containername && docker rm containername && docker run --name=containername -d -p hostport:containerport -p hostport:containerport containername
```
 
![](img/5.png)

5. Узнать mac-address контейнера:

```
docker inspect containername | grep MacAddress
```
![](img/6.png)

6. Узнать внутренний IP контейнера:

```
docker inspect containername | grep IP
```
![](img/7.png)

7. Посмотреть логи контейнера:

```
docker logs containername
```
![](img/8.png)

