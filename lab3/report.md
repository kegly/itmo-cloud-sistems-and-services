# Лабораторная работа №3

### Задание

Поднять kubernetes кластер локально (например minikube), в нём развернуть свой сервис, используя 2-3 ресурса kubernetes. В идеале разворачивать кодом из yaml файлов одной командой запуска. Показать работоспособность сервиса.
(сервис любой из своих не опенсорсных, вывод “hello world” в браузер тоже подойдёт)



### Ход работы
#### 1. Поднятие кластера - minikube start

![image](https://github.com/kegly/itmo-cloud-systems-and-services/blob/main/lab3/images/Screenshot%20from%202024-10-15%2004-45-56.png)


#### 2. Загрузка образа приложения в minikube

![image](https://github.com/kegly/itmo-cloud-systems-and-services/blob/main/lab3/images/photo_2024-10-15_04-49-14.jpg)

#### 3. Создание Deployment
Необходимо указать  imagePullPolicy: Never чтобы образ брался локально из minikube

![image](https://github.com/kegly/itmo-cloud-systems-and-services/blob/main/lab3/images/Screenshot%20from%202024-10-15%2004-50-54.png)

#### 4. Создание Service
Сопостовление внутреннему порту приложения (80) внешнего порта назначаемого рандомно
![image](https://github.com/kegly/itmo-cloud-systems-and-services/blob/main/lab3/images/Screenshot%20from%202024-10-15%2004-54-13.png)

#### 5. Тестирование доступности
Приложение доступно по http://<minikube_ip>:<external_port>

![image](https://github.com/kegly/itmo-cloud-systems-and-services/blob/main/lab3/images/Screenshot%20from%202024-10-15%2005-01-27.png)
