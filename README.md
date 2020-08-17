# opc2redis
OPC client &amp; required components

opccli2redis.exe шлюз для создания дуплексного канала обмена данными между сервером ОРС и Redis.

opccli2redis.ini

[general]

//progid сервера ОРС

opc_server_name=easyopc.da2.1

// имя исполняемого файла, которого надо дождаться в памяти для подключения

opc_server_exe=easyopc

// айпишник Redis
redis_ip = 127.0.0.1
redis_port = 6379

// флаг передачи значения ключа редиса в виде json объекта

to_redis_as_json=0

[opc_source]

// источник тэгов орс-сервер

// слева - имя в орс-сервере

// справа - имя в редисе

x1_1=x1_1


[redis_source]

// источник тэгов редис

// слева - имя в редисе

// справа - имя в орс-сервере

x1_1=x1_124

OPC Core Components Redistributable (x86) 105.1.zip - системные библиотеки поддержки технологии ОРС. Требует Microsoft .NET Framework 2.0.

OPCExplorer.exe тестовый клиент ОРС.

Первоначальная установка:
1. Поместить файлы 
OPC Core Components Redistributable (x86) 105.1.zip, 
opccli2redis.exe, 
opccli2redis.ini, 
OPCExplorer.exe, 
README.md
в папку "c:\OPC2REDIS\" или выбранную пользователем.
2. Выполнить установку OPC Core Components из архива, с правами администратора.
3. Проверить подключение к нужному орс-серверу в OPCExplorer.
4. Заменить opccli2redis.ini на "боевой", с корректными адресами и именами сервера и тэгов.
5. Добавить opccli2redis.exe в автозагрузку, например планировщиком задач.
6. Запустить opccli2redis.exe.

Шлюз управляется через меню в трее.

