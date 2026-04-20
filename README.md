# image_illumination_corrector

Утилита для коррекции виньетки и выравнивания яркости по всему изображению с живым предпросмотром, пресетами и пакетной обработкой.

GitHub:

- [omigutin/image_illumination_corrector](https://github.com/omigutin/image_illumination_corrector)

## Что умеет

- оценивать плавную неравномерность яркости по кадру;
- исправлять виньетку разными методами;
- настраивать параметры в GUI с предпросмотром;
- сохранять и загружать пресеты;
- обрабатывать целую папку изображений;
- использовать опорный кадр и радиальную модель виньетки.

## Документация

- [Архитектура](docs/architecture.md)
- [Справочник по методам](docs/methods-guide.md)
- [Запуск на Ubuntu](docs/ubuntu-run.md)

## Установка через Poetry

```bash
poetry env use 3.12
poetry install
```

## Запуск через Poetry

```bash
poetry run python -m image_illumination_corrector
```

## Запуск без Poetry

```bash
py -3.12 -m venv .venv
.venv\Scripts\activate
pip install -e .
python -m image_illumination_corrector
```

## Структура проекта

- `image_illumination_corrector/` - исходный код приложения
- `docs/` - документация
- `presets/` - пресеты пользователя
- `images/` - тестовые и рабочие изображения

## Сборки

Готовые исполняемые файлы лучше публиковать через GitHub Releases или получать как артефакты GitHub Actions, а не хранить внутри репозитория.
