---
description: Crea un worktree de git en .worktree/<nombre>.
agent: build
---

Crea un worktree de git a partir del argumento proporcionado.

Toma el argumento `$1` recibido por el comando y conviértelo en un slug:
- pasa todo a minúsculas
- reemplaza los espacios y caracteres no alfanuméricos por guiones (`-`)
- elimina guiones duplicados y finales

- Si no se proporciona ningún argumento, usa un nombre por defecto como `worktree`.

- Ejecuta únicamente el siguiente comando, sustituyendo `<slug>` por el nombre generado:

- No hagas nada más: no uses cd, no corras otros comandos, no edites archivos, no confirmes con el usuario, no hagas commit ni push.

- Reporta únicamente el resultado del comando (stdout/stderr y código de salida).

- Si los argumentos son muy largos, simplifícalos a un nombre significativo.

```
git worktree add .worktree/<slug>
```

No cambies de directorio. No hagas nada más.