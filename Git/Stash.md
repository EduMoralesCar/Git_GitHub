
## ¿Qué es git stash?

`git stash` permite guardar temporalmente los cambios que no has confirmado (commit) para poder cambiar de rama o realizar otras tareas sin perder tu trabajo.

### ¿Para qué sirve?
Sirve para:
- Guardar cambios sin hacer commit.
- Cambiar de rama sin perder el trabajo actual.
- Recuperar los cambios guardados cuando lo necesites.

### ¿Cómo funciona?
Cuando ejecutas:
```bash
git stash
```
Git guarda los cambios en una pila especial y deja tu área de trabajo limpia.

Para ver los stashes guardados:
```bash
git stash list
```

Para recuperar el último stash:
```bash
git stash apply
```
O para eliminarlo después de aplicarlo:
```bash
git stash pop
```

### Ejemplo práctico
Supón que estás trabajando en una nueva funcionalidad, pero necesitas cambiar de rama para corregir un error urgente:

1. Guarda tus cambios:
	```bash
	git stash
	```
2. Cambia de rama y resuelve el error.
3. Vuelve a tu rama original y recupera los cambios:
	```bash
	git stash pop
	```
