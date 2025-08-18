
## Git avanzado

### Alias de comandos
Simplifica comandos frecuentes:
```bash
git config --global alias.co checkout
git config --global alias.st status
```

### Hooks
Automatiza tareas antes/después de commits:
Ubica scripts en la carpeta `.git/hooks/`.

### Submódulos
Incluye otros repositorios dentro de tu proyecto:
```bash
git submodule add URL ruta/
```

### Cherry-pick
Aplica un commit específico de otra rama:
```bash
git cherry-pick hash_commit
```

### Reflog
Recupera commits perdidos:
```bash
git reflog
```

### Firmar commits y tags con GPG
Agrega seguridad y autenticidad:
```bash
git commit -S -m "Mensaje firmado"
git tag -s v1.0 -m "Tag firmado"
```
