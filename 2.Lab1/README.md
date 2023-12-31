# Лабораторная работа № 1. Основные команды Docker. 

Узнать версию программы:

```
docker -v
```
![](img/1.png)

Узнать количество работающих контейнеров на хосте:

```
docker ps
```
![](img/2.png)

Узнать количество образов на хосте:

```
docker images
```
![](img/3.png)

Запустить контейнер из образа:

```
docker run redis
```
 
![](img/4.png)

Остановить только что созданный контейнер:

```
Ctrl+C
```
![](img/5.png)

Узнать, сколько контейнеров запущено на хосте:

```
docker ps
```
![](img/6.png)

Узнать сколько контейнеров всего на хосте, включая запущенные и остановленные:

```
docker ps -a
```
![](img/7.png)

Узнать, какой образ использован для запуска контейнера:

```
docker ps -a
```
![](img/8.png)

Узнать название контейнера, собранного из определенного образа:

```
docker ps -a
```

![](img/9.png)

Узнать ID контейнера, собранного из определенного образа:

```
docker ps -a
```
![](img/10.png)

Узнать состояние остановленного контейнера:

```
docker ps -a
```
![](img/11.png)

Удалить все контейнеры с хоста:

```
docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q)
```
![](img/12.png)

Удалить определенный образ:

```
docker rmi ubuntu
```
![](img/13.png)

Скачать определенный образ без его запуска:

```
docker pull nginx:1.14-alpine
```
![](img/14.png)

Запустить контейнер с определеного образа и присвоить ему название:

```
docker run --name webapp nginx:1.14-alpine
```
![](img/15.png)

Удалить все образы на хосте (для этого нужно остановить все контейнеры и удалить их):

```
docker stop $(docker ps -a -q) && docker rm $(docker ps -a -q) && docker rmi $(docker images -a -q)
```
![](img/16.png)
		
