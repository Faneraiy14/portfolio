# Projects

*[English](README.md)*

Карта того, що я зробив — [github.com/Faneraiy14](https://github.com/Faneraiy14).
Згруповано за тим, що це реально таке, а не за тим, коли зроблено.

## Nyxilum — власна мова програмування

Компілятор у байткод + стекова VM з нуля, з власною стандартною
бібліотекою й пакетним менеджером. Самохостована — власний інтерпретатор
написаний тією самою мовою.

- **[NyxilumLang](https://github.com/Faneraiy14/NyxilumLang)** — сама мова: компілятор, VM, 166 вбудованих функцій (математика, рядки, HTTP + WebSocket-сервер, 2D-графіка, GUI, конкурентність, вбудована БД, керування процесами ОС, zip/regex).
- **[NyxilumDb](https://github.com/Faneraiy14/NyxilumDb)** — вбудована key-value база даних, на якій працює `dbOpen()` у NyxilumLang, з WAL-довговічністю.
- **[NyxilumNode](https://github.com/Faneraiy14/NyxilumNode)** — самостійний рантайм (`nx файл.nx`), плюс пакетний менеджер (`nx install owner/repo`). Готовий `.exe` — .NET встановлювати не треба.
- **[NyxilumMcp](https://github.com/Faneraiy14/NyxilumMcp)** — MCP-сервер, щоб AI-асистент міг компілювати, запускати, лінтити й вести REPL-сесію з `.nx`-кодом напряму, у пісочниці.
- **[nyxilum-assert](https://github.com/Faneraiy14/nyxilum-assert)** — бібліотека тверджень для тестування коду NyxilumLang.

## Зроблено на Nyxilum

Реальні застосунки, не іграшкові демки — кожен працює повністю на
власній стандартній бібліотеці NyxilumLang, без зовнішніх залежностей.

- **[nyxilum-chat](https://github.com/Faneraiy14/nyxilum-chat)** — живий груповий чат: справжнє WebSocket-розсилання одне-до-багатьох.
- **[nyxilum-control-center](https://github.com/Faneraiy14/nyxilum-control-center)** — живий монітор системи: веб-дашборд, WebSocket live-пуш, ping, експорт історії в zip.
- **[nyxilum-paste](https://github.com/Faneraiy14/nyxilum-paste)** — сервіс шерингу сніпетів у стилі Pastebin.

## FL Launcher

Minecraft-лаунчер, який я активно розробляю й доставляю реальним
користувачам.

- **[fl-launcher](https://github.com/Faneraiy14/fl-launcher)** — канал релізів (`.exe` з автооновленням); вихідний код лежить в окремому приватному репо.
- **[fl-bridge](https://github.com/Faneraiy14/fl-bridge)** — релізи `FLBridge.jar`, мод-лоадера, який FL Launcher завантажує й оновлює автоматично.

## NyxilumCMS

Багатоцільова система керування контентом, написана з нуля — PHP + MySQL, без фреймворку.

- **[NyxilumCMS](https://github.com/Faneraiy14/NyxilumCMS)** — контент довільного типу, категорії, меню, медіа, ролі (admin/editor) з двофакторним входом (TOTP), заплановані публікації, SEO/Open Graph теги, sitemap.xml + RSS, повний експорт/імпорт і власний веб-інсталятор. Супутній MCP-сервер дає AI-асистенту прямий доступ до бази (лишається приватним).

## MCP-сервери

Інструменти, що дають AI-асистенту реально ЩОСЬ РОБИТИ, а не лише
розповідати про це.

- **[wordpress-mcp](https://github.com/Faneraiy14/wordpress-mcp)** — MCP-сервер для WordPress (стан сайту, пости, плагіни), збудований на офіційному `modelcontextprotocol/php-sdk`.
- **[minecraft-rcon-mcp](https://github.com/Faneraiy14/minecraft-rcon-mcp)** — дає AI керувати живим Minecraft-сервером через RCON (гравці, чат, телепорт, погода і не тільки).
- **[workspace-status-mcp](https://github.com/Faneraiy14/workspace-status-mcp)** — п'ять інструментів для роботи з десятками репо одразу: знімок git+CI-статусу, які документи `Architecture/<repo>.txt` відсутні чи застаріли, дрейф релізу між репо-джерелом і репо, що з нього тегує релізи, і пакетна перевірка статусу GitHub PR (стан, CI, рішення рев'ю, кількість top-level і inline коментарів окремо).
- **[ci-watch-mcp](https://github.com/Faneraiy14/ci-watch-mcp)** — чекає завершення прогону GitHub Actions і звітує результат, щоб AI не опитував вручну.

*(NyxilumMcp уже в списку вище, під Nyxilum — це теж MCP-сервер.)*

## Інструменти розробника

- **[anylint](https://github.com/Faneraiy14/anylint)** — кросмовний статичний аналізатор: одне ядро, провайдери-плагіни на мову (PHP, NyxilumLang, JS/TS + 15 через tree-sitter) — ті самі правила ловлять ті самі баги скрізь.
- **[anylint-vscode](https://github.com/Faneraiy14/anylint-vscode)** — розширення VS Code: вбудована діагностика й quick fix від anylint.
- **[envcheck](https://github.com/Faneraiy14/envcheck)** — CLI, що звіряє `.env` з `.env.example` (відсутні/порожні/зайві ключі).
- **[secretscan](https://github.com/Faneraiy14/secretscan)** — CLI-сканер випадково закомічених секретів (API-ключі, токени, приватні ключі).

## Просто для фану

- **[CursorNinja](https://github.com/Faneraiy14/CursorNinja)** — Fruit Ninja курсором миші. Python + tkinter, без залежностей.
- **[DesktopCat](https://github.com/Faneraiy14/DesktopCat)** — котик на робочому столі: сидить, стукає по клавішах у ритм друку, засинає, коли ти відходиш. Python + tkinter, без залежностей.
- **[tap-site](https://github.com/Faneraiy14/tap-site)** — клікер-тапалка з окремими backend і frontend на TypeScript.

## Дослідження безпеки

- **[obriycipher](https://github.com/Faneraiy14/obriycipher)** — саморобний блоковий шифр, винесений з месенджера, чесно позначений як небезпечний для реального використання (див. його `SECURITY.md`).

## Контриб'юшени в чужі проєкти

- **[cyklokoalicia/OpenSourceBikeShare](https://github.com/cyklokoalicia/OpenSourceBikeShare)** — реальна, жива система шерингу велосипедів у Братиславі. 9 змерджених PR: впровадив статичний аналіз PHPStan (рівень 4) і виправив усі 82 знайдені помилки, далі — низка реальних багів, знайдених під час рев'ю коду та розслідування CI: `TypeError`-крах на старих записах кредитної історії, баг генератора купонів, що міг тихо видати менше кодів, ніж запитано (або зіткнутись на `UNIQUE`-колонці), відсутній `ext-intl`, що ламав ICU-переклади, і регресія Symfony-патча безпеки, яка ламала сесії при зміні пароля.
- **[modelcontextprotocol/php-sdk](https://github.com/modelcontextprotocol/php-sdk)** — офіційний PHP SDK для MCP. Один змерджений PR (варіативні параметри тулів).
