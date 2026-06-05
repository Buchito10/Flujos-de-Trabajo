# Reporte de practica: Flujos de trabajo

## 1. Uso guiado de IA y comprension

GitHub Flow ayuda a evitar que el equipo trabaje directamente sobre `main` porque cada cambio se desarrolla en una rama independiente. De esta forma, los modulos pueden revisarse antes de integrarse y los errores quedan aislados hasta que el equipo valide que el cambio funciona.

Las ramas temporales tambien hacen mas claro quien trabaja en cada requerimiento. Si una rama se llama `feature/header`, el equipo sabe que esos cambios pertenecen al encabezado. Esto reduce confusiones y facilita detectar conflictos antes de afectar la version principal del proyecto.

## 2. Estandar de trabajo del equipo

### Nomenclatura de ramas

- `feature/`: para nuevos modulos o caracteristicas. Ejemplos: `feature/header`, `feature/footer`, `feature/catalogo`.
- `fix/`: para correcciones de errores. Ejemplos: `fix/alineacion-imagenes`, `fix/color-navbar`.
- `docs/`: para documentacion o cambios de texto. Ejemplos: `docs/reporte-practica`, `docs/protocolo-conflictos`.

### Flujo de revision en parejas

Ningun integrante puede hacer merge de su propia rama a `main`. Cada Pull Request debe ser revisado por al menos un companero del equipo, quien debe verificar el cambio en la interfaz de GitHub/GitLab y dejar un comentario de aprobacion antes de combinar.

## 3. Protocolo ante un merge conflict

1. Leer el aviso de conflicto en GitHub/GitLab.
2. Descargar los cambios mas recientes de `main` en la computadora local.
3. Cambiarse a la rama con conflicto.
4. Ejecutar `git merge main` o `git pull origin main`.
5. Abrir los archivos marcados con conflicto.
6. Identificar las marcas:

```text
<<<<<<< HEAD
(Codigo actual de la rama donde estamos)
=======
(Codigo que viene de la otra rama)
>>>>>>> nombre-de-la-rama
```

7. Dialogar con el companero para decidir que codigo conservar.
8. Eliminar las marcas `<<<<<<<`, `=======` y `>>>>>>>`.
9. Guardar el archivo corregido.
10. Confirmar la solucion con `git add .` y `git commit -m "Resuelve conflicto de estilos"`.
11. Subir la rama con `git push`.
12. Regresar al Pull Request y completar el merge cuando la plataforma lo permita.

## 4. Evidencia visual del conflicto

Agregar aqui la captura de pantalla donde GitHub/GitLab indique que el Pull Request no puede combinarse automaticamente por conflicto.

## 5. Evidencia de solucion

Agregar aqui la captura del historial del repositorio, Network Graph o lista de commits donde se vea que la rama fue integrada correctamente despues de resolver el conflicto.

## 6. Enlace del repositorio

Pegar aqui el enlace publico del repositorio usado por el equipo:

`https://github.com/usuario/repositorio`
