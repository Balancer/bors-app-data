---
Date: 2016-12-27 21:14:23 +0300
Author: Balancer <balancer@balancer.ru>
---

# Начало процесса вынесения логгирования доступа в отдельные пакеты

Продолжается рефакторинг. Теперь начат выноса громоздкого кода
`bors_access_log` в отдельный пакет — `balancer/bors-log-access-mysql`.
Также заведён более производительный пакет логгирования
`balancer/bors-log-access-redis`. После окончания переноса подключение
нужного пакета будет происходить полностью автоматически:

```bash
composer require balancer/bors-log-access-redis
```
