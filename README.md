# ПоздравОК — React + Bootstrap

Готовый праздничный сайт с:
- двумя таймерами на стартовом экране;
- салютами на canvas;
- падающим конфетти;
- красивым вступлением с большим количеством комплиментов;
- 3 фотографиями;
- отдельными поздравлениями от семьи, родителей и лично для тебя;
- появлением текста по словам;
- разными эффектами переходов, включая ауру и переворот третьей фотографии;
- адаптацией под ПК и телефон;
- React + Bootstrap 5.

## Запуск

1. Установи Node.js 18+ (лучше актуальную LTS-версию).
2. Открой терминал в этой папке.
3. Выполни:

npm install
npm run dev

4. Открой адрес, который покажет Vite (обычно http://localhost:5173).

## Сборка

npm run build

Папка dist будет готова для загрузки на Netlify/Vercel/GitHub Pages.

Фотографии находятся в `public/`.


## Если появляется ошибка esbuild

Если в консоли ошибка начинается с `failureErrorWithLog` и указывает на `node_modules/esbuild`,
это обычно повреждённая или несовместимая локальная установка зависимостей. В PowerShell из
папки проекта выполни:

```powershell
Remove-Item -Recurse -Force node_modules
Remove-Item -Force package-lock.json -ErrorAction SilentlyContinue
npm cache verify
npm install
npm run build
npm run dev
```

Если `Remove-Item` не срабатывает, закрой VS Code/терминал, который использует проект, и
повтори команды. Не добавляй `node_modules` в ZIP: он должен устанавливаться заново через `npm install`.
