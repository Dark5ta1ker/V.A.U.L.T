Находится на [[Физический уровень|физическом]] и [[Канальный уровень|канальном]] уровне модели OSI.
На канальном уровне использует два формата кадров
- Ethernet II - фирменный стандарт Ethernet, созданный Intel, DEC и Xerox. 
- IEEE 802.3 - юридический стандарт.
Ethernet II используется чаще. однако современное оборудование поддерживает оба стандарта. 

Кадр Ethernet выглядит так:

| <center>6 байт</center>           | <center>6 байт</center>            | <center>      2         байта         </center> | <center>46-1500 байт</center> | <center>4 байта</center>           |
| --------------------------------- | ---------------------------------- | ----------------------------------------------- | ----------------------------- | ---------------------------------- |
| <center>Адрес получателя</center> | <center>Адрес отправителя</center> | <center>Тип</center>                            | <center>Данные</center>       | <center>Контрольная сумма</center> |
|                                   |                                    | 0800 - IPv4<br>86DD - IPv6<br>0806 - ARP        | JumboFrame - до 9000 байт     |                                    |
