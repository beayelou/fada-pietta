# Clientes Web SEO — YELOU Ocean

Repositorio operativo para la gestión de las webs de los clientes de restauración de **YELOU Ocean** (Bea González Moreno). Diseñado para ser el home de trabajo de un agente senior WordPress + SEO operando desde Claude Code.

## Clientes activos

- **Pietta** — restaurante italiano y pizzería napolitana · Granada
- **Grupo Fadá** (4 marcas):
  - **Burbu** — sushi & fusión
  - **Solasta** — catering & eventos
  - **Epicureum** — brunch & café de especialidad
  - **Gigi** — brunch & healthy gluten-free

## Cómo arrancar

1. **Lee `CLAUDE.md`** (raíz) — es la memoria operativa maestra del agente.
2. **Lee el `CLAUDE.md` del cliente** con el que vas a trabajar antes de tocar nada.
3. **Completa `credenciales.md`** del cliente partiendo de `credenciales.md.example`.
4. **Consulta el comando** correspondiente en `_comandos/` para tareas recurrentes.

## Estructura

```
clientes-web-seo/
├── CLAUDE.md                    ← memoria operativa maestra (leer siempre primero)
├── ROADMAP.md                   ← hoja de ruta global
├── _templates/                  ← plantillas reutilizables
├── _comandos/                   ← flujos recurrentes documentados
├── pietta/                      ← Pietta (cliente independiente)
└── grupo-fada/
    ├── CLAUDE.md                ← contexto común del grupo
    ├── burbu/
    ├── solasta/
    ├── epicureum/
    └── gigi/
```

Cada carpeta de cliente contiene:

- `CLAUDE.md` — alma de marca, tono, keywords, stack
- `credenciales.md` — accesos WP, GA4, GSC (no versionado)
- `roadmap.md` — hoja de ruta del cliente
- `carta/` — material relacionado con la carta
- `campanas/` — landings de campaña
- `informes/` — informes mensuales PDF
- `assets/` — imágenes y material visual

## Comandos disponibles

- `/pasta-pizza-mes` — actualización mensual de Pietta
- `/actualizar-carta` — cambios de carta (cualquier cliente)
- `/duplicar-pagina-campana` — nueva landing
- `/informe-mensual` — informe PDF mensual
- `/instagram-feed` — integración del feed de IG

## Principios no negociables

1. Contexto antes que acción.
2. Borrador para contenido nuevo, directo para cambios menores.
3. SEO integrado, no añadido.
4. Una marca, una voz.
5. Log en `roadmap.md` al terminar cualquier tarea.

---

*Operativa diseñada para Bea González Moreno · YELOU Ocean*
