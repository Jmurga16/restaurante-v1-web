# Restaurante · Web

Frontend de un sistema de gestión de restaurante: carta de menús, platos, recetas, ingredientes y encargados por categoría.
Consume la API REST de [restaurante-v1-api](https://github.com/Jmurga16/restaurante-v1-api) (.NET Minimal API + SQL Server).

## Qué hace

- **Carta de menús**: lista los menús y despliega los platos de cada uno.
- **Platos**: catálogo con búsqueda y filtro por categoría.
- **Recetas e ingredientes**: cada plato tiene su receta con los ingredientes que usa; los ingredientes se gestionan con cantidad disponible y unidad de medida, en una tabla paginada con formulario modal.
- **Encargados**: responsables asignados a cada categoría.
- **Tema claro y oscuro**.

## Stack

- **Angular 19** (componentes standalone, rutas con *lazy loading*, control flow `@for` / `@if`)
- **TypeScript** · **RxJS** · `HttpClient`
- **Tailwind CSS 4**
- Backend: [restaurante-v1-api](https://github.com/Jmurga16/restaurante-v1-api) en **.NET** con **SQL Server**

## Estructura

```
src/app/
├── global/    # Páginas generales (inicio, 404) y piezas compartidas
├── layout/    # Layout principal y cabecera
└── menu/
    ├── pages/     # carta, plato, receta, ingredientes, encargado
    ├── services/  # Servicios HTTP por entidad (CRUD contra la API)
    └── models/    # Interfaces de dominio
```

## Ejecutar en local

Requiere Node.js 18 o superior y la API corriendo.

```bash
git clone https://github.com/Jmurga16/restaurante-v1-web.git
cd restaurante-v1-web
npm install
npm start
```

La app abre en `http://localhost:4200`. La URL de la API se configura en `src/environments/environment.ts` (`apiUrl`, por defecto `https://localhost:44369`).

## Créditos

Desarrollado por **José Murga** ([josemurga.dev](https://josemurga.dev)), con aportes de Erik Antony en recetas e ingredientes.
