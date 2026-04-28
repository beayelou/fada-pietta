# /instagram-feed — Implementación o actualización de feed de Instagram en web

**Clientes objetivo:** todos (Pietta, Burbu, Solasta, Epicureum, Gigi)
**Uso:** integrar el feed de Instagram de cada marca en su web
**Frecuencia:** implementación puntual por cliente + mantenimiento ocasional

---

## Plugin recomendado

**Smash Balloon Social Feed** (versión gratuita suficiente para la mayoría de casos):
- Estándar del mercado, muy compatible con Elementor y Bricks
- Cumple con las últimas políticas de Instagram Graph API
- Configuración simple
- Versión Pro si se requiere moderación avanzada, layouts múltiples o feeds combinados

**Alternativa gratuita:** Spotlight Social Media Feeds (también buena y mantenida).

---

## Requisitos previos

- [ ] Cuenta de Instagram de la marca ha de ser **Business** o **Creator** (ya lo son todas)
- [ ] Acceso a Facebook Business Manager asociado (para conectar via Graph API)
- [ ] Permisos de administrador en WordPress del cliente

---

## Pasos de implementación (primera vez, por cliente)

### 1. Instalar plugin
- WordPress → Plugins → Añadir nuevo → "Smash Balloon Instagram Feed"
- Activar

### 2. Conectar cuenta
- Ajustes → Instagram Feed → Connect an Instagram Account
- Autorizar vía Facebook Business Manager
- Elegir la cuenta de la marca (ej. @burbu.sushi)

### 3. Configurar feed
- **Layout:** Grid (recomendado), 2–3 filas según cliente
- **Número de posts:** 6 o 9 (múltiplos de 3 funcionan mejor visualmente)
- **Columnas:** 3 desktop / 2 tablet / 1 móvil
- **Mostrar likes/comentarios:** off (menos carga visual)
- **Lightbox:** on (para ver posts al clicar sin salir de la web)
- **Botón "Follow on Instagram":** on, con el @ correcto

### 4. Decidir ubicación en la web

Por marca (propuesta, a validar con Bea):

- **Pietta:** bloque en home, al final (antes del footer)
- **Burbu:** bloque en home + en "sushi a domicilio" para prueba social
- **Solasta:** bloque en home y en casos de éxito / galería
- **Epicureum:** bloque en home, reforzando el "ambiente con alma"
- **Gigi:** bloque en home, apoyando el "aesthetic" de la marca

### 5. Insertar en la página

- **Shortcode** nativo del plugin: `[instagram-feed feed=X]`
- Si es Elementor: widget "Shortcode" + pegar
- Si es Bricks: elemento "Shortcode" + pegar
- Configurar margen superior/inferior para integración visual

### 6. Revisar rendimiento

- Instagram Graph API puede añadir peso → verificar con PageSpeed Insights
- Si impacta mucho en LCP, activar lazy loading del feed
- Caché: asegurar que se actualiza cada 1–6h (configuración del plugin)

### 7. Guardar como borrador y entregar a Bea

```
Feed IG implementado en [cliente] (borrador).

Ubicación: [página]
Posts mostrados: [n]
Layout: grid [x] columnas

Preview: [link]

Pendiente:
- Revisar encaje visual
- Publicar
```

---

## Mantenimiento

El feed se auto-actualiza desde Instagram. Solo requiere mantenimiento si:

- Instagram revoca el token (cada ~60 días en versiones antiguas, permanente en las nuevas) → reconectar
- Se cambia el handle de la cuenta
- El plugin requiere actualización

**Revisión recomendada:** trimestral. Incluir en el roadmap.

---

## Log estándar

```
- [YYYY-MM-DD] Feed IG implementado en [cliente] · borrador
- [YYYY-MM-DD] Feed IG publicado en [cliente]
```
