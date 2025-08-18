
## Rebase interactivo: squash, reword y edit

El rebase interactivo permite modificar el historial de commits usando diferentes opciones:

- **squash:** Fusiona varios commits en uno solo.
- **reword:** Permite cambiar el mensaje de un commit.
- **edit:** Permite modificar el contenido de un commit (archivos o mensaje).

### ¿Cómo usar rebase interactivo?
Ejecuta:
```bash
git rebase -i HEAD~3
```
Esto abrirá un editor con una lista de los últimos 3 commits:

```
pick a1b2c3 Primer commit
pick d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```

#### Ejemplo de uso de squash
Para fusionar los dos últimos commits:
```
pick a1b2c3 Primer commit
squash d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```

#### Ejemplo de uso de reword
Para cambiar el mensaje del segundo commit:
```
pick a1b2c3 Primer commit
reword d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```

#### Ejemplo de uso de edit
Para modificar el contenido del segundo commit:
```
pick a1b2c3 Primer commit
edit d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```
Guarda y sigue las instrucciones en la terminal para editar el commit.

## ¿Qué es git rebase?

`git rebase` es una herramienta que permite mover o combinar una secuencia de commits a una nueva base, normalmente para mantener un historial más limpio y lineal.

### ¿Para qué sirve?
- Actualizar una rama con los cambios de otra sin crear commits de merge.
- Reorganizar o modificar el historial de commits.

### ¿Cómo funciona?
Supón que tienes una rama llamada `feature` y quieres actualizarla con los cambios de `main`:
```bash
git checkout feature
git rebase main
```
Esto mueve los commits de `feature` para que estén encima de los últimos commits de `main`.

### Diferencia entre rebase y merge
- **merge:** Une el historial de dos ramas y crea un commit de merge.
- **rebase:** Reescribe el historial, colocando tus cambios después de los de la otra rama, sin crear commit de merge.

### Ejemplo práctico
1. Estás en la rama `feature` y quieres traer los cambios de `main`:
	```bash
	git rebase main
	```
2. Si hay conflictos, resuélvelos manualmente, luego:
	```bash
	git add archivo-en-conflicto
	git rebase --continue
	```
3. Si necesitas abortar el rebase:
	```bash
	git rebase --abort
	```

> Nota: El rebase modifica el historial. Úsalo solo en ramas que no estén compartidas o si todos los colaboradores están informados.
