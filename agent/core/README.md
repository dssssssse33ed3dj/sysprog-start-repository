# Ядро агента (C)

Ядро собирается в динамическую библиотеку: `sentry_core.dll` в Windows, `libsentry_core.dylib` в macOS, `libsentry_core.so` в Linux. Первая функция появляется на паре 2.

Сборка библиотеки (Windows): `cl /nologo /W4 /LD core_info.c core_procs.c core_spawn.c /Fe:sentry_core.dll`

| Файл | Что в нём |
|---|---|
| core.h | Заголовочный файл: структуры и объявления функций |
| core_info.c | Реализация функции `core_get_info` (сведения о системе) |
| core_procs.c | Реализация функции `core_list_procs` (список процессов) |
| core_spawn.c | Реализация функций `core_spawn` (запуск) и `core_wait` (ожидание) |
| list_procs.c | Программа проверки списка процессов на C |
| run_child.c | Программа проверки запуска и ожидания на C |