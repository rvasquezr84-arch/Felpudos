# CLAUDE.md — Felpudos (repo de contexto multi-marca)

Este repositorio se usa como catálogo web de **Felpudos y Servicios** y, además, como
repositorio de contexto para tres marcas del usuario:

1. **Felpudos y Servicios** — felpudos/pisos comerciales (ver `contexto-marcas/felpudos-y-servicios/`)
2. **Daynite Nutrition** — snacks saludables (ver `contexto-marcas/daynite-nutrition/`)
3. **Marca personal** — streetworkout + box + coaching (ver `contexto-marcas/marca-personal/`)

`brand-kit.md` en la raíz es el resumen ejecutivo de las tres. `contexto-marcas/` guarda
el material fuente completo, organizado por marca en `documentos/` (docx/pdf/pptx
originales) y `capturas/` (imágenes/screenshots), más un `notas.md` con el resumen
estructurado de cada carpeta.

## Regla: "para el repo"

Cuando el usuario adjunte archivo(s) y diga **"para el repo"** (o equivalente: "guarda
esto", "para el contexto"), seguir SIEMPRE este flujo:

1. **Identificar la marca** a la que pertenece el material (Felpudos y Servicios /
   Daynite Nutrition / Marca personal).
   - **Si es ambiguo o no es obvio a qué marca corresponde, o podría aplicar a más de
     una, PREGUNTAR antes de guardar nada.** No asumir.
   - Si es claramente obvio (p. ej. una cotización de felpudos, o una captura de
     Daynite), proceder sin preguntar.
2. Copiar el/los archivo(s) originales a `contexto-marcas/<marca>/documentos/` (o
   `capturas/` si son imágenes), con un nombre de archivo limpio y descriptivo.
3. Extraer la información relevante y **actualizar** (no duplicar) el `notas.md` de esa
   marca: si un dato ya existe, actualizarlo; si es nuevo, agregarlo en la sección que
   corresponda.
4. Si el cambio es relevante para el resumen ejecutivo, reflejarlo también en
   `brand-kit.md`.
5. Hacer commit con mensaje descriptivo y **hacer push a la rama actual automáticamente,
   sin pedir confirmación** — esta sesión corre en un contenedor temporal, así que sin
   push el trabajo se pierde al cerrar la sesión.

## Rama de trabajo

Desarrollar y pushear directo a la rama en curso (no crear una rama nueva por cada
tanda de archivos, salvo que el usuario lo pida).
