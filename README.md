# mogram-gifts

Каталог кастомных подарков NimarkoGram.

## Структура

- `catalog.json` — список подарков. Клиент и сервер читают этот файл по прямой ссылке.
- `gifts/` — файлы подарков в формате `.tgs` (анимированный стикер Telegram).

## Как добавить подарок

1. Положите файл `.tgs` в папку `gifts/`, например `gifts/rose.tgs`.
2. Добавьте запись в `catalog.json` в массив `gifts`:

```json
{
  "id": "rose",
  "title": "Роза",
  "file": "gifts/rose.tgs",
  "price_stars": 0,
  "created_at": "2026-11-19T00:00:00Z"
}
```

- `id` — уникальный, латиницей, без пробелов.
- `file` — путь относительно корня репозитория.
- `price_stars` — пока всегда `0`.

Коммит в `main` сразу попадает в каталог, передеплоивать сервер не нужно.

## Прямые ссылки

Каталог: `https://raw.githubusercontent.com/BayRex1/mogram-gifts/main/catalog.json`

Файл подарка: `https://raw.githubusercontent.com/BayRex1/mogram-gifts/main/<file>`
