## Пояснительная записка к composer.json

### Основные зависимости (`require`)

| № | Пункт задания | Пакет | Зачем |
|---|---------------|-------|-------|
| 1 | БД для хранения данных | `laravel/framework` | Eloquent ORM + Query Builder, миграции, сиды. Поддержка MySQL/PostgreSQL/SQLite/MSSQL — отдельный пакет не нужен. |
| 2 | Кеш в памяти | `predis/predis` | Чистый PHP-клиент Redis (без C-расширения). Используется как драйвер кеша Laravel для хранения результатов тяжёлых SQL-запросов. |
| 3 | XLS-отчёты | `maatwebsite/excel` | Экспорт данных в XLSX/CSV/XLS, в т.ч. потоковый для больших выборок. |
| 4 | PDF-документы | `barryvdh/laravel-dompdf` | Генерация PDF из Blade-шаблонов, поддержка кириллицы и встраивания шрифтов. |
| 5 | SMS-верификация | `laravel/vonage-notification-channel` | Официальный канал Laravel-нотификаций для отправки SMS через Vonage (Nexmo). |
| 6 | E-mail-уведомления и рассылки | `laravel/framework` | Компонент `Illuminate\Mail` (Symfony Mailer) уже входит в ядро: SMTP, Mailgun, SES, очереди, шаблоны Blade. Отдельный пакет не требуется. |
| 7 | Облачное хранилище | `league/flysystem-aws-s3-v3` | Адаптер Flysystem для AWS S3. Laravel «из коробки» использует его для диска `s3`. При необходимости Azure Blob добавляется отдельно. |
| 8 | Служба доставки | `sch-group/pickpoint` | Готовый коннектор к API PickPoint для расчёта стоимости и оформления отправлений. |
| 9 | Авторизация через соцсети | `laravel/socialite` + `socialiteproviders/vkontakte` + `socialiteproviders/yandex` | Socialite даёт единый OAuth-интерфейс, провайдеры добавляют ВКонтакте и Яндекс. |
| 10 | Выгрузка в Яндекс.Маркет | `bukashk0zzz/yml-generator` | Формирует YML-файл с товарами в формате, который принимает Яндекс.Маркет. |
| 11 | Онлайн-оплата | `yoomoney/yookassa-sdk-php` | Официальный SDK ЮKassa: создание платежей, вебхуки, возвраты, чеки. |

### Зависимости для разработки (`require-dev`)

| № | Пункт задания | Пакет | Зачем |
|---|---------------|-------|-------|
| 12 | Тестирование | `phpunit/phpunit` | Стандартный фреймворк модульных и функциональных тестов Laravel. |
