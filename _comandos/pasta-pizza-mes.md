# /pasta-pizza-mes — Actualización mensual Pietta

**Cliente:** Pietta
**Frecuencia:** mensual (primeros días de cada mes)
**Modo:** Borrador — Bea revisa y publica

---

## Input esperado de Bea

- [ ] Nombre de la pasta del mes
- [ ] Nombre de la pizza del mes
- [ ] Lista de ingredientes (para cada una)
- [ ] Fotos profesionales editadas (1 principal + extras opcionales)
- [ ] Creatividades sociales (por si se quiere reutilizar parte del copy)
- [ ] Mes al que corresponde (ej. "enero 2026")

Si falta alguno, **no arranques**. Pide lo que falte.

---

## Pasos de ejecución

### 1. Copy de ficha de plato

Genera para cada una (pasta + pizza):

- **Nombre del plato** (tal cual llega)
- **Descripción corta** (1 frase, estilo Pietta — sensorial, ingrediente-protagonista)
- **Descripción larga** (2–4 frases, mezcla ES+IT natural, texturas y contrastes)
- **Lista de ingredientes** (formato limpio, con italiano donde aplique: *guanciale*, *pecorino*, etc.)

**Plantilla de referencia:** `_templates/pasta-pizza-mes.md`

### 2. Alt text de las imágenes

- Descriptivo, incluye el plato + "pizza del mes/pasta del mes" + "Pietta Granada"
- Ej: *"Pasta del mes en Pietta Granada: tagliolini con ragú de cordero y pecorino"*
- Nombre de archivo de imagen en slug: `pasta-mes-[nombre-plato]-pietta-YYYY-MM.jpg`

### 3. Meta SEO de las páginas afectadas

**Home** (si el plato del mes tiene keyword fuerte, opcional):
- Revisar si tiene sentido actualizar meta description para incluir el plato estrella
- No cambiar meta title de la home por rotación mensual

**Carta / menú** (pasta o pizza según corresponda):
- Mantener meta estable, no rotar mensualmente

### 4. Subida a WordPress (API REST)

- Subir imágenes a biblioteca de medios con alt text
- Actualizar bloques correspondientes en home y carta
- Estado: **borrador** para que Bea revise
- Si el layout es Elementor/Bricks → entregar a Bea el copy + las instrucciones de reemplazo

### 5. Instrucciones para Bea (modo asistido)

Entregar en un bloque Markdown claro:

```
## Para publicar en Pietta — [mes]

### HOME
1. Ir a Páginas → Home → Editar con [Elementor/Bricks]
2. Localizar sección "Pasta del mes / Pizza del mes"
3. Sustituir:
   - Foto pasta: [ruta a imagen subida]
   - Título: [nombre]
   - Descripción: [descripción corta]
   - Foto pizza: [ruta]
   - Título: [nombre]
   - Descripción: [descripción corta]
4. Guardar como borrador + previsualizar

### CARTA
1. Ir a Páginas → Carta → Editar
2. Sustituir fichas en las secciones correspondientes
3. Guardar como borrador

### Checklist previo a publicar
- [ ] Alt text correctos
- [ ] Sin typos
- [ ] Imágenes con peso < 200 KB (comprimir si no)
- [ ] Preview en móvil
```

### 6. Log en roadmap

Al terminar, añadir entrada en `pietta/roadmap.md`:

```
## Hecho (últimos 30 días)
- [YYYY-MM-DD] Pasta y pizza del mes [mes] publicadas (borrador) · pendiente revisión Bea
```

---

## Timing estimado

- Copy + alt + meta: 20 min
- Subida a WP: 10 min
- Instrucciones a Bea: 5 min

**Total: 35 min por mes.**
