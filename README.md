# agapov97_microservices
agapov97 microservices repository

## ДЗ 12

Произошло знакомство с docker и docker-machine.

Был создан образ с приложением.

Образ был опубликован на dockerhub.


## ДЗ 13

В ходе выполнения ДЗ разбил существующее монолитное приложение на микросервисы.

Объединили микросервисы в одну сеть.

Ознакомился с базовыми принципами оптимизации размера изображений.

Создал volume для БД, чтобы после перезапуска контейнеров, данные сохранялись.

Для запуска контейнерова с другими сетевыми алиасами:

`docker run -d --network=reddit --network-alias=post_db_new --network-alias=comment_db_new mongo:latest
docker run -d --network=reddit --network-alias=post_new -e POST_DATABASE_HOST=post_db_new agapov97/post:1.0
docker run -d --network=reddit --network-alias=comment_new -e COMMENT_DATABASE_HOST=comment_db_new agapov97/comment:1.0
docker run -d --network=reddit -e POST_SERVICE_HOST=post_new -e COMMENT_SERVICE_HOST=comment_new -p 9292:9292 agapov97/ui:1.0`


## ДЗ 14

В ходе выполнения ДЗ познакомились с сетями в докере, с утилитой docker-compose.

Базовое имя проекта образуется из названия текущей директории. Поменять можно либо флагом --project-name/-p при запуске docker-compose, либо задав переменную окружения COMPOSE_PROJECT_NAME


## ДЗ 15

Подготовил инсталляцию Gitlab CI.

Подготовил репозиторий с кодом приложения.

Описал для приложения этапы пайплайна.

Задал ограничения для этапов.

Задал ручные этапы пайплайна.

Определил окружения.


## ДЗ 16

Ознакомился с инструментом для мониторинга Prometheus.

Поднял мониторинг для микросервисов и для ВМ.

Мой докерхаб с образами микросервисов и прометея.

https://hub.docker.com/u/agapov97


## ДЗ 17

Настроил мониторинг Docker контейнеров при помощи cAdvisor и Prometheus.

Настроил визуализацию метрик в Grafana.

Настроил сбор метрик работы приложения и бизнес метрик.

Настроил и проверил алертинг при недоступности одного из сервисов при помощи AlertManager.

Мой докерхаб:
https://hub.docker.com/u/agapov97


## ДЗ 18

Настроил логирование Docker контейнеров при помощи ElasticSearch и Fluentd.

Настроил визуализацию этого добра в Kibana.

Настроил парсинг плохо структурированных логов.

Поднял распределенный трейсинг с помощью Zipkin


## ДЗ 19

Настроил логирование Docker контейнеров при помощи ElasticSearch и Fluentd.

Настроил визуализацию этого добра в Kibana.

Настроил парсинг плохо структурированных логов.

Поднял распределенный трейсинг с помощью Zipkin


## ДЗ 20

В ходе выполнения ДЗ поднял кластер Kebernetes, следуя указаниям Kubernetes The Hard Way.

Разобраны основные компоненты Kubernetes.

Написаны базовые нерабочие деплойменты.


## ДЗ 21

В ходе выполнения ДЗ поднял кластер Kebernetes в Virtualbox посредством minikube, а затем внутри GKE.

Доработаны деплойменты, а также написаны конфиги для сервисов и нейспейса.


## ДЗ 22

В ходе выполнения ДЗ были изучены и настроены следующие компоненты Kubernetes:
Ingress Controller
 - Ingress
 - Secret
 - TLS
 - LoadBalancer Service
 - Network Policies
 - PersistentVolumes
 - PersistentVolumeClaims
