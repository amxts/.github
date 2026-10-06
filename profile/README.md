<div align="center">

<img src="logo.svg" width="112" alt="amxts">

# amxts

**Counter-Strike 1.6 plugins in TypeScript.**<br>
Write a plugin the way you write any TypeScript. amxts compiles it to machine code<br>
and runs it inside AMX Mod X, next to your Pawn plugins.

[Documentation](https://amxts.github.io/) · [Getting started](https://amxts.github.io/docs/getting-started/quick-start) · [Modules](https://amxts.github.io/modules) · [По-русски](#по-русски)

</div>

```ts
plugin({ name: "Hello", version: "1.0.0", author: "you", description: "An example" });

server.addCommand("/hp", ({ player }) => {
	print(player, `${player.name}, your HP: ${player.health}`);
	if (player.health < 50) player.health = 100;
});

server.addEventListener("putInServer", (event) => {
	setTimeout(() => print(event.player, "Welcome!"), 3000);
});
```

- **TypeScript you already know**: classes, closures, `Map`, template strings, `async`/`await`, timers. No import lines.
- **Players and entities are objects**: `player.health = 100`, `player.team == "CT"`, events as in the DOM, with `preventDefault()`.
- **The editor knows the game**: every field, event and native has its real type and a tooltip, in English or Russian.
- **Save and play**: `amxts dev` rebuilds what you saved and reloads the running server, with no map change.
- **Tests without a server**: your plugin runs on a fake server under `bun test`.
- **Modules**: menus, configs, FTP and more from the [catalog](https://amxts.github.io/modules), one `amxts module add` away.
- **Windows and Linux**, ReHLDS or plain HLDS, AMX Mod X 1.9 and later.

```sh
npm create amxts@latest
```

| | |
| --- | --- |
| [**amxts**](https://github.com/amxts/amxts) | the core: the API, the compiler and the AMX Mod X module |
| [**amxts-cli**](https://github.com/amxts/amxts-cli) | `create-amxts` and the `amxts` command: `build`, `dev`, `test`, `module add` |
| [**amxts-vscode**](https://github.com/amxts/amxts-vscode) | VS Code: completion and checks for menu and config files |
| [**modules**](https://github.com/amxts/modules) | the module catalog: one YAML file per module, added by pull request |

## По-русски

**Плагины для Counter-Strike 1.6 на TypeScript.** Плагин пишется так же, как любой
код на TypeScript: amxts компилирует его в машинный код и запускает внутри
AMX Mod X рядом с плагинами на Pawn. Классы, замыкания, `async`/`await`, таймеры,
никаких строк импорта. Редактор знает каждое поле игрока, событие и натив.
`amxts dev` пересобирает плагин при сохранении и перезагружает его на работающем
сервере. Тесты без сервера, модули из каталога. Windows и Linux, ReHLDS и обычный HLDS.

[Документация](https://amxts.github.io/ru) · [Первый плагин](https://amxts.github.io/ru/docs/getting-started/quick-start) · [Модули](https://amxts.github.io/ru/modules)
