# Приложение для подсчёта труб в пачках с использованием компьютерного зрения (надо придумать название)

## Содержание
- [Описание проекта](#описание-проекта)
- [Цель](#цель)
- [Функциональные возможности](#функциональные-возможности)
- [Тренировочные данные](#тренировочные-данные)
- [Структура тестового набора](#структура-тестового-набора)
- [Требования к результатам](#требования-к-результатам)
- [Стек технологий](#стек-технологий)

## Описание проекта
В производстве необходим быстрый и точный способ пересчёта продукции в пачках. Существующий метод наполнения карманов агрегатов не позволяет производить подсчёт продукции, что ведёт к отсутствию точной информации о количестве штанг, прутков и других изделий в пачке готового проката. Это может стать причиной претензий со стороны клиентов.

## Цель
Разработать мобильное приложение с функцией автоматического подсчёта, которое позволит избежать высокой стоимости существующих решений. В основе приложения будет лежать модель компьютерного зрения, которая сможет по изображению пачки труб круглого сечения, снятой с торца, определить количество труб и создать маски сегментации для каждой из них.

## Функциональные возможности
Автоматический подсчёт труб: Приложение принимает фотографии, снятые на смартфон, и выдает количество труб в пачке.
Сегментация изображений: Создание масок или контуров для каждой трубы.
Работа офлайн: Приложение должно работать без подключения к интернету.
Выбор области подсчёта: Возможность выбрать область на изображении, где нужно произвести подсчёт.
Поддержка одного типа объектов: На первом этапе поддерживается только один вид профиля — круглый.
Данные и тестирование
Тестовые данные
Открытый тест: Доступен участникам и содержит фотографии, похожие на те, что есть в архиве.
Закрытый тест: Включает более разнообразные фотографии с других производств и недоступен участникам.
Тестовые данные выбраны таким образом, чтобы на изображении была четко видна область с одной пачкой труб.

## Тренировочные данные
Тренировочный набор может содержать несколько пачек труб разного профиля. Участники могут нарезать фотографии по своему усмотрению.

## Структура тестового набора
Фотографии одного класса труб (0 — круглые трубы)
Файл labels.csv: Содержит метаданные фотографий
Путь к фотографиям и сегментационной разметке
Класс определяемого профиля: На первом этапе только один класс — 0 (круглые трубы)
Количество труб в пачке

## Требования к результатам
- submission.csv: Файл с результатами подсчёта труб для тестовых изображений.
- Маски изображений в формате .npz
- Код с обучением и инференсом модели
- Видеопрезентация: Описание задачи, структура пайплайна, обоснование подходов. Видео должно быть загружено в облачное хранилище и предоставлена ссылка.
- Установочный пакет или ссылка на мобильное приложение / PWA

## Стек технологий
- Язык разработки: Flutter для мобильного приложения.
- Модели компьютерного зрения: Обученные модели YOLO и другие для детекции и сегментации.

