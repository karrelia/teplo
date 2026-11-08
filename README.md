# Показники котельні — демо APK

Android-обгортка навколо клікабельного прототипу (`app/src/main/assets/index.html`). Працює офлайн.

## Спосіб 1 — без встановлення програм (GitHub, у браузері)
1. Зареєструйтесь на github.com (безкоштовно).
2. Створіть новий репозиторій: «+» → New repository → назва, наприклад `pokaznyky` → Create.
3. На сторінці репозиторію: «uploading an existing file» → перетягніть **весь вміст** папки `android` (разом із папкою `.github`) → Commit changes.
   - Якщо папка `.github` не перетягується (прихована), створіть файл вручну: Add file → Create new file → назва `.github/workflows/build-apk.yml` → вставте вміст із цього архіву → Commit.
4. Вкладка **Actions** → «Build APK» → дочекайтесь зеленої галочки (~5 хв).
5. Відкрийте запуск → внизу «Artifacts» → **pokaznyky-apk** → завантажиться zip з `app-debug.apk`.

## Спосіб 2 — Android Studio
File → Open → папка `android` → Build → Build APK(s). Файл: `app/build/outputs/apk/debug/app-debug.apk`.

## Встановлення на телефон
Перекиньте `app-debug.apk` на телефон (кабель, Telegram, Viber) → відкрийте → дозвольте «Встановлення з невідомих джерел».

## Що змінити
- Номер диспетчера: зараз умовний `tel:+380000000000` у прототипі.
- Іконка: стандартна системна — замініть у `AndroidManifest.xml`.
- Оновити прототип: замініть `assets/index.html` новою офлайн-версією — GitHub перебудує APK автоматично.
