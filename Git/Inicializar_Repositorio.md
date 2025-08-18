## Clonar un repositorio desde remoto

Si quieres obtener una copia de un repositorio existente (por ejemplo, desde GitHub), utiliza el comando:

```bash
git clone URL-del-repositorio
```

Esto descargará todo el historial y archivos del proyecto en una nueva carpeta.

## Ver el estado del proyecto en local

Para ver los archivos modificados, agregados o eliminados en tu proyecto local, usa:

```bash
git status
```

Este comando te muestra el estado actual de tu repositorio y te ayuda a saber qué archivos están listos para ser guardados (commit) o si hay cambios sin registrar.

## Inicializar un repositorio local con Git

Para comenzar a usar Git en un proyecto existente, debes inicializar un repositorio en la carpeta del proyecto. Esto crea una carpeta oculta llamada `.git` donde se almacenará toda la información de control de versiones.

```bash
git init
```

Después de ejecutar este comando, tu carpeta estará lista para empezar a rastrear cambios con Git.
