# TTcux · staff

Личная страница-визитка: тёмный неон, дождь, частицы, неоновый курсор, плейлист с визуализатором, живой статус Discord, значки, счётчик просмотров, проекты.

## Файлы
- `index.html` — вся страница
- `avatar.webm`, `avatar.mp4` — аватарка (видео вместо GIF, в ~15 раз легче)
- `cover.jpg` — обложка по умолчанию, иконка вкладки, картинка пока грузится аватарка
- `og.jpg` — картинка-превью ссылки для Telegram / Discord / VK (1200×630)
- `bg.jpg` — размытый фон
- `music.mp3`, папка `music/` — треки; папка `covers/` — обложки треков
- `avatar.gif` больше не нужен — можно удалить

## Настройки
Всё меняется в блоке `CONFIG` в начале `<script>` внутри `index.html`:

| Поле | Что это |
|---|---|
| `telegram` | ник Telegram без @ |
| `github` | ник GitHub |
| `discordName` | ник Discord — кнопка «Discord» копирует его |
| `discordId` | числовой ID Discord для живого статуса |
| `goatcounter` | код сайта в GoatCounter (см. ниже). Пусто = запасной счётчик |
| `badges` | значки под ником: подсказка, иконка, цвет |
| `playlist` | треки: название, исполнитель, путь к mp3, обложка |
| `projects` | карточки проектов |
| `phrases` | фразы печатающегося текста |

### Счётчик просмотров через GoatCounter
1. Зарегистрируйся на https://www.goatcounter.com/signup — придумай код сайта, например `ttcux`
   (тогда панель будет на `https://ttcux.goatcounter.com`).
2. В панели: **Settings → Site settings** → включи **«Allow adding visitor counts on your website»** → Save.
3. В `index.html` впиши код: `goatcounter: 'ttcux',`
4. Закоммить и запушь. В панели GoatCounter видно графики, страны, устройства и откуда пришли.

### Значки
Иконки: `code`, `java`, `cube`, `wrench`, `server`, `moon`, `star`, `heart`, `bolt`.
Пример: `{ tip: 'Night coder', icon: 'moon', c: '#a55bff' },`

### Превью ссылки
В `<head>` прописан полный адрес `https://ttcux1.github.io/og.jpg`. Если поменяешь адрес сайта
(свой домен) — поменяй его и в тегах `og:url`, `og:image`, `twitter:image`.
Telegram кэширует превью: чтобы обновить, отправь ссылку боту @WebpageBot.

## Горячие клавиши
Пробел / K — пауза · ← → — перемотка на 5 с · N / P (или Shift+← →) — следующий / предыдущий трек ·
↑ ↓ — громкость · M — выключить звук · Enter — войти с заставки.
На телефоне треком можно управлять из шторки и с экрана блокировки.

## Как добавить трек
1. Положи mp3 в папку `music/`.
2. Добавь строку в `playlist`:
   `{ title: 'Название', artist: 'Исполнитель', file: 'music/track.mp3', cover: 'cover.jpg' },`

## Публикация (GitHub Desktop)
Скопируй файлы в папку клона репозитория → Commit to main → Push origin.
Через 1–2 минуты изменения на https://ttcux1.github.io/ (обнови с Ctrl+F5).
