---
name: cerebro-maestro
description: Como trabajar con el vault Cerebro Maestro como fuente unica de verdad y mantener memoria persistente. Usar al empezar cualquier proyecto que tenga un vault Obsidian de Cerebro Maestro, antes de leer o modificar codigo, y cuando aparezca un hecho estable que valga la pena recordar.
---

# Cerebro Maestro — forma de trabajo

El usuario mantiene un **vault de Obsidian** que es la **fuente unica de verdad**.
Manda sobre la auto-memoria de Claude Code y sobre cualquier suposicion.

## Antes de trabajar un proyecto

1. Abre la nota del proyecto en `proyectos/<nombre>/` dentro del vault.
2. Lee **primero la seccion `## Pendientes`** — ahi esta lo que importa ahora.
3. Lee las reglas en `permanent/` — aplican a todos los proyectos.
4. Si el vault contradice el codigo o tu memoria, **gana el vault**; si el vault
   contradice la realidad del codigo, dilo en vez de asumir.

## Estructura del vault

```
<vault>/
├── permanent/            # reglas globales (mandan sobre todo)
├── proyectos/
│   └── <nombre>/         # una carpeta por proyecto
│       └── <nombre>.md   # Pendientes primero, luego Contexto/Decisiones/Enlaces
```

## Memoria persistente (auto-memoria de Claude Code)

Claude Code guarda hechos estables en archivos de memoria propios. Reglas:

- Guarda solo lo **no derivable del codigo ni del git**: preferencias del usuario,
  decisiones de negocio, contexto de proyecto que no vive en el repo.
- Un hecho por archivo, con frontmatter y un `MEMORY.md` como indice de una linea.
- Convierte fechas relativas a absolutas ("la semana pasada" -> fecha concreta).
- Antes de guardar, revisa si ya existe una nota que lo cubra: actualiza, no dupliques.
- **El vault manda sobre la auto-memoria.** Si algo esta en el vault, no lo repitas
  como memoria; apunta al vault.

## Que NO hacer

- No inventes datos ni reglas para "que funcione": si falta un dato, pidelo o dejalo vacio.
- No metas informacion personal del usuario en este skill ni en el plugin.
- No asumas que hace un proyecto por su nombre: explora la estructura real.
