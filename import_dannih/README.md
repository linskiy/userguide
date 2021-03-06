# Импорт данных

PricePlan поддерживает пакетную загрузку клиентов и подписок из других систем. Пакетная загрузка данных обычно является одной последних операции перед запуском системы в работу.

## Перед загрузкой клиентов необходимо:

1. создать в PricePlan все поля для импортируемых данных
2. подготовить файл загрузки в формате CSV

## Перед загрузкой подписок необходимо:

1. создать в PricePlan все поля для импортируемых данных
2. создать в PricePlan клиентов, к которым относятся загружаемые подписки
3. создать в PricePlan продукты, к которым относятся загружаемые подписки
4. подготовить файл загрузки в формате CSV

Загрузку данных можно тестировать в режиме песочницы, не превышая ограничение 50 лицевых счетов.

Загрузку полного списка клиентов, следует производить сразу после перехода в боевой режим.

Примечания:

> 1. При импорте данных не происходит триггера событий "клиент:создание" и "подписка:создание". Соответственно, не будут выполняться правила, созданные для этих событий.
> 2. При импорте данных "новые клиенты", существующие в системе клиенты, не пропадут и их данные не изменятся.

