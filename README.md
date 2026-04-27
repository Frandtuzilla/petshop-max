# PetShop Max

E-commerce simple de productos para mascotas.
Proyecto evolutivo de 8 semanas que parte de HTML/CSS/JS vanilla y migra a un stack moderno hacia el final.

## Stack previsto

- **Semanas 1 a 6:** HTML5, CSS3 y JavaScript vanilla (sin dependencias).
- **Semanas 7 y 8:** migración a Next.js + React + Tailwind CSS.

## Estado actual

Semana 1 completada.

## Cómo correr

No requiere instalación de dependencias. Podés:

1. Abrir `index.html` directamente en el navegador (doble clic), o
2. Servirlo con una extensión tipo **Live Server** de VS Code para tener auto-reload.

## Estructura

```
petshop-max/
├── index.html
├── styles/
│   └── main.css
├── scripts/
│   └── main.js
├── assets/
├── data/
├── .gitignore
└── README.md
```

## Flujo de trabajo Git

El proyecto sigue un modelo basado en **Git Flow simplificado**, alineado con el calendario de 8 semanas (4 módulos de 2 semanas cada uno).

### Ramas principales

- **`main`** — rama de **producción**. Solo recibe código estable y verificado. Cada merge a `main` representa una versión liberable del proyecto.
- **`develop`** — rama de **integración**. Acumula todas las funcionalidades terminadas que aún no se han liberado a producción.

### Ramas de trabajo

- **`semana-N`** — una rama por cada semana del plan (`semana-1`, `semana-2`, …, `semana-8`). Toda la implementación de la semana se realiza ahí.

### Ciclo semanal

1. Se crea la rama `semana-N` a partir de `develop`.
2. Se trabaja durante la semana sobre esa rama, con commits siguiendo [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, `refactor:`, `style:`, `chore:`).
3. Al cerrar la semana se abre un **Pull Request** de `semana-N` hacia `develop`, se revisa y se mergea.

### Liberación por módulo (cada 2 semanas)

Al cierre de cada módulo (semanas 1-2, 3-4, 5-6, 7-8) se abre un PR de `develop` hacia `main` y se mergea, consolidando una nueva versión estable en producción.

```
                 (semana-1)         (semana-2)
                     │                  │
                     ▼                  ▼
develop  ──●─────────●──────────────────●────────●────►  (cierre módulo 1)
            \                                    │
             \                                   ▼
main     ────●───────────────────────────────────●─────►
```
