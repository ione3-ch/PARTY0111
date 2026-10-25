# Birthday Night 31.10

Неоновый сайт-приглашение на день рождения: заставка, обратный отсчёт, детали вечеринки, ответ гостя и встроенный рейв-бит (генерируется в браузере, без аудиофайлов).

## Файлы

- `index.html` — весь сайт (стили и скрипты внутри)
- `poster.jpg` — афиша
- `.nojekyll` — чтобы GitHub Pages отдавал файлы как есть

## Как опубликовать на GitHub Pages

1. Создай новый публичный репозиторий на github.com, например `birthday-night`.
2. Нажми **Add file → Upload files** и перетащи `index.html`, `poster.jpg`, `README.md` и `.nojekyll`. Нажми **Commit changes**.
3. Открой **Settings → Pages**. В разделе **Build and deployment** выбери **Source: Deploy from a branch**, ветку `main` и папку `/ (root)`, нажми **Save**.
4. Через 1–2 минуты сайт будет доступен по адресу `https://<твой-логин>.github.io/birthday-night/`.

Через терминал:

```bash
cd birthday-night
git init
git add .
git commit -m "Birthday invite site"
git branch -M main
git remote add origin https://github.com/<твой-логин>/birthday-night.git
git push -u origin main
```

## Превью ссылки в Telegram / WhatsApp

После публикации замени в `index.html` строку

```html
<meta property="og:image" content="poster.jpg">
```

на полный адрес: `https://<твой-логин>.github.io/birthday-night/poster.jpg` — так мессенджеры покажут афишу в превью.

## Что поменять под себя

- Дата отсчёта — в скрипте строка `Date.parse('2026-10-31T21:00:00+03:00')`.
- Адрес, дресс-код и тексты — прямо в разметке `index.html`.
- Кнопка трека ведёт на поиск песни на Яндекс Музыке; можно вставить прямую ссылку.
