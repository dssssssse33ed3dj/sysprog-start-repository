# Ядро агента (C)

Ядро собирается в динамическую библиотеку: `sentry_core.dll` в Windows, `libsentry_core.dylib` в macOS,
`libsentry_core.so` в Linux. Первая функция появляется на паре 2.

| Файл | Что в нём |
|---|---|
| core.h | Заголовочный файл: структура core_info и объявление функции |
| core_info.c | Реализация функции core_get_info |
| show_info.c | Программа проверки функции ядра |
| sentry_core.dll | Собирается из core_info.c командой cl /LD |