# Отчёт о тестировании приложения Money Transfer

## Краткое описание

В ходе тестирования функции пополнения счета VIP-клиента обнаружены ошибки в коде, приводящие к неверному итоговому значению баланса счета.

## Описание тестов

Проводилось позитивное функциональное тестирование функции пополнения счета.

## Результаты

1. 50/50% успешных/не успешных тестов
2. Баг-репорт: https://github.com/kristinavenevtseva/java-2-1/issues/1

## Общие рекомендации

Проведя тестирование функции пополнения счета на двузначных числах и получив верное итоговое значение, делаю вывод, что ошибки в коде нет и проблема в размере чисел. Необходимо заменить тип всех переменных (base, transit, total) на *long*, так как итоговое значение баланса счета выходит за пределы типа *int*.
