# Домашнее задание к занятию "`Репликация и масштабирование. Часть 1`" - `Никулин Михаил Сергеевич`



---

### Задание 1

`Репликация Master-slave`

`Master - основной сервер, на котором происходит обработка данных (добавление, обновление, удаление)`

`Slave - выступает как вспомогательный сервер БД, который копирует все данные с мастера. С данного сервера происходит 
чтение данных. Возможно наличие нескольких таких серверов.`

`Преимущества:`
* `проще настройка`
* `подчиненные устройства могут быть подключены и отключены к ведущему устройству без простоев`
* `для анализа данных можно использовать подчиненные устройства, что не повлияет на основное`

`Недостатки:`
* `в случае сбоя мастера необходимо переводить slave в master, что требует времени и может привести к потере данных`
* `чем больше вторичных серверов, тем больше нагрузка на основной, т.к. требуется передача данных или изменений на каждый сервер`


`Репликация Master-master`

`Репликация типа Мастер-Мастер для баз данных увеличивает скорость доступа к данным и повышает избыточность для действующих сайтов. 
Использование репликации хотя бы двух серверов MySQL которые будут работать как кластер очень полезно для сайтов с требованиями high-availability. 
Это настройка обычной Master-Slave репликации, только в обе стороны. Конфигурация повышиет эффективность при обращении к данным, т.к. чтение и запись могут 
происходить на обеих серверах и распределять нагрузку между собой. При сбое одного из серверов происходит автоматическое 
переключение на второй, без потерь времени и данных`

`При этом главной проблемой данной конфигурации является сложность в настройке, т.к. неоходимо решать вопросы цикличности 
копирования данных между серверами`


---

### Задание 2

`master - 192.168.0.28`

`slave - 192.168.0.17`

![task_2_1.png](img%2Ftask_2_1.png)
![task_2_2.png](img%2Ftask_2_2.png)
![task_2_3.png](img%2Ftask_2_3.png)
![task_2_4.png](img%2Ftask_2_4.png)


---

## Дополнительные задания (со звездочкой*)


### Задание 3*

`master - 192.168.0.28`

`master - 192.168.0.17`


![task_3_1.png](img%2Ftask_3_1.png)
![task_3_2.png](img%2Ftask_3_2.png)
![task_3_3.png](img%2Ftask_3_3.png)
![task_3_4.png](img%2Ftask_3_4.png)
