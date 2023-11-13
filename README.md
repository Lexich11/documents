# Имя хоста (hostname)

## Назначение команды
Для указания или изменения имени хоста на сетевом сервере используйте команду `hostname` в глобальной конфигурации. Для восстановления конфигурации по умолчанию используйте команду `no hostname`.

## Синтаксис команды
```bash
hostname NAME
no hostname
```

| Параметр | Описание параметра      | Значение параметра          |
|----------|------------------------|----------------------------|
| NAME(ИМЯ)      | Новое имя хоста сервера | Строка от 1 до 63 символов       |

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

# Управление IP-адресом (IP adress)

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
Отсутствует

## Использование
Отсутствует

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
Отсутствует

## Использование
Отсутствует

## Примеры
```bash
Switch# configure terminal
Switch(config)# маршрут управления add шлюз 192.168.100.254
Switch(config)# управление маршрутом ipv6 add шлюз 2001:1000::1
```

---

**Глоссарий**

1. **ARPANET**: Сеть передачи данных, предшествующая интернету, разработанная в 1969 году. В данном контексте, правила ARPANET используются для ограничения имен хостов.

2. **Глобальная конфигурация**: Режим настройки, в котором производятся изменения, касающиеся всего устройства.

3. **IPv4**: Четвёртая версия протокола интернета, используемая для идентификации и распределения сетевых узлов в сети.

4. **IPv6**: Шестая версия протокола интернета, предназначенная для замены IPv4, обеспечивает больше уникальных IP-адресов.

5. **Параметр**: Компонент команды, который указывает на конкретное действие или настройку.

6. **Сетевой сервер**: Устройство, обеспечивающее сетевые функции и обработку данных в сети.

7. **Сетевой узел**: Конечное устройство в сети, обладающее собственным IP-адресом.

8. **Шлюз**: Устройство, предоставляющее путь для обмена данными между сетями.

9. **Строка**: Символьная последовательность в контексте этой документации, представляющая имя хоста или адрес.

10. **Терминал**: Режим устройства, который позволяет пользователю взаимодействовать с устройством и вводить команды.

11. **Управление маршрутом**: Настройка шлюза для управления IP-адресом в сети.

12. **Управление IPv6-адресом**: Команда для настройки IPv6-адреса управления.

13. **Управление IPv4-адресом**: Команда для настройки IPv4-адреса управления.

14. **Устройство**: Физическое или виртуальное устройство, обеспечивающее сетевые функции, такие как коммутатор или маршрутизатор.

15. **Файл конфигурации**: Файл, содержащий настройки и конфигурации устройства.
