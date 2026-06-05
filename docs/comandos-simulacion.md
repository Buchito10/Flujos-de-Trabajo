# Comandos para la simulacion

Estos pasos se ejecutan despues de crear el repositorio remoto e invitar a los companeros.

## Preparacion inicial

```bash
git init
git add .
git commit -m "Crea base del proyecto"
git branch -M main
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

## Alumno A

```bash
git checkout main
git pull origin main
git checkout -b feature/header
```

Editar la linea 5 de `styles.css`, por ejemplo:

```css
:root { --header-bg: #1d4ed8; }
```

Despues:

```bash
git add styles.css
git commit -m "Actualiza color del header"
git push -u origin feature/header
```

Abrir Pull Request, pedir revision y hacer merge cuando sea aprobado.

## Alumno B

```bash
git checkout main
git pull origin main
git checkout -b feature/hero-section
```

Editar intencionalmente la misma linea 5 de `styles.css`, por ejemplo:

```css
:root { --header-bg: #9333ea; }
```

Despues:

```bash
git add styles.css
git commit -m "Propone color para hero section"
git push -u origin feature/hero-section
```

Abrir Pull Request. Cuando GitHub/GitLab marque conflicto, resolverlo localmente:

```bash
git checkout feature/hero-section
git fetch origin
git merge origin/main
```

Editar `styles.css`, borrar las marcas del conflicto y dejar el valor final acordado. Luego:

```bash
git add styles.css
git commit -m "Resuelve conflicto de color principal"
git push
```

Regresar al Pull Request y terminar el merge.
