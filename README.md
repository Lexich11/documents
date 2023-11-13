# Имя хоста

## Назначение команды
Для указания или изменения имени хоста на сетевом сервере используйте команду `hostname` в глобальной конфигурации. Для восстановления конфигурации по умолчанию используйте команду `no hostname`.

## Синтаксис команды
```bash
hostname ИМЯ
no hostname
```

| Параметр | Описание параметра      | Значение параметра          |
|----------|------------------------|----------------------------|
| ИМЯ      | Новое имя хоста сервера | Строка (1-63 символа)       |

## Командный режим
Глобальная конфигурация

## По умолчанию
Имя хоста по умолчанию — Switch.

## Употребление
Имя хоста используется в приглашениях и именах файлов конфигурации по умолчанию. Имя должно соответствовать правилам ARPANET, содержащие только буквы, цифры, дефисы и подчеркивание. Имена должны состоять из 64 символов или меньше.

## Примеры
```bash
Switch# configure terminal
Switch(config)# hostname sandbox
sandbox(config)#
```

# IP-адрес управления

## Назначение команды
Используйте эту команду для задания IP-адреса управления на коммутаторе. Для удаления IP-адреса управления используйте форму `no` этой команды.

## Синтаксис команды
```bash
IP-адрес управления A.B.C.D/M
no IP-адреса управления
IPv6-адрес управления X:X::X:X/M
no управление IPv6-адресом
```

| Параметр        | Описание параметра                           | Значение параметра          |
|-----------------|---------------------------------------------|----------------------------|
| A.B.C.D/M       | IPv4-адрес управления с длиной маски 1-32   | IPv4-адрес с длиной маски 1-32 |
| X:X::X:X/M      | IPv6-адрес управления с длиной маски 1-128  | IPv6-адрес с длиной маски 1-128 |
| шлюз A.B.C.D    | Добавление шлюза IPv4                       | IPv4-адрес шлюза            |
| шлюз X:X::X:X   | Добавление шлюза IPv6                       | IPv6-адрес шлюза            |

## Командный режим
Глобальная конфигурация

## По умолчанию
Никакой

## Употребление
Никакой

## Примеры
```bash
Switch# configure terminal
Switch(config)# IP-адрес управления 192.168.100.100/24
Switch(config)# no IP-адреса управления
Switch(config)# управление ipv6 адресом 2001:1000::1000/96
Switch(config)# no управление ipv6 адресом
```

# Маршрут управления

## Назначение команды
Используйте эту команду для задания шлюза на коммутаторе для управления IP-адресом.

## Синтаксис команды
```bash
маршрут управления (add|del) шлюз A.B.C.D
управление маршрутом ipv6 (add|del) шлюз X:X::X:X
```

| Параметр  | Описание параметра | Значение параметра |
|-----------|--------------------|---------------------|
| add       | Добавление маршрута | -                   |
| del       | Удаление маршрута   | -                   |
| IPv6      | Настройка шлюза IPv6 | -                   |
| Шлюз      | Добавить шлюз       | A.B.C.D (IPv4) или X:X::X:X (IPv6) |

## Командный режим
Глобальная конфигурация

## По умолчанию
Никакой

## Употребление
Никакой

## Примеры
```bash
Switch# configure terminal
Switch(config)# маршрут управления add шлюз 192.168.100.254
Switch(config)# управление маршрутом ipv6 add шлюз 2001:1000::1
```

---
**Примечание:** 
В данном документе представлены команды и примеры настройки для управления и конфигурации сетевого сервера. Убедитесь, что вы имеете достаточные права доступа и знание конфигурации вашего оборудования перед применением этих команд.