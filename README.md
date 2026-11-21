# FutbolWebApp

Proyecto web móvil en DataFlex 25.0 conectado a MySQL 8.4 (base de datos `futbol`).

## Qué incluye
- **Vistas y Dashboard**: `Select` y `Zoom` para `liga`, `posicion`, `equipo`, `entrenador` y `jugador`, con acceso desde `Dashboard.wo`.
- **Navegación**:
  - Navegación desde padre hacia hijos (`Zoomliga` con listado de equipos de la liga).
  - Navegación desde hijo hacia padre mediante prompt en `Zoomequipo`, `Zoomentrenador` y `Zoomjugador`.
  - Navegación `Undefined` desde `Zoomjugador` hacia `Selectposicion` para gestionar `jugadorposicion`.

## Cómo probarlo
1. Importar la base de datos `futbol` en MySQL 8.4.
2. Configurar el origen ODBC `futbol` en `Data/DFConnId.ini`.
3. Abrir `FutbolWebApp.sws` en DataFlex 25.0, compilar y ejecutar.