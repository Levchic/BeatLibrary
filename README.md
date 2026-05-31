# Pocket Operations — Drum Pattern Reference
## Инструкция по деплою

Приложение состоит из трёх файлов:
- `index.html` — само приложение (всё внутри)
- `manifest.json` — настройки PWA
- `sw.js` — сервис-воркер (работа офлайн)

---

## Вариант 1: Vercel (рекомендую — бесплатно, быстро)

**Шаг 1.** Создай аккаунт на [vercel.com](https://vercel.com) (можно войти через GitHub)

**Шаг 2.** Установи Vercel CLI (нужен Node.js):
```bash
npm install -g vercel
```

**Шаг 3.** Зайди в папку с файлами и задеплой:
```bash
cd pocket-operations
vercel
```

Vercel задаст несколько вопросов — отвечай Enter на всё. Через 30 секунд получишь ссылку вида `https://pocket-operations-xxx.vercel.app`

**Обновить сайт позже:**
```bash
vercel --prod
```

---

## Вариант 2: Netlify (ещё проще — drag & drop)

**Шаг 1.** Зайди на [netlify.com](https://netlify.com) и зарегистрируйся

**Шаг 2.** На дашборде найди блок **"Deploy manually"**

**Шаг 3.** Перетащи папку `pocket-operations` прямо в браузер

Готово. Netlify сам выдаст ссылку вида `https://random-name.netlify.app`

Чтобы обновить — просто перетащи папку снова.

---

## Вариант 3: GitHub Pages (бесплатно + своя история изменений)

**Шаг 1.** Создай репозиторий на [github.com](https://github.com)

**Шаг 2.** Загрузи файлы (кнопка "Add file → Upload files")

**Шаг 3.** Зайди в Settings → Pages → Source: **Deploy from branch → main → / (root)**

Сайт будет на `https://твой-юзернейм.github.io/имя-репо`

---

## Своё доменное имя

Если хочешь адрес типа `drumref.ru`:
1. Купи домен на [reg.ru](https://reg.ru) или [namecheap.com](https://namecheap.com) (~$10/год)
2. В Vercel или Netlify зайди в Settings → Domains → Add domain
3. Пропиши NS-записи, которые они покажут, в настройках домена

Это занимает 10 минут + до 24 часов на распространение DNS.

---

## Добавить на телефон (PWA)

Приложение уже готово к установке на телефон:

**iOS (Safari):** Открой сайт → кнопка «Поделиться» → «На экран "Домой"»

**Android (Chrome):** Открой сайт → три точки → «Добавить на главный экран»

После этого приложение работает как нативное — без браузерной строки, с иконкой. Работает офлайн после первого открытия.

---

## Структура файлов

```
pocket-operations/
├── index.html      ← всё приложение здесь
├── manifest.json   ← настройки PWA
├── sw.js           ← офлайн-кэш
├── icon-192.png    ← иконка (добавить самостоятельно)
└── icon-512.png    ← иконка большая (добавить самостоятельно)
```

Иконки не обязательны для работы, но нужны если хочешь красивую иконку при установке на телефон. Можно сгенерировать на [favicon.io](https://favicon.io) или [realfavicongenerator.net](https://realfavicongenerator.net).
