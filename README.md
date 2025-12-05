# Heart of the Night Bot

Telegram-бот для эмоциональной поддержки в ночное время.

## Описание

**Heart of the Night** — это Telegram-бот, созданный для тех, кто ищет поддержку в самые тёмные моменты. Бот предоставляет безопасное пространство для самовыражения и рефлексии.

### Функции бота:

- **AI — Тайны ночи** — получение атмосферных ответов от AI
- **AI — Шёпот тени** — мягкие напоминания о внутренней силе
- **AI — Зеркало души** — отражение ваших мыслей
- **Выговориться** — место для выражения тяжёлых мыслей
- **Отправить свою историю** — поделиться своей историей
- **Дневник ночи** — ведение личного дневника
- **Полуночная поэзия** — атмосферные поэтические строки
- **Летопись теней** — истории ночи
- **Мерцание свечи** — ритуалы для успокоения
- **Эхо ночи** — напоминание о том, что вас слышат
- **Тень друга** — виртуальный спутник
- **Сфера покоя** — визуализации для внутреннего покоя
- **Лабиринт разума** — исследование своих мыслей

## Требования

- Python 3.9+
- Telegram Bot Token (получить у [@BotFather](https://t.me/BotFather))

## Деплой на Fly.io (рекомендуется)

### 1. Установите Fly CLI

```bash
curl -L https://fly.io/install.sh | sh
```

### 2. Авторизуйтесь

```bash
fly auth login
```

### 3. Создайте приложение

```bash
fly launch --name heart-of-the-night-bot --region ams --no-deploy
```

### 4. Установите секреты

```bash
fly secrets set TELEGRAM_BOT_TOKEN="your_bot_token_here"
fly secrets set WEBHOOK_URL="https://heart-of-the-night-bot.fly.dev"
```

### 5. Задеплойте

```bash
fly deploy
```

После деплоя бот автоматически установит webhook и начнёт работать 24/7.

## Локальный запуск

1. Клонируйте репозиторий:
```bash
git clone https://github.com/YOUR_USERNAME/heart-of-the-night-bot.git
cd heart-of-the-night-bot
```

2. Установите зависимости:
```bash
pip install -r requirements.txt
```

3. Установите переменные окружения:
```bash
export TELEGRAM_BOT_TOKEN="your_bot_token_here"
export WEBHOOK_URL="https://your-domain.com"
export PORT=8080
```

4. Запустите бота:
```bash
python bot.py
```

## Структура проекта

```
heart-of-the-night-bot/
├── bot.py              # Основной файл бота (webhook + HTTP сервер)
├── requirements.txt    # Зависимости Python
├── Dockerfile          # Docker образ для деплоя
├── fly.toml           # Конфигурация Fly.io
├── README.md          # Документация
├── .gitignore         # Игнорируемые файлы
└── user_data/         # Данные пользователей (создаётся автоматически)
```

## Переменные окружения

| Переменная | Описание |
|------------|----------|
| `TELEGRAM_BOT_TOKEN` | Токен бота от @BotFather |
| `WEBHOOK_URL` | URL вашего приложения (например, https://app-name.fly.dev) |
| `PORT` | Порт для HTTP сервера (по умолчанию 8080) |

## Лицензия

MIT License

## Автор

Heart of the Night Project
