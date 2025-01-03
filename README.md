### Описание работы
В рамках задания было изучено и протестировано использование YouTube Data API для получения информации о видеороликах. API предоставляет широкий функционал для работы с данными, такими как метаданные видео, статистика просмотров, рейтинги и другая информация. Были выполнены несколько экспериментов с использованием запросов через Python и curl.

### **Пример 1: Получение базовой информации о видео**
Цель: Получить метаданные видео, включая название, описание, дату публикации, статистику просмотров, лайков и комментариев.

Запрос:

Метод: !curl -X GET 
URL: https://www.googleapis.com/youtube/v3/videos?part=snippet,contentDetails,statistics&id=rDjuyN-T1n8&key=AIzaSyCNXxCjOTRgS3kaLwbqsFg12Hedb34MY1c
Параметры:
part=snippet,contentDetails,statistics — указывает, какие части данных нужно получить.
id={VIDEO_ID} — уникальный идентификатор видео.
key={API_KEY} — API-ключ для аутентификации.
Результат:

Успешно получена информация:
Название видео.
Описание и дата публикации.
Статистика: количество просмотров, лайков, комментариев.
Длительность видео (в формате ISO 8601).
**Пример данных:**

Название: "ИСТОРИЯ СУКУНЫ И УРАЮМЕ".
Просмотры: 12,473.
Лайки: 589.
Длительность: 12 минут 4 секунды.

### **Пример 2: Фильтрация данных по нескольким видео**
Цель: Получить информацию сразу о нескольких видео для сравнения статистики.

Запрос:

Метод: !curl -X GET 
URL: https://www.googleapis.com/youtube/v3/videos?part=snippet,contentDetails,statistics&id=MjDU9Go6YbQ,{VIDEO_ID2}&key=AIzaSyCNXxCjOTRgS3kaLwbqsFg12Hedb34MY1c
Результат:

**Были получены данные для двух видео:**
Видео: "ИСТОРИЯ СУКУНЫ И УРАЮМЕ".
Просмотры: 12,473.
Лайки: 589.
Видео: "СОБОЛЕВ vs МАРКАРЯН: Детальный разбор дебатов".
Просмотры: 14,437.
Лайки: 1,240.
Вывод: Сравнение метрик показало, что второе видео имеет более высокий уровень вовлеченности аудитории.

### **Пример 3: Анализ видео по категориям**
Цель: Получить данные о популярности видео в конкретных категориях (например, "Игры", "Развлечения").

Запрос:

Метод:
URL: https://www.googleapis.com/youtube/v3/videos?part=snippet,contentDetails,statistics&id=h2MGC7gD9uM&key=AIzaSyCNXxCjOTRgS3kaLwbqsFg12Hedb34MY1c

Результат для видео в категории "Игры":
Название: "САМАЯ ХУДШАЯ РОЛЬ В ДОТЕ".
Просмотры: 123,175.
Лайки: 5,346.
Комментарии: 573.
Вывод: Видео в категории "Игры" имеет высокий уровень вовлеченности, что подтверждается большим количеством комментариев.

### **Выводы**

**Изучение работы с YouTube Data API:**

В процессе работы был исследован и применен API для получения информации о видео. API показал себя как мощный инструмент для извлечения метаданных (название, описание, дата публикации) и статистики (просмотры, лайки, комментарии) видеороликов.
Практическая реализация:

**Было успешно выполнено несколько запросов для анализа конкретных видео. Получены данные, которые могут быть использованы для анализа популярности контента, вовлеченности аудитории и сравнения видео между собой.**
Протестированы два подхода к работе с API:
С помощью библиотеки requests на Python, что дает возможность легко обрабатывать данные и интегрировать их в проекты.
С помощью curl, что удобно для тестирования запросов.
Полученные результаты:

**Получена информация о видео, включая просмотры, лайки, длительность и ключевые теги.**
Данные могут быть использованы для анализа вовлеченности аудитории, изучения трендов и выявления популярных категорий контента.
Потенциал применения:
