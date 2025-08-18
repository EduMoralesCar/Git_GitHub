
## Historial y recuperación en Git

### Ver historial detallado
Muestra el historial de commits de forma compacta y visual:
```bash
git log --oneline --graph --all
```

### Recuperar archivos borrados
Si borraste un archivo por error y aún no has hecho commit:
```bash
git checkout nombre_archivo
```
Si ya hiciste commit, busca el commit donde estaba y recupéralo:
```bash
git checkout commit_hash -- nombre_archivo
```

### Recuperar commits perdidos
Si perdiste commits por reset, rebase o errores:
```bash
git reflog
```
Muestra el historial de movimientos y permite recuperar estados anteriores:
```bash
git checkout hash_reflog
```
