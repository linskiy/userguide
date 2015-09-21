#Блокировки на подписку
Для того чтобы ваш сервис мог получить информацию о статусе подписки используется механизм блокировок. Предполагается, что перед входом в ваш сервис вы вызовете API биллинга, и если количество активных блокировок больше 0 то доступ к вашему сервису будет запрещен.

Вы также можете в это момент показать причины блокировок вашим пользователям. 

![Блокировки клиента](blocked-subs.png)

На каждую подписку может быть установлена одна или более блокировок.

##Работа с блокировками в правилах
Блокировка может быть создана в правилах биллинга  **автоматически** (при наступлении определенных условий). Например если подписку не удалость продлить из за недостатка средств на баллансе. Вданном примере создано правило, устанавливающее блокировку, если при создании подписки не хватает средств на ее активацию.
![Блокировки клиента](blokirovka-auto.png)
При поступленни средств эта блокировка должна быть снята 
![Блокировки клиента](blokirovka-auto-куьщму.png)

##Ручные блокировки
Блокировка пользователем pricePlan может быть создана **вручную**  Например если в вашем сервисе предусмотрена блокировка по просьбе клиента. Для создания ручной блокировки найдите клиента и откройте вкладку `подписки` и нажмите кнопку "Блокировать"

![Блокировки клиента](blokirovka-create1.png)
В открывшемся окне 
- выберите тип блокировки (любыет типы блокировки могут быть заданы в настройках системы).
- Введите комментарии (обязательное поле)
- Дата начата блокировки. Может быть в будущем (отложенная блокировка)
- Дата окончания блокировки. 
  - Если эта дата не задана то подписка будет блокирована до то как кто то ее не снимет. 
  - Если эта дата указана то сисиема отменит блокировку автоматически.


![Блокировки клиента](blokirovka-create2.png)

Созданная блокировка будет видна в разделе "Блокировки" клиента.
![Блокировки клиента](blokirovka-create3.png)
Снятие блокировки также может произведено как вручную так и автоматически (например при поступлении средств на баланс). В нашем случае:
- Блокировка №9 активна, но будет отменена системой автоматически 2015-07-04 в 15:35
- Блокировка №7 активна и никогда не будет отменена автоматически
- Блокировка №7 отменена 2015-06-26 в 14:54 пользователем №2