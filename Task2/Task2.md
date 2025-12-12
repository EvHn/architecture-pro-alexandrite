# Выбор и настройка мониторинга в системе

## Мотивация

Настройка мониторинга всех частей приложения важна, по следующим причинам:
1) В MES столкнулись с проблемами производительности и чтобы лучше понять по какой причине возникла проблема и найти её
   источник необходимо собрать метрики.
2) При эксплуатации проложения неизбежно возникают проблема, поэтому для оперативного их выявления необходимы метрики,
   которые позволят быстро обнаружить возникшую проблему.
3) Для бизнеса важно отслеживать какая функциональность пользуется популярностью, а какая нет, понимать как новый
   функционал влияет на поведение пользователей. Сбор метрик помогает принимать взвешенные решения при развитии бизнеса.

## Выбор подхода к мониторингу

### Онлайн-магазин
Метод Четырех золотых сигналов:
* Response time (latency) for shop API - Задержка 
* Number of requests (RPS) for internet shop API - Траффик
* Number of HTTP 200 for shop API - Ошибки 
* Number of HTTP 500 for shop API - Ошибки
* Memory Utilisation for shop API - Насыщенность 

### БД онлайн-магазина
* Number of connections for shop db instance
* Memory Utilisation for shop db instance
* Size of shop db instance

### 3D files storage
* Kb provided (sent) for shop API
* Size of S3 storage

### БД MES
* Number of connections for MES db instance
* Memory Utilisation for MES db instance
* Size of MES db instance

### MES
Метод USE для отслеживания проблем с производительностью:
* Memory Utilisation for MES API - Утилизация
* CPU % for MES API - Утилизация
* Number of message in flight in RabbitMQ - Насыщенность
* Number of requests (RPS) for MES API - Насыщенность
* Number of dead-letter-exchange letters in RabbitMQ - Ошибки
* Number of HTTP 500 for MES API - Ошибки

### CRM
Метод Четырех золотых сигналов:
* Response time (latency) for CRM API - Задержка
* Number of requests (RPS) for CRM API - Траффик
* Number of HTTP 200 for CRM API - Ошибки
* Number of HTTP 500 for CRM API - Ошибки
* Memory Utilisation for CRM API - Насыщенность
