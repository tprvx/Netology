# SUBD - Petr

### Задание 1

- электронные чеки в json-виде -> Документоориентрованная, так как не понятно какой набор данных будет в чеке
- склады и автомобильные дороги для логистической компании -> Графовая, будет удобно сроить маршруты
- генеалогические деревья -> Графовая, будет понятно кто откуда, удобно
- кэш идентификаторов клиентов с ограниченным временем жизни для движка аутенфикации -> Redis или Memcahed 
- отношения клиент-покупка для интернет-магазина ->  Реляционная, тут понятна структура и она не будет меняться скорее всего

### Задание 2

1) Согласно CAP-теореме это AP система. Так как система в случае сетевого разделения узлов продолжает отвечать пользователям на запросы, при этом не гарантируя консистентности данных.

2) Согласно PACELC-теореме это PA/EC система. При наличии сетевого разделения системы ставка делается на доступность, а при отсутствии распределения – на консистентность.

### Задание 3

Не могут, така как эти подходы противоречат друг другу. Base отдлает приоритет высокой производительности в ущерб согласованности, ACID - требует немедленной и постоянной согласованности, а это невозможно с сочетанием высокой производительности. Но возможен подход когда система согласуется через определенное время после пиковой нагрузки, но это не ACID подход всё рано. Поэтому они не могут вместе быть.

### Задание 4

Что это?

Поведенческий шаблон проектирования передачи сообщений, в котором отправители сообщений, именуемые издателями, напрямую не привязаны программным кодом отправки сообщений к подписчикам.

Какие минусы выбора этой системы?

- В Pub/Sub сообщения отправляются и никогда не сохраняются