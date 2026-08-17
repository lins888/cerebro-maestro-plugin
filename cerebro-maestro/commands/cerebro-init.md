---
description: Monta el vault Cerebro Maestro (fuente unica de verdad) y deja el sistema listo para trabajar.
argument-hint: [ruta-del-vault]  (opcional, por defecto ~/Desktop/Cerebro-Maestro)
allowed-tools: Bash(mkdir:*), Bash(ls:*), Write, Read, Edit
---

Vas a montarle al usuario su **Cerebro Maestro**: un vault de Obsidian que sera la
fuente unica de verdad para todos sus proyectos, mas las instrucciones para que
Claude Code lo consulte siempre antes de trabajar.

## Paso 1 — Ubicacion del vault

Usa la ruta que paso el usuario en `$ARGUMENTS`. Si viene vacia, usa
`~/Desktop/Cerebro-Maestro`. Confirma la ruta antes de crear nada.

## Paso 2 — Crear la estructura (vacia)

Crea estas carpetas y archivos semilla dentro del vault:

```
Cerebro-Maestro/
├── README.md                 # que es esto y como se usa
├── permanent/                # reglas globales que aplican a TODO proyecto
│   └── reglas-globales.md
└── proyectos/
    └── _plantilla/
        └── _plantilla.md     # plantilla de nota de proyecto
```

- `README.md`: explica que el vault es la fuente unica de verdad, que `permanent/`
  manda sobre todo, y que cada proyecto vive en `proyectos/<nombre>/`.
- `permanent/reglas-globales.md`: dejalo con encabezados vacios para que el usuario
  escriba sus propias reglas (ej. "Estilo de commits", "Que nunca hacer",
  "Preferencias de trabajo"). NO inventes reglas.
- `proyectos/_plantilla/_plantilla.md`: una nota con secciones en este orden:
  `## Pendientes` (primero, siempre), `## Contexto`, `## Decisiones`, `## Enlaces`.

## Paso 3 — Regla de trabajo en CLAUDE.md

Anade (o crea) `~/.claude/CLAUDE.md` con un bloque que diga, adaptado a la ruta real:

> # Cerebro Maestro (fuente unica de verdad)
> El vault en `<RUTA>` manda. Antes de trabajar cualquier proyecto, consulta su nota
> en `proyectos/<nombre>/` (seccion **Pendientes** primero) y las reglas en
> `permanent/`. El vault manda sobre la auto-memoria de Claude Code.

Si ya existe un bloque parecido, no lo dupliques: actualiza la ruta.

## Paso 4 — Cerrar

Muestra al usuario el arbol creado y explicale en 3 lineas: (1) escribe tus reglas
en `permanent/`, (2) crea una carpeta por proyecto copiando `_plantilla`, (3) yo
consultare el vault solo desde ahora. No llenes contenido personal por el.
