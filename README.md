# s6

Браузерный калькулятор.

## Локальный запуск

Откройте `index.html` в браузере или запустите локальный сервер:

```powershell
npx serve .
```

## Деплой на Vercel

### Через Git (рекомендуется)

1. Загрузите репозиторий на GitHub.
2. На [vercel.com](https://vercel.com) создайте новый проект и подключите репозиторий.
3. Настройки сборки оставьте по умолчанию:
   - **Framework Preset:** Other
   - **Build Command:** пусто
   - **Output Directory:** `.`
   - **Install Command:** `pnpm install` (или оставьте автоопределение)
4. Нажмите **Deploy**.

### Через CLI

```powershell
pnpm dlx vercel
```

Для продакшн-деплоя:

```powershell
pnpm dlx vercel --prod
```

После деплоя калькулятор будет доступен по корневому URL (`/`). Старый путь `/calculator.html` автоматически перенаправляется на главную.
