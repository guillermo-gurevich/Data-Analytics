# Desafío Espectáculos - DATATON 2022
## Messi10 by Cirque du Soleil

### Introducción
En el contexto de los espectáculos, la curva de ventas puede ser muy diferente y depender
de varios factores, tanto internos como externos. En este caso les presentamos el dataset de
las ventas hasta el día de la fecha de un evento en particular.

### Detalles del evento
El evento detallado consiste en varios shows (o funciones), y además una experiencia
interactiva previa a cada una de ellas.
Los usuarios tienen la posibilidad de comprar un ticket para el show y otro ticket para la
experiencia (para el mismo día del show) en un horario determinado. Solo los que compraron
ticket para el show están habilitados para comprar tickets para la experiencia previa. Los
tickets son individuales en ambos casos, es decir, si un usuario compra 5 tickets para el show
y 4 de ellos desean participar de la experiencia previa, deberá comprar además 4 tickets para
esta última.
El estadio está dividido en 2 tribunas las cuales se dividen en varios sectores. El precio varía
según la posición relativa al escenario. Además, a lo largo de la venta se ofrecieron distintas
promociones para la compra de tickets.
Por último, se entrega otro dataset con ejemplos de ventas de otros shows y su respectiva
capacidad. Tener en cuenta que estos ejemplos son de shows distintos

### Consignas
El desafío abarca tres consignas, que los participantes deben responder tomando el rol de
consultores externos contratados por la empresa.

1. Definir KPI’s de interés para el rubro, que permita entender la performance en la venta
del espectáculo.
2. Crear un dashboard de control que permita evaluar el comportamiento de las ventas y
ayudar en la toma de decisiones.
3. Encontrar uno o más insights en los datos que pueda tener relevancia para futuras
decisiones en otros eventos.


### Detalle de orders.csv

|Atributo|Descripción|Tipo|
| -- | -- | -- |
|order_id|id de la orden de compra|string|
|order_date |fecha de la orden de compra |date|
|order_hour |orden de la hora de compra |time|
|status |indica si las tickets se entregaron o deben entregarse |string|
|event |nombre del evento |string|
|show_date |fecha del show |date|
|show_hour |hora del show |time|
|tickets_quantity |cantidad de tickets en la orden y sector |integer|
|ticket_type |indica si el usuario compró sector del estadio, parking o experiencia previa|string
|tribune |indica la tribuna del estadio |string|
|previuos_experience_hour |hora de la experiencia previa, en el caso que haya comprado|time|
|price_type |indica si compro precio regular o con promoción |string|
|order_amount |monto de la orden |numeric|
|payment_method |indica el método de pago de la orden |string|
|client_id |id del cliente |string|
|city [^1]|ciudad donde habita el cliente |string|
|region |región en la que habita el cliente |string|
|country |país en el que habita el cliente |string|

[^1]: este campo se llena de forma manual a la hora de realizar el pago


### Detalle de show_capacity.csv

|Atributo |Descripción |Tipo|
| -- | -- | -- |
|show_date |fecha del show |date|
|show_hour |hora del show |time|
|ticket_type|indica sector, experiencia previa o estacionamiento|string|
|capacity |capacidad máxima correspondiente |integer|


### Detalle de other_show_sales.csv

|Atributo |Descripción |Tipo|
| -- | -- | -- |
|event |nombre del evento |string|
|first_week_tickets_quantity|cantidad de tickets vendidos en la primera semana de venta|integer|
|second_week_tickets_quantity|cantidad de tickets vendidos en la segunda semana de venta|integer|
|middle_weeks_tickets_quantity |cantidad de tickets vendidos durante las semanas intermedias|integer|
|two_weeks_before_tickets_quantity |cantidad de tickets vendidos en la anteúltima semana de venta|integer|
|last_week_tickets_quantity |cantidad de tickets vendidos en la última semana de venta|integer|
|total_tickets_quantity |cantidad total de tickets vendidos |integer|
|venue_capacity |capacidad del estadio |integer|
|middle_weeks_quantity |cantidad de semanas intermedias de venta |integer|
|shows_quantity |cantidad de shows (o funciones) del evento |integer|
|sold_out_flag |indica si el show se agoto o no |boolean|

