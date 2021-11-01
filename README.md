# Тестовое задание в ЭР-Телеком
```
Задача:

Подготовить docker-compose проект в котором должны быть развернуты контейнеры

   1. Jbpmn
   2. Nginx
   3. Postgres
   4. Prom
   5. Grafana
   6. Node-exporter

Проверка правильности выполнения задания:

    Для выполненного задания все запросы поступают на 80 порт через Nginx контейнер (запросы проксируются в Jbpmn и Grafana на разные endpoint-ы). Остальные порты должны быть закрыты.
    Jbpmn настроен на работу с СУБД postgres
    Grafana настроена на работу с Prometheus. Внутри Grafana настроен dashboard для отображение метрик из Prometheus
    Prometheus забирает метрики с host машины (node-exporter)
```
### Запуск
Клонирую репозиторий, запускаем docker-compose.yml командой:
```
docker-compose up
```
### Endpoints
**Grafana:** `localhost/grafana/`

**Jbpmn:** `localhost/jbpmn/`

