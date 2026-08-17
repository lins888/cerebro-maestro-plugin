# Cerebro Maestro — plugin de Claude Code

Monta un **vault de Obsidian como fuente unica de verdad** y le ensena a Claude Code
a consultarlo antes de trabajar, ademas de mantener memoria persistente.

Es una **plantilla vacia**: no trae datos personales ni reglas de nadie. Cada quien
lo llena con lo suyo.

## Que incluye

- **Comando `/cerebro-init`** — crea el vault (`permanent/`, `proyectos/_plantilla/`)
  y deja la regla de trabajo en tu `~/.claude/CLAUDE.md`.
- **Skill `cerebro-maestro`** — le dice a Claude como usar el vault (Pendientes primero,
  vault manda sobre la memoria) y como mantener memoria persistente.

## Instalacion

En Claude Code:

```
/plugin marketplace add lins888/cerebro-maestro-plugin
/plugin install cerebro-maestro
```

(Si te lo pasaron como carpeta local: `/plugin marketplace add /ruta/a/cerebro-maestro-plugin`)

## Uso

1. Corre `/cerebro-init` (opcional: `/cerebro-init ~/Desktop/Mi-Cerebro`).
2. Abre el vault en Obsidian y escribe tus reglas en `permanent/`.
3. Crea una carpeta por proyecto copiando `proyectos/_plantilla/`.
4. Desde ahi, Claude consulta el vault (Pendientes primero) antes de trabajar.

## Nota sobre "apenas se abre Obsidian"

Claude Code **no se dispara solo al abrir Obsidian**. El plugin actua cuando abris una
sesion de Claude Code en ese equipo. Si quieres automatizar algo al abrir Obsidian
necesitas un plugin de Obsidian aparte; esto no lo cubre.
