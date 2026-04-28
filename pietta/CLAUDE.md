# CLAUDE.md — Pietta Restaurante

> **Lee primero el `CLAUDE.md` maestro del repo.** Este archivo complementa ese con el contexto específico de Pietta.

---

## 1. Qué es Pietta

**Pietta · Ristorante Italiano & Pizzería** es un restaurante italiano en Granada especializado en cocina napolitana auténtica y pizza napoletana. Abierto con alma de trattoria familiar, con chef **Gennaro** al frente y un concepto que prioriza la tradición del sur de Italia con pinceladas de innovación.

- **Web:** https://pietta.es (también responde piertta.es)
- **Instagram:** @pietta.ristorante
- **TikTok:** @pietta.ristorante
- **Dirección:** C. Torre de Comares, 1, Local 5, Zaidín, 18008 Granada
- **Zona:** Zaidín, junto al Palacio de Deportes y el Estadio Nuevo Los Cármenes
- **Delivery:** Uber Eats, Just Eat, Glovo + WhatsApp directo

---

## 2. Alma de marca

### Posicionamiento
"La auténtica trattoria napoletana en Granada." Pietta es el italiano de verdad: horno de piedra a la vista, masa de larga fermentación, ingredientes italianos reales, y un ambiente familiar y cálido. No es un italiano genérico — es **napolitano**, y se nota en cada decisión (desde la margherita con guanciale y pecorino hasta la pasta con estofado de carrillera).

### Valores
- **Tradizione** — recetas del sur de Italia respetadas, no reinterpretadas sin sentido
- **Familia** — "queremos que te sientas como en casa"
- **Producto real** — mozzarella, guanciale, pecorino, scamorza ahumada, grana padano… nombres propios, no genéricos
- **Espectáculo discreto** — horno a la vista, pizza hecha delante del cliente
- **Cariño al detalle** — "cada plato pensado con amore"

### Tono de voz
- **Cálido, cercano, pasional.** Como hablaría un italiano que te invita a cenar en casa de su nonna.
- **Mezcla ES + IT natural.** Palabras en italiano cuando aportan autenticidad: *trattoria, amore, tradizione, nonna, antipasti*. Nunca forzado.
- **Orgulloso de la tradición**, pero sin aires. Sabe lo que hace y lo dice con naturalidad.
- **Sensorial.** Habla de texturas, aromas, temperatura, contraste. La pizza no es "buena", es "masa de larga fermentación con scamorza ahumada y un toque de pimienta negra".
- **Nunca:** tono corporativo, superlatives vacíos ("el mejor", "increíble"), marketing-speak.

### Ejemplos de copy de referencia (extraídos de la web actual)
- *"La vera, l'autentica cucina italiana 👨🏻‍🍳"*
- *"Cada uno de los platos de nuestra carta ha sido creado por nuestro chef Gennaro, respetando la tradición de una pizzería napolitana."*
- *"Queremos que te sientas como en casa, en un espacio moderno y acogedor que invite a compartir momentos."*
- *"Una combinación irresistible de mozzarella suave, nata cremosa, porchetta asada y champiñones frescos."*

---

## 3. Público objetivo

- **Primario:** familias y parejas de Granada (30–55) que buscan una cena italiana de calidad, sin pretensiones, con niños bienvenidos.
- **Secundario:** grupos de amigos (25–40) que quieren pizza de verdad + vino, en un ambiente tranquilo.
- **Turistas** que buscan un italiano auténtico en Granada (nicho pero creciente vía Google "restaurantes italianos Granada").
- **Delivery:** público 25–45 del Zaidín y alrededores que pide pizza de calidad a casa.

---

## 4. Keywords y estrategia SEO

### Keywords principales
- restaurante italiano Granada
- pizzería napolitana Granada
- pizza napolitana Granada
- trattoria Granada
- italiano Zaidín
- pasta artesanal Granada

### Long-tail y oportunidades
- pizza a domicilio Granada Zaidín
- dónde comer pizza napoletana en Granada
- restaurante italiano cerca Estadio Los Cármenes
- pasta sin gluten Granada (sí adaptan, está documentado)
- restaurante italiano para familias Granada

### Intención local prioritaria
- "restaurante italiano Granada" → home
- "pizza a domicilio Granada" → página de delivery
- "pizzería napolitana Granada" → home/carta
- Páginas de campaña para búsquedas estacionales/de promoción

### Competencia local a monitorizar
- Otros italianos de Granada en Maps: La Perla Italiana, Tagliatella, Il Profumo, Oliva Mia, Cucina Mia

---

## 5. Stack técnico

- **Builder:** Bricks
- **Plugin SEO:** Rank Math
- **Analytics:** Google Site Kit (GA4 conectado via plugin)
- **Plugin de reservas/delivery:** [PENDIENTE VERIFICAR]
- **Plugin Instagram feed:** a implementar (ver `/instagram-feed`)
- **GA4:** pendiente acceso directo (disponible via Site Kit en el panel WP)
- **Search Console:** pendiente acceso

---

## 6. Operativa recurrente

### 🍕 Pasta y pizza del mes (MENSUAL, día ~1 de cada mes)

**Qué es:** cada mes Pietta destaca una pasta especial y una pizza especial. Estas dos creaciones se muestran en:

1. **Home** — bloque destacado con ambas
2. **Página de carta / menú** — dentro de las secciones correspondientes

**El resto de la carta NO cambia.** Solo se actualiza el plato destacado del mes.

**Input que llega de Pietta:**
- Fotos profesionales editadas
- Creatividades para RRSS
- Nombre del plato y lista de ingredientes

**Output que produce el agente:**
- Copy de la ficha de plato (estilo Pietta: sensorial, mezcla ES+IT, 2–4 frases)
- Alt text SEO-friendly para cada imagen
- Meta update de la home si la keyword del mes lo merece
- Subida a WP (borrador), con instrucciones exactas de dónde reemplazar en la home y en el menú para Bea

**Ver flujo completo en:** `_comandos/pasta-pizza-mes.md`

### 🍽️ Cambios de carta

- Añadir plato: copy + imagen con alt + posición en la carta + update de página
- Quitar plato: localización en la carta, eliminación, verificar que no se enlaza desde otro sitio
- Cambio de precio: directo (sin borrador), se registra en `roadmap.md`

### 📣 Páginas de campaña puntuales

Ejemplo: "Promoción pasta a domicilio", "Cena de San Valentín", "Menú Navidad 2026".

**Flujo resumido:**
1. Duplicar página base con layout similar
2. URL nueva: `pietta.es/campana/[slug-campana]/`
3. Copy específico de campaña (usando tono Pietta)
4. Meta SEO optimizada para la keyword de la campaña
5. Borrador → Bea revisa → Bea publica
6. Registrar en `roadmap.md`
7. Al cerrar campaña: 301 a home o página relevante si la URL tiene tráfico, o `noindex` si no

**Ver flujo completo en:** `_comandos/duplicar-pagina-campana.md`

---

## 7. Contexto adicional útil

- Pietta acepta reservas por WhatsApp — el CTA "reservar" suele dirigir a WhatsApp.
- Tienen **opciones vegetarianas y sin gluten** claramente — mencionar cuando haga sentido SEO (long-tail de alto valor).
- El **horno de piedra** y el **chef Gennaro** son activos de marca. Úsalos en el storytelling.
- **Delivery propio vía WhatsApp** además de Uber/Just Eat/Glovo — diferenciador a destacar.
- **Aparcamiento gratuito** cercano + 2 paradas de metro a 3 min → información útil en páginas locales y schema.

---

## 8. FAQs que ya están resueltas en la web (no reinventar)

- ¿Hacéis a domicilio? Sí (WhatsApp + plataformas).
- ¿Opciones vegetarianas? Sí.
- ¿Sin gluten? Sí, avisar al hacer pedido.
- ¿Eventos / grupos? Sí, por WhatsApp.

---

**Última actualización:** [fecha]
**Pendiente confirmar con Bea:**
- Accesos GA4 + GSC directos (fuera del panel WP)
