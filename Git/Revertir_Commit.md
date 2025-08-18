
## Revertir un commit en Git

Revertir un commit significa deshacer los cambios realizados por ese commit, creando uno nuevo que los revierte.

### 1. Revertir el último commit
```bash
git revert HEAD
```
Esto crea un nuevo commit que deshace los cambios del último commit.

### 2. Revertir un commit específico
Busca el hash del commit con `git log` y luego:
```bash
git revert abc1234
```
Reemplaza `abc1234` por el hash del commit que quieres revertir.

### 3. Revertir varios commits
Puedes revertir varios commits uno por uno:
```bash
git revert abc1234 def5678
```
O usar un rango (desde hasta):
```bash
git revert abc1234^..def5678
```

### 4. ¿Qué pasa si hay conflictos?
Si al revertir hay conflictos, Git te pedirá que los resuelvas manualmente antes de finalizar el commit.

### 5. Diferencia entre revertir y resetear
- `git revert` crea un nuevo commit que deshace los cambios, recomendado para repositorios compartidos.
- `git reset` elimina commits del historial, úsalo solo si no has hecho push o si trabajas solo.
