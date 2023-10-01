# Описание

Этот код представляет собой набор функций для работы с данными из JSON-файла, представляющего список операций. Он включает функции для чтения данных из файла, сортировки операций по дате и вывода информации о транзакциях. Код разработан на языке Python и может быть полезен для анализа и визуализации операций.

# Использование

Для использования этого кода, следуйте инструкциям ниже:

1. **Установка зависимостей**: Убедитесь, что у вас установлен Python, и вам необходим модуль `json`. Если он не установлен, вы можете установить его с помощью следующей команды:
    ```
    pip install json
    ```
2. **Подготовка данных**: Поместите файл с данными операций (например, `operations.json`) в ту же директорию, где находится данный код.
3. **Запуск кода**: Запустите код, указав путь к вашему JSON-файлу:
    ```python
    URL = "operations.json"
    get_data_transactions(get_last_operations(read_from_json(URL)))
    ```
    Этот код загрузит данные из JSON-файла, отсортирует операции по дате и выведет информацию о последних пяти операциях.

# Функции

Данный код включает в себя следующие функции:

- `read_from_json(path)`: Загружает данные из JSON файла. Принимает путь к JSON файлу в качестве аргумента и возвращает загруженные данные или строку "Файл не найден", если файл не существует.
- `get_last_operations(operations)`: Сортирует список операций по дате и возвращает последние пять операций. Принимает список операций для сортировки и фильтрации.
- `get_data_transactions(operations)`: Выводит информацию о транзакциях из списка операций. Принимает список операций для печати информации о транзакциях.

# Пример вывода

Пример вывода кода может выглядеть следующим образом:
```
2023-09-18 12:30:45 Покупка товара
Иванов И.И. -> Магазин "Пример"
1000.00 RUB

2023-09-17 09:15:20 Перевод средств
Счет пользователя А -> Счет пользователя B
500.00 USD
```