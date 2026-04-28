# /actualizar-carta — Cambios en la carta de cualquier cliente

**Cliente:** cualquiera
**Frecuencia:** ad-hoc, según petición de Bea o del cliente final
**Modo:** depende del tipo de cambio

---

## Tipos de cambio y modo de publicación

| Acción | Modo |
|---|---|
| Añadir un plato nuevo | **Borrador** |
| Quitar un plato | **Directo** (tras verificar que no se enlaza desde otro sitio) |
| Cambiar precio | **Directo** (con log) |
| Cambiar descripción | Borrador si es reescritura importante, directo si es corrección menor |
| Añadir/quitar sección entera de carta | **Borrador** |

---

## Input esperado

- [ ] Qué cambio (añadir/quitar/modificar)
- [ ] Qué plato(s)
- [ ] Qué cliente y en qué página(s)
- [ ] Si es añadir: foto + ingredientes + precio
- [ ] Si es quitar: nombre exacto para localizar

---

## Pasos

### Para AÑADIR plato

1. **Localiza la página de carta** del cliente vía API REST (`/wp/v2/pages`)
2. **Redacta copy** en tono de la marca (ver `CLAUDE.md` del cliente)
3. **Sube imagen** con alt text descriptivo
4. **Inserta la ficha** en la sección correspondiente
5. **Guarda como borrador**
6. **Entrega instrucciones** a Bea para publicar desde el builder si el layout lo requiere
7. **Log** en roadmap

### Para QUITAR plato

1. **Busca menciones cruzadas**: ¿aparece en la home? ¿En alguna landing de campaña? ¿En un post del blog?
2. Si aparece en otra página, **avisa a Bea** antes de eliminar para decidir qué hacer en cada sitio
3. Elimina la ficha de la carta
4. Verifica que **no se rompe ninguna ancla** (enlaces internos tipo `#margherita-pietta`)
5. Publica directo
6. **Log** en roadmap

### Para CAMBIAR PRECIO

1. Localiza la ficha
2. Actualiza el precio
3. Publica directo
4. **Log** en roadmap con valor antiguo → valor nuevo

### Para MODIFICAR DESCRIPCIÓN

1. Redacta nueva versión en tono de marca
2. Si es reescritura sustancial → borrador
3. Si es corrección de typo o ajuste menor → directo
4. **Log** en roadmap

---

## Checklist SEO post-cambio

- [ ] Alt text en imagen nueva (si aplica)
- [ ] Ningún link roto internamente
- [ ] Meta title y meta description de la página carta no se han visto afectados (si la carta es una página entera, no toca por un plato concreto)
- [ ] Schema `Menu` o `MenuItem` actualizado si el cliente lo tiene implementado

---

## Log estándar en roadmap

```
- [YYYY-MM-DD] Carta [cliente]: añadido/quitado/modificado "[nombre plato]" · [directo/borrador]
```
