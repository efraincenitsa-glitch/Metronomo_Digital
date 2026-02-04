# Metrónomo Digital (PWA)

Metrónomo **completo** que funciona en iPhone y Android y se puede **agregar a pantalla de inicio**. Totalmente **offline** tras la primera carga (Service Worker).

## Características
- BPM 20–300, con controles ±1/±10, edición directa y **Tap Tempo**.
- **Compás** (1–12 tiempos) y **subdivisiones** (x1, x2, x3, x4, x6, x8).
- **Editor de acentos** por tiempo: A (acentuado), • (normal), – (silencio).
- **Voces**: Clásico, Beep, Clave (sintetizado con Web Audio).
- **Péndulo** animado y **LEDs** de tiempos.
- **Volumen** maestro.
- **PWA**: `manifest.webmanifest`, `sw.js`, e **icono 1024** para iOS.

## Uso
1. Publica en **HTTPS** (GitHub Pages, Netlify, Vercel).
2. Abre en **Safari** (iPhone) y toca **Iniciar** para habilitar audio.
3. **Compartir → Agregar a pantalla de inicio**.
4. Desde el icono, funcionará **sin internet**.

## Despliegue en GitHub Pages
- Sube todo el contenido a un repositorio (raíz) y activa **Settings → Pages**.
- Las rutas son **relativas** (`./`), por lo que funciona en repositorios de proyecto.

## Notas técnicas
- Motor de tiempo: programador con **lookahead** y reloj de **Web Audio** para minimizar drift.
- Sonidos 100% locales, sin dependencias externas.
- Guarda preferencias en `localStorage`.
