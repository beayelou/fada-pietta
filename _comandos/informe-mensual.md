# /informe-mensual — Generación de informe PDF mensual

**Cliente:** uno por informe (no se mezclan marcas)
**Frecuencia:** mensual, en los primeros 5 días del mes siguiente
**Output:** PDF en castellano, 3–5 páginas, en `[cliente]/informes/YYYY-MM-informe.pdf`

---

## Input esperado (fase inicial — extracción manual)

De Bea:
- [ ] **CSV export de GA4** del mes completo (métricas principales)
- [ ] **CSV export de Search Console** del mes (Queries, Pages, Countries)
- [ ] Notas puntuales si las hay (ej. campañas activas, incidencias)

De `[cliente]/roadmap.md`:
- Trabajo realizado en el mes (sección "Hecho")
- Acciones pendientes priorizadas (sección "Pendiente")

## Input esperado (fase 2 — extracción automática)

Cuando estén configurados los accesos OAuth:
- GA4 Data API
- Search Console API

El agente extraerá los datos directamente y generará el informe sin pasar por Bea.

---

## Estructura del informe (ver `_templates/informe-mensual.md`)

### Portada
- Logo del cliente (si disponible en `assets/`)
- Título: "Informe mensual · [Mes Año]"
- Cliente
- Autor: YELOU Ocean

### 1. Resumen ejecutivo (media página)
3–4 líneas: qué se ha hecho, qué ha funcionado, qué viene.

**Tono:** directo, conclusivo, ejecutivo. El cliente lee esto y ya tiene el pulso del mes.

### 2. Trabajo realizado (1 página)
Lista de acciones del mes, con fecha y resultado si aplica.
Formato tabla:

| Fecha | Acción | Resultado / estado |
|---|---|---|
| 2026-01-03 | Actualización pasta y pizza del mes | Publicado |
| 2026-01-12 | Landing "San Valentín" | Publicada, 45 visitas primeras 48h |

### 3. Métricas clave (1 página)

**Tabla comparativa vs mes anterior:**

| Métrica | Mes actual | Mes anterior | Variación |
|---|---|---|---|
| Usuarios únicos | | | |
| Sesiones | | | |
| Páginas/sesión | | | |
| Duración media de sesión | | | |
| Tráfico orgánico (sesiones) | | | |

**Top 5 páginas más vistas** (tabla sencilla).

**SEO — Search Console:**

| Métrica | Mes actual | Mes anterior | Variación |
|---|---|---|---|
| Clicks orgánicos | | | |
| Impresiones | | | |
| CTR medio | | | |
| Posición media | | | |

**Top 5 queries que traen tráfico** (tabla con query, clicks, impresiones, CTR, posición).

**Conversiones clave (según cliente):**
- Pietta: clicks a WhatsApp, clicks a "cómo llegar", clicks a plataformas delivery
- Burbu: reservas, clicks a delivery
- Solasta: envíos de formulario de contacto
- Epicureum: clicks a WhatsApp reservas, clicks a "cómo llegar"
- Gigi: reservas online, clicks a WhatsApp

### 4. Qué ha funcionado y qué no (media página)

2–3 insights breves. Un párrafo cada uno. Ejemplos:

- **Funciona:** la landing de delivery ha subido a top 3 en "pizza a domicilio Granada Zaidín" — impulso directo en pedidos.
- **No funciona:** la página de reservas tiene un 68% de rebote — se recomienda revisar CTA y tiempo de carga.
- **Atención:** la keyword "brunch Granada" ha caído 2 posiciones — revisar si hay competidor nuevo.

**Cero paja. Insights accionables.**

### 5. Roadmap del próximo mes (media página)

Lista priorizada (alta / media / baja) extraída de `roadmap.md` + propuestas nuevas derivadas de los insights del mes.

Formato:

```
🔴 ALTA
- [acción] — justificación breve

🟡 MEDIA
- [acción]

🟢 BAJA
- [acción]
```

---

## Generación del PDF

Tecnología: **Python + ReportLab o WeasyPrint** (Bea ya usa estos stacks en su operativa).

- Hoja A4, márgenes 2 cm
- Tipografía limpia (sans-serif: Inter, Open Sans, o la de la marca si está disponible)
- Color de acento según marca (extraer del logo/CLAUDE.md si está documentado)
- Sin gráficos innecesarios — tablas claras, algún sparkline si aporta
- Logo del cliente en cabecera

**El PDF debe poder leerse en móvil.** Nada de tablas que se rompan.

---

## Nombrado y archivado

- **Nombre:** `YYYY-MM-informe.pdf` (ej. `2026-01-informe.pdf`)
- **Ubicación:** `[cliente]/informes/`
- **Versión editable:** también generar `.md` origen en la misma carpeta por si Bea quiere ajustar algo antes de enviar

---

## Entrega a Bea

```
Informe mensual [cliente] [Mes Año] listo.

Resumen: [3 líneas clave]

Documento: [cliente]/informes/YYYY-MM-informe.pdf

Destacados del mes:
- [insight 1]
- [insight 2]

Priorización propuesta para [mes siguiente]:
1. [acción alta]
2. [acción alta]
3. [acción media]
```

---

## Log estándar

```
- [YYYY-MM-DD] Informe mensual [Mes] generado · [cliente]
```
