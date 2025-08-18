
## Actualizar un commit en Git

### 1. Modificar el mensaje del último commit
Si solo quieres cambiar el mensaje:
```bash
git commit --amend -m "Nuevo mensaje"
```

### 2. Agregar archivos olvidados al último commit
Si olvidaste agregar archivos antes de hacer commit:
```bash
git add archivo-olvidado.txt
git commit --amend
```
Esto abrirá el editor para modificar el mensaje si lo deseas.

### 3. Reemplazar el último commit completamente
Puedes modificar tanto los archivos como el mensaje:
```bash
git add archivo1 archivo2
git commit --amend -m "Mensaje actualizado"
```

### 4. ¿Y si ya hiciste push?
Si el commit ya fue subido al remoto, deberás forzar el push:
```bash
git push --force
```
> ¡Advertencia! Usar `--force` puede sobrescribir cambios en el remoto y afectar a otros colaboradores. Hazlo solo si trabajas solo o si todos están informados.


### 5. Cambiar el mensaje de un commit anterior
Si necesitas cambiar el mensaje de un commit más antiguo, usa rebase interactivo:


```bash
git rebase -i HEAD~3
```
Por ejemplo, si quieres cambiar el mensaje de los últimos 3 commits. Al ejecutar el comando, se abrirá un editor con una lista como esta:

```
pick a1b2c3 Primer commit
pick d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```
Cambia `pick` por `reword` en el commit que deseas modificar:

```
pick a1b2c3 Primer commit
reword d4e5f6 Segundo commit
pick g7h8i9 Tercer commit
```
Guarda y el editor te pedirá el nuevo mensaje para ese commit.

> Advertencia: Si ya hiciste push de esos commits al remoto y otros han trabajado sobre ellos, cambiar el historial puede causar problemas. Hazlo solo si trabajas solo o sabes cómo resolver conflictos de historial.
