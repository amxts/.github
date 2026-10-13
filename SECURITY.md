# Security policy

**English** | [Русский](#политика-безопасности)

## Supported versions

Fixes go to the latest release line of each package, and come out as its
next patch. A security fix for an older line is made when it is still widely
used.

| Package | Supported |
| --- | --- |
| `@amxts/core` and the server's module | the latest line - now 0.3.x |
| `@amxts/cli`, `create-amxts` | the latest version |
| the official modules | the latest version of each |

## Reporting a vulnerability

Please do not open a public issue for a vulnerability.

Report it privately on GitHub: open the repository it is in, then
**Security → Report a vulnerability**
([amxts/amxts](https://github.com/amxts/amxts/security/advisories/new) for
the core and the server's module). Say what is affected, how to reproduce it,
and what it allows - a plugin or a player reaching files outside the game
folder, a crash a player can cause, a way round a check.

You get an answer within a week. Once a fix is released, the advisory is
published with credit to you, unless you ask otherwise.

---

# Политика безопасности

## Поддерживаемые версии

Исправления выходят в последней линии каждого пакета, следующим патчем. Для
старой линии исправление безопасности делается, если ею ещё широко пользуются.

| Пакет | Поддерживается |
| --- | --- |
| `@amxts/core` и модуль сервера | последняя линия - сейчас 0.3.x |
| `@amxts/cli`, `create-amxts` | последняя версия |
| официальные модули | последняя версия каждого |

## Как сообщить об уязвимости

Не открывайте об уязвимости публичный issue.

Сообщите приватно на GitHub: в репозитории, к которому она относится,
**Security → Report a vulnerability**
([amxts/amxts](https://github.com/amxts/amxts/security/advisories/new) - для
ядра и модуля сервера). Напишите, что затронуто, как воспроизвести и что это
позволяет - доступ плагина или игрока к файлам вне папки игры, падение,
которое может вызвать игрок, обход проверки.

Ответ - в течение недели. Когда исправление выйдет, сообщение публикуется с
благодарностью вам, если вы не попросите иначе.
