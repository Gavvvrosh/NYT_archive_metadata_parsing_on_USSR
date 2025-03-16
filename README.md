# NYT_archive_metadata_parsing_on_USSR
Пример использования бибилотеки pynytimes (подробное описание бибилиотеки [здесь](https://github.com/michadenheijer/pynytimes/tree/0.8.0))  для сбора метаданных публикаций The New-York Times за 1941 - 1945 гг., в которых упоминается СССР.
## Методология поиска публикаций
Было выделено **7 ключевых слов** для поиска статей: "_USSR_", "_Russia_", "_Russian_", "_Soviet_", "_Russians_", "_Stalin_", "_Moscow_". 

Во избежании суточных лимитов на кол-во запросов через api скрипт сбора метаданых запускался ежедневно со сдвигом дат окна поиска. 

Экспериментальным путем было выработано правило: дельта окна дат **delta = 29** дней, максимальное количество статей по одному ключевому слову для шага цикла **result = 400**.

## Содержимое репозитория
### Используемые скрипты:
основной скрипт сбора метаданных - [7_key_words_for_ussr.ipynb](https://github.com/Gavvvrosh/NYT_archive_metadata_parsing_on_USSR/blob/main/7_key_words_for_ussr.ipynb); 

скрипт для "разворачивания" поля keywords (исходный формат dictionary) в строки - [flattering_the_keywords_column.ipynb](https://github.com/Gavvvrosh/NYT_archive_metadata_parsing_on_USSR/blob/main/flattering_the_keywords_column.ipynb);

скрипт для объединения двух таблиц в итоговую - [Merging main_table with key_values.ipynb](https://github.com/Gavvvrosh/NYT_archive_metadata_parsing_on_USSR/blob/main/Merging%20main_table%20with%20key_values.ipynb).

### Полученные данные
Итоговая таблица - [merged_table_with_key_values.xlsx](https://github.com/Gavvvrosh/NYT_archive_metadata_parsing_on_USSR/blob/main/merged_table_with_key_values.xlsx).
