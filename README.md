# FutbolWebApp

Aplicación web móvil desarrollada en **DataFlex 25.0** y conectada a **MySQL 8.4** (esquema `futbol`) para la gestión de ligas, equipos, entrenadores, jugadores y posiciones.

## Módulos y vistas

| Entidad | Vistas | Descripción |
| :--- | :--- | :--- |
| **Ligas** | `Selectliga` / `Zoomliga` | Gestión de ligas y consulta de sus equipos asociados |
| **Equipos** | `Selectequipo` / `Zoomequipo` | Alta/edición de equipos con selección de liga |
| **Entrenadores** | `Selectentrenador` / `Zoomentrenador` | Ficha de entrenadores vinculados a un equipo |
| **Jugadores** | `Selectjugador` / `Zoomjugador` | Ficha de jugadores, equipo y acceso a posiciones |
| **Posiciones** | `Selectposicion` / `Zoomposicion` | Catálogo de posiciones en el campo |

El acceso principal se realiza desde `Dashboard.wo` mediante tarjetas para cada entidad.

## Navegación implementada

- **Desde listas (`Select*`)**: apertura del formulario `Zoom` correspondiente en modo solo lectura y sincronización de título y migas de pan (*breadcrumb*).
- **Padre → Hijo**: desde `Zoomliga` se muestra el listado filtrado de equipos de la liga y el acceso directo al detalle.
- **Hijo → Padre**: botón de búsqueda (*prompt*) en `Zoomequipo` (liga) y en `Zoomentrenador` / `Zoomjugador` (equipo).
- **Relación N:M (`jugadorposicion`)**: navegación `Undefined` desde `Zoomjugador` hacia `Selectposicion`.

## Requisitos y puesta en marcha

- **DataFlex 25.0** (Web Application Server).
- **MySQL 8.4** con la base de datos `futbol` importada y conector **MySQL ODBC 8.4**.

1. Configurar el origen ODBC `futbol` y comprobar la cadena en `Data/DFConnId.ini`.
2. Abrir `FutbolWebApp.sws` en DataFlex 25.0 Studio.
3. Compilar `WebApp.src` y ejecutar la aplicación web.