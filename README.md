# FutbolWebApp — Sprint 1 (DF1 - Vistas)

Aplicación web móvil en **DataFlex 25.0** conectada a **MySQL 8.4** (`futbol`) siguiendo flujo **Gitflow**.

## Estructura de ramas (Gitflow)
- `main`: versión final entregable.
- `develop`: rama de integración funcional.
- `feature/vista-liga`: vistas Select y Zoom de `liga`.
- `feature/vista-posicion`: vistas Select y Zoom de `posicion`.
- `feature/vista-equipo`: vistas Select y Zoom de `equipo`.
- `feature/vista-entrenador`: vistas Select y Zoom de `entrenador`.
- `feature/vista-jugador`: vistas Select y Zoom de `jugador`.
- `feature/dashboard-tiles`: tarjetas (*tiles*) de acceso en `Dashboard.wo`.

## Puesta en marcha
1. Importar el script de la base de datos `futbol` en MySQL 8.4.
2. Configurar la conexión ODBC (`futbol`) en `Data/DFConnId.ini`.
3. Abrir `FutbolWebApp.sws` en DataFlex 25.0 Studio, compilar y ejecutar (`F5`).
