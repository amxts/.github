<div align="center">

<img src="logo.svg" width="112" alt="amxts">

# amxts

**Counter-Strike 1.6 plugins in TypeScript.**<br>
Write a plugin the way you write any TypeScript - amxts compiles it to native code<br>
and runs it inside AMX Mod X, next to your Pawn plugins.

[Documentation](https://amxts.github.io/) · [Getting started](https://amxts.github.io/docs/getting-started/) · [API](https://amxts.github.io/docs/plugin/) · [По-русски](#по-русски)

</div>

```ts
import { Player, plugin, print, server } from "~/facade";

plugin({ name: "Hello", version: "1.0.0", author: "you", description: "An example" });

server.addCommand("/hp", (player: Player) => {
	print(player, `${player.name}, your HP: !g${player.health}`);
	if (player.health < 50) player.health = 100;
});

server.addEventListener("putinserver", (event) => {
	setTimeout(() => print(event.player, "Welcome!"), 3000);
});
```

- **TypeScript you already know** - classes, closures, `Map`, template strings, `async`/`await`, timers.
- **The editor knows the game** - every player field, entity, event and native with its real type and a tooltip.
- **Save and play** - the server compiles a plugin the moment you save it and swaps it in.
- **Faster than Pawn** - compiled to machine code ahead of time.
- **Windows and Linux** servers, with a ready Docker image.

```sh
npm create amxts@latest
```

## По-русски

**Плагины для Counter-Strike 1.6 на TypeScript.** Пишете плагин так же, как любой
код на TypeScript, — amxts компилирует его в машинный код и запускает внутри
AMX Mod X рядом с вашими плагинами на Pawn. Классы, замыкания, `async`/`await`,
таймеры; редактор знает каждое поле игрока, событие и натив; сервер пересобирает
плагин при сохранении. Windows и Linux, готовый Docker-образ.

[Документация](https://amxts.github.io/ru/) · [Первый плагин](https://amxts.github.io/ru/docs/getting-started/)
