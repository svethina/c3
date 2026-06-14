# s6

Браузерный калькулятор.

## Локальный запуск

Откройте `index.html` в браузере или запустите локальный сервер:

```powershell
npx serve .
```

## Деплой на Vercel

Проект — статический сайт без сборки. Все настройки заданы в `vercel.json`.

### Через Git (рекомендуется)

1. Создайте проект на [vercel.com](https://vercel.com) и подключите репозиторий `svethina/c3`.
2. Убедитесь, что используется ветка `main`.
3. Настройки сборки подтянутся из `vercel.json` автоматически:
   - **Framework Preset:** Other
   - **Build Command:** пусто
   - **Output Directory:** `.`
4. Нажмите **Deploy**.

> **Важно:** подключайте именно репозиторий `svethina/c3`. Старый проект `s6` на Vercel не связан с этим репозиторием и отдаёт 404.

### Через CLI

```powershell
pnpm dlx vercel
```

Для продакшн-деплоя:

```powershell
pnpm dlx vercel --prod
```

### Проверка после деплоя

1. Откройте корневой URL (`/`).
2. Если видите 404 — в дашборде Vercel откройте **Deployments → Source → Output** и убедитесь, что там есть `index.html`.
3. Проверьте **Settings → Build & Deployment**: Output Directory должен быть `.`, Build Command — пустой.

После деплоя калькулятор доступен по `/`. Старый путь `/calculator.html` перенаправляется на главную.
