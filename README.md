# San Juan Digital - Flujo de Trabajo

Proyecto de practica para simular un flujo simplificado basado en GitHub Flow.

## Objetivo

Evitar el problema de "pisar codigo" trabajando con ramas temporales por cada caracteristica, revisiones en parejas y resolucion controlada de conflictos antes de integrar cambios a `main`.

## Ramas obligatorias

- `feature/nombre-del-modulo`: nuevas secciones o componentes, por ejemplo `feature/header`, `feature/hero-section` o `feature/catalogo`.
- `fix/descripcion-del-error`: correcciones, por ejemplo `fix/alineacion-imagenes`.
- `docs/tema-documentado`: documentacion o textos, por ejemplo `docs/protocolo-conflictos`.

## Flujo acordado

1. Actualizar `main`: `git checkout main` y `git pull origin main`.
2. Crear una rama semantica: `git checkout -b feature/header`.
3. Hacer cambios pequenos y relacionados con esa caracteristica.
4. Guardar cambios: `git add .` y `git commit -m "Agrega header base"`.
5. Subir la rama: `git push -u origin feature/header`.
6. Abrir un Pull Request hacia `main`.
7. Pedir revision a un companero.
8. Esperar al menos un comentario de aprobacion.
9. Hacer merge solo cuando no existan conflictos.

## Regla de revision

Ningun integrante debe unir su propia rama a `main`. Un companero debe revisar el Pull Request en GitHub o GitLab, comprobar visualmente el cambio y dejar un comentario de aprobacion antes del merge.

## Simulacion del conflicto

El archivo `styles.css` tiene una linea preparada para practicar el conflicto:

```css
:root { --header-bg: #0f766e; }
```

Alumno A debe cambiar esa linea en `feature/header`.

Alumno B debe cambiar la misma linea en `feature/hero-section`.

Cuando la rama de Alumno A se integre primero a `main`, la rama de Alumno B quedara desactualizada y debera resolver el conflicto antes de terminar su Pull Request.
