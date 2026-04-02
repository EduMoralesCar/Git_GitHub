
## Fusionar commits y ramas en Git

En Git, fusionar (merge) se refiere a combinar los cambios de una rama en otra. Esto suele ocurrir cuando trabajas en ramas diferentes y quieres unir el trabajo.

### Fusionar una rama en la rama actual
```bash
git merge nombre-rama
```
Esto traerá los cambios de `nombre-rama` a la rama donde estás.

### ¿Qué pasa si hay conflictos?
Si los mismos archivos fueron modificados en ambas ramas, Git te pedirá que resuelvas los conflictos manualmente. Los archivos en conflicto mostrarán marcas como:

```text
Cambios en la rama que se fusiona
```
Edita el archivo para dejar solo la versión que deseas, guarda y luego ejecuta:
```bash
git add archivo-en-conflicto
git commit
```

### Fusionar commits (squash)
Si quieres combinar varios commits en uno solo (por ejemplo, antes de subir a remoto), puedes usar:

```bash
git rebase -i HEAD~3
```
Por ejemplo, si quieres combinar los últimos 3 commits en uno solo. Al ejecutar el comando, se abrirá un editor con una lista como esta:

```
pick a1b2c3 Primer commit
pick d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```
Cambia `pick` por `squash` en los commits que quieres fusionar:

```
pick a1b2c3 Primer commit
squash d4e5f6 Segundo commit
squash g7h8i9 Tercer commit
```
Guarda y el editor te permitirá escribir el nuevo mensaje para el commit combinado.

> Nota: El uso de squash y rebase modifica el historial, úsalo solo en ramas que no estén compartidas con otros colaboradores.
