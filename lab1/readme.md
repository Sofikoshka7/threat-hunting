# Лабораторная работа №1 Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  Ноутбук Lenovo
2.  Windows 11
3.  Visual Code

## План

1.  Ввод команд в эмулятор терминала
2.  Анализ данных

## Ход работы

1.  Получим сведения о версии ядра:

```
winver
```

![](https://github.com/Sofikoshka7/threat-hunting/edit/main/lab1/Screenshot_1.png)


В результате выполнения данной команды была получена версия ядра - 22Н2 (сборка ОС 22621.1702)

2.  Далее можно получить сведения о процессоре:

```
Get-WmiObject win32_Processor
```

![](https://github.com/Sofikoshka7/threat-hunting/edit/main/lab1/Screenshot_2.png)

```
WMIC CPU Get DeviceID,NumberOfCores NumberOfLogicalProcessors
```

![](https://github.com/Sofikoshka7/threat-hunting/edit/main/lab1/Screenshot_3.png)

Было определено, что используемый процессор - 4-х ядерный 8-ми поточный Intel(R) Core(TM) i5-8265U

3.  Также получим последние 30 строк логов системы:

```
Get-EventLog -LogName 'system' -Newest 30
```

![](https://github.com/Sofikoshka7/threat-hunting/edit/main/lab1/Screenshot_4.png)

## Оценка результата

В результате лабораторной работы мы получили основную информацию об ОС, процессоре и логи системы

## Вывод

Таким образом, мы научились работать с базовыми командами Windows, получать сведения о системе
