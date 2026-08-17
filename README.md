# 🧠 Cerebro Maestro — plugin para Claude Code

> Convierte un vault de Obsidian en la **fuente única de verdad** de tu trabajo, y
> haz que Claude Code lo consulte siempre antes de tocar nada.

La mayoría de la gente le repite el mismo contexto a la IA una y otra vez: qué hace
cada proyecto, qué quedó pendiente, qué reglas seguir. **Cerebro Maestro** rompe eso:
tú escribes tu contexto una vez en Obsidian y Claude lo lee solo, en el orden correcto,
antes de trabajar.

Es una **plantilla vacía**. No trae datos de nadie: tú lo llenas con lo tuyo.

---

## ✨ Qué puedes lograr con esto

- **Un cerebro central, no memoria dispersa.** Todos tus proyectos viven en un solo
  vault de Obsidian. Claude lee de ahí en vez de adivinar.
- **"Pendientes primero" automático.** Cada proyecto tiene su lista de pendientes y
  Claude la lee *antes* que cualquier otra cosa, así arranca por lo que importa hoy.
- **Reglas globales que siempre se respetan.** Lo que pongas en `permanent/` aplica a
  todos tus proyectos, sin recordárselo cada vez.
- **El vault manda.** Si tu contexto contradice una suposición de la IA, gana el vault.
  Menos alucinaciones, menos "invento un dato para que funcione".
- **Memoria persistente ordenada.** Claude guarda hechos estables (decisiones,
  preferencias, contexto de negocio) que no viven en el código, sin duplicar.
- **Portátil y compartible.** Es un plugin: se instala en un comando y funciona igual
  en cualquier equipo.

---

## 🚀 Instalación

En Claude Code:

```
/plugin marketplace add lins888/cerebro-maestro-plugin
/plugin install cerebro-maestro
```

> ¿Prefieres clonarlo? `git clone https://github.com/lins888/cerebro-maestro-plugin.git`
> y luego `/plugin marketplace add /ruta/al/repo`.

---

## 🛠️ Uso en 3 pasos

1. **Monta el vault:**
   ```
   /cerebro-init
   ```
   (opcional: `/cerebro-init ~/Desktop/Mi-Cerebro` para elegir la ruta)

   Esto crea la estructura y deja la regla de trabajo en tu `~/.claude/CLAUDE.md`.

2. **Llénalo en Obsidian:** escribe tus reglas en `permanent/` y crea una carpeta por
   proyecto copiando `proyectos/_plantilla/`.

3. **Trabaja normal.** Desde ahí Claude consulta el vault (Pendientes primero) antes de
   ponerse a hacer cualquier cosa.

---

## 📦 Qué incluye

| Componente | Qué hace |
|---|---|
| **Comando `/cerebro-init`** | Crea el vault (`permanent/`, `proyectos/_plantilla/`) y la regla en `~/.claude/CLAUDE.md`. |
| **Skill `cerebro-maestro`** | Le enseña a Claude a usar el vault como fuente de verdad y a mantener memoria persistente sin inventar datos. |

### Estructura que genera

```
Cerebro-Maestro/
├── README.md
├── permanent/                 # reglas globales (mandan sobre todo)
│   └── reglas-globales.md
└── proyectos/
    └── _plantilla/            # copia esto por cada proyecto nuevo
        └── _plantilla.md      # Pendientes primero → Contexto → Decisiones → Enlaces
```

---

## ⚠️ Nota

Claude Code **no se dispara solo al abrir Obsidian**. El plugin actúa cuando abres una
sesión de Claude Code en ese equipo. Automatizar algo *al abrir Obsidian* requeriría un
plugin de Obsidian aparte; esto no lo cubre.

---

## 📄 Licencia

MIT — úsalo, modifícalo y compártelo libremente.
