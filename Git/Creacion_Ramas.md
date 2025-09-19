
## Ramas en Git

Las ramas permiten trabajar en diferentes versiones del proyecto de forma independiente.

### Ver ramas existentes
```bash
git branch
```
Muestra todas las ramas locales. Para ver también las remotas:
```bash
git branch -a
```

### Crear una nueva rama
```bash
git branch nombre-rama
```
Crea una rama llamada `nombre-rama`.

### Cambiar de rama
Si la rama ya existe localmente:
```bash
git checkout nombre-rama
```
o con el comando clásico:
```bash
git checkout nombre-rama
```
Te mueve a la rama indicada. En versiones recientes de Git también puedes usar:
```bash
git switch nombre-rama
```
Si la rama solo existe en remoto (GitHub) y no en local:
```bash
git fetch origin
git switch -c nombre-de-la-rama origin/nombre-de-la-rama
```

### Fusionar ramas
```bash
git merge nombre-rama
```
Fusiona la rama `nombre-rama` en la rama actual.

### Eliminar una rama
```bash
git branch -d nombre-rama
```
Elimina la rama local. Para eliminar una rama remota:
```bash
git push origin --delete nombre-rama
```

## Repositorio remoto

```bash
git remote -v             # Ver remotos
git clone URL             # Clonar repositorio
git push                  # Subir cambios
git pull                  # Descargar cambios       
```

## Ayuda de comandos

```bash
git help
```
