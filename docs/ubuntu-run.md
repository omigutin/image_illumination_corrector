# Ubuntu Run Guide

Этот документ объясняет, как запускать готовую Ubuntu-сборку без ручной настройки Python.

## Что скачивать

Для Ubuntu пользователю нужен готовый архив со сборкой.

Обычно такой архив лучше брать из GitHub Releases или из артефактов GitHub Actions.

## Быстрый запуск

Если у пользователя уже есть файл `image-illumination-corrector-linux.tar.gz`, запуск такой:

```bash
tar -xzf image-illumination-corrector-linux.tar.gz
chmod +x image-illumination-corrector
./image-illumination-corrector
```

## Если сборка скачана из GitHub Actions

GitHub Actions обычно отдаёт `.zip`-артефакт, внутри которого уже лежит `.tar.gz`.

Тогда порядок такой:

```bash
unzip image-illumination-corrector-linux.zip
tar -xzf image-illumination-corrector-linux.tar.gz
chmod +x image-illumination-corrector
./image-illumination-corrector
```

## Возможные проблемы

### Permission denied

Нужно дать право на запуск:

```bash
chmod +x image-illumination-corrector
```

### No such file or directory

Обычно это значит, что архив ещё не распакован или команда запущена не из той папки.

### Нет графического окна

Приложение использует `tkinter`, значит ему нужен GUI-сеанс Ubuntu.

На headless-сервере без `DISPLAY` окно не откроется.

## Рекомендация по совместимости

Для Linux-сборок обычно безопаснее собирать на `ubuntu-22.04`, а не на `ubuntu-latest`.
