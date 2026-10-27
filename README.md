# Launcher iOS + One UI

Launcher base para Android (Kotlin + Jetpack Compose) que mezcla:

- **iOS:** iconos con esquinas suaves, dock y tarjetas de vidrio translúcido, páginas con puntos, cajón con desenfoque del fondo (Android 12+).
- **One UI (Samsung):** tarjeta de reloj grande con esquinas de 28dp, cuadrícula de 4 columnas, cajón de apps deslizando hacia arriba, dock con apps de Samsung por defecto.

## Cómo probarlo

1. Abre la carpeta en Android Studio y espera el Gradle Sync.
2. Conecta tu Samsung con depuración USB activada y pulsa Run.
3. Pulsa el botón Inicio: Android te preguntará qué pantalla de inicio usar. Elige "Launcher iOS+One UI" > "Siempre".
4. Para volver al launcher original: Ajustes > Aplicaciones > Apps predeterminadas > Pantalla de inicio.

## Gestos

- Deslizar hacia arriba: abre el cajón de apps.
- Botón Inicio o Atrás: cierra el cajón.
- Deslizar a los lados: cambia de página.
- Mantener pulsada una app: abre su información (desde ahí puedes desinstalarla).

## Dónde cambiar cosas

- `AppRepository.kt`: qué apps van en el dock (`dockPreferences`).
- `HomeScreen.kt`: colores de vidrio (`GlassColor`), radios de esquina, tamaño de iconos, reloj.
- `AppDrawer.kt`: cajón y buscador.
- `MainActivity.kt`: gestos y desenfoque.

## Ideas para seguir

- Guardar la posición de las apps con DataStore o Room.
- Arrastrar y soltar iconos.
- Carpetas.
- Widgets reales con `AppWidgetHost`.
- Botón/gesto para activar tu asistente de voz.
