# /duplicar-pagina-campana — Nueva landing de campaña puntual

**Cliente:** cualquiera
**Uso:** campañas puntuales (San Valentín, Navidad, promoción de delivery, menú degustación, eventos privados…)
**Modo:** Borrador — Bea revisa y publica

---

## Input esperado

- [ ] Cliente
- [ ] Nombre de la campaña
- [ ] Keyword objetivo (intención de búsqueda)
- [ ] Fecha de inicio y fin de la campaña
- [ ] Página existente a duplicar como base (opcional pero recomendado)
- [ ] Imágenes y creatividades
- [ ] Oferta/propuesta concreta de la campaña

---

## Pasos

### 1. Definir URL

Estructura recomendada:

- Pietta: `pietta.es/campana/[slug]/` o `pietta.es/[slug]/` si es recurrente
- Grupo Fadá: igual — `[dominio]/[slug]/`

**El slug:**
- Corto (máx 4–5 palabras)
- Con la keyword principal
- Sin stopwords innecesarias
- Ej: `san-valentin-2026` o `menu-pasta-domicilio`

### 2. Duplicar página base

- Vía API REST: crear nueva página clonando el contenido de la base
- Si el layout es Elementor/Bricks → **entregar a Bea las instrucciones** de cómo duplicar desde el builder (ambos tienen funcionalidad de duplicado nativa o vía plugin)
- Estado inicial: **borrador**

### 3. Reescribir contenido

- **H1** con keyword objetivo natural
- **Copy** en tono de la marca (consultar `CLAUDE.md` del cliente)
- **Estructura H2/H3** lógica, con keywords long-tail
- **CTAs claros** (reservar, llamar, WhatsApp, pedir online)
- **Prueba social** cuando aporte (reseñas, menciones)

### 4. SEO técnico

- **Meta title:** 50–60 car., keyword al inicio, marca al final
- **Meta description:** 140–160 car., propuesta de valor + fechas + CTA
- **Focus keyword** configurada en Rank Math / SEO Framework
- **Alt text** en todas las imágenes
- **Enlazado interno:** mínimo 2 enlaces a páginas relevantes del propio sitio (home, carta, reservar)
- **Schema** `Event` u `Offer` si aplica a la campaña (navideña, San Valentín, promoción)

### 5. Entregar a Bea

Mensaje tipo:

```
Landing de [campaña] lista en borrador.

URL: [dominio]/[slug]/
Meta title: [x]
Meta description: [x]
Focus keyword: [x]

Review en preview: [link preview]

Pendiente de ti:
- Revisar copy y fotos
- Si todo OK → publicar

Bloque SEO (si quieres cambiarlo): 
[title / description / keyword]
```

### 6. Plan de fin de campaña

En el **momento de crear la página** ya dejo apuntado en `roadmap.md` del cliente la fecha de cierre y qué hacer:

```
## Pendiente
- [fecha fin] Gestionar fin de campaña "[nombre]":
  - Si URL tiene tráfico orgánico → 301 a página relevante
  - Si no → añadir `noindex` y retirar del menú
```

Así no se queda una landing huérfana posicionando para nada después de la campaña.

---

## Checklist pre-publicación

- [ ] H1 único con keyword
- [ ] Meta title único en el sitio
- [ ] Meta description única
- [ ] Slug correcto
- [ ] Mínimo 300 palabras de contenido real
- [ ] Alt text en todas las imágenes
- [ ] 2+ enlaces internos
- [ ] CTA visible above the fold y repetido al final
- [ ] Preview en móvil ok
- [ ] Schema si aplica

---

## Log estándar

```
- [YYYY-MM-DD] Landing "[campaña]" creada en borrador · [cliente] · URL: [slug]
```
