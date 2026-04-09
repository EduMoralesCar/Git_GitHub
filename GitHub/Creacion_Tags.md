# Creación de Tags de Versiones en Git/GitHub

Este documento explica **cómo crear tags de versión** y **por qué se usan**.

## ¿Qué es un tag?

Un tag es una etiqueta fija que apunta a un commit específico. Se usa para marcar versiones importantes como `v1.0.0`, `v1.1.0`, `v2.0.0`.

## ¿Por qué usar tags de versión?

- Permiten identificar exactamente qué código salió en una versión.
- Facilitan volver a una versión estable en caso de problemas.
- Ayudan a automatizar despliegues y releases en GitHub Actions.
- Mejoran la colaboración: todos el equipo habla de la misma versión.
- Dan trazabilidad entre cambios, issues y releases.

## Recomendación de formato: SemVer

Usa versionado semántico: `MAJOR.MINOR.PATCH`.

- `MAJOR` (`v2.0.0`): cambios incompatibles con versiones anteriores.
- `MINOR` (`v1.3.0`): nuevas funcionalidades compatibles.
- `PATCH` (`v1.3.2`): correcciones de errores sin romper compatibilidad.

## Tipos de tag

### 1) Tag lightweight

Es una etiqueta simple sin metadatos avanzados.

```bash
git tag v1.0.0
```

Cuándo usarlo:
- Marcado rápido local.

### 2) Tag annotated (recomendado)

Guarda autor, fecha y mensaje. Es el tipo recomendado para versiones oficiales.

```bash
git tag -a v1.0.0 -m "Release v1.0.0"
```

Cuándo usarlo:
- Releases formales en equipo o en producción.

### 3) Tag firmado (opcional)

Firma criptográficamente el tag (GPG) para validar autenticidad.

```bash
git tag -s v1.0.0 -m "Release firmada v1.0.0"
```

Cuándo usarlo:
- Proyectos con requisitos de seguridad o trazabilidad estricta.

## Flujo recomendado paso a paso

### Paso 1: Confirmar rama y estado limpio

```bash
git branch --show-current
git status
```

Por qué:
- Asegura que estás en la rama correcta (normalmente `main` o `master`).
- Evita etiquetar código con cambios sin commit.

### Paso 2: Actualizar rama local

```bash
git pull origin main
```

Por qué:
- Evita crear un tag sobre un commit desactualizado.

### Paso 3: Crear el tag de versión

```bash
git tag -a v1.2.0 -m "Release v1.2.0"
```

Por qué:
- El mensaje deja contexto de la versión.
- El tag annotated es más útil para auditoría e historial.

### Paso 4: Verificar que el tag existe

```bash
git tag
git show v1.2.0
```

Por qué:
- Confirmas que el tag apunta al commit correcto.

### Paso 5: Subir el tag a GitHub

```bash
git push origin v1.2.0
```

Por qué:
- Un tag local no lo ve el equipo hasta que lo publicas en remoto.

Si deseas subir todos los tags locales:

```bash
git push origin --tags
```

## Crear tag sobre un commit anterior

Si necesitas etiquetar un commit viejo:

```bash
git log --oneline
git tag -a v1.1.0 <hash_commit> -m "Release v1.1.0"
git push origin v1.1.0
```

Por qué:
- Permite reconstruir versiones históricas correctamente.

## Corregir un tag creado por error

### Eliminar tag local

```bash
git tag -d v1.2.0
```

### Eliminar tag remoto

```bash
git push origin --delete v1.2.0
```

### Recrear correctamente

```bash
git tag -a v1.2.0 -m "Release v1.2.0 corregida"
git push origin v1.2.0
```

Por qué:
- Los tags deben apuntar al commit correcto para no romper despliegues ni trazabilidad.

## Usar una versión etiquetada

Ver una versión específica:

```bash
git checkout v1.2.0
```

Nota:
- Quedarás en estado `detached HEAD`.
- Si vas a trabajar desde esa versión, crea una rama:

```bash
git checkout -b hotfix/v1.2.1 v1.2.0
```

## Buenas prácticas

- Usa prefijo `v` en todas las versiones (`v1.0.0`, `v1.0.1`).
- Mantén una convención única de nombres en todo el repositorio.
- Crea tags solo sobre commits ya probados.
- Documenta cada tag con release notes en GitHub.
- No reescribas tags ya publicados, salvo emergencia y comunicándolo al equipo.

## Relación con GitHub Releases

Un **Git tag** marca el commit.
Un **GitHub Release** agrega presentación y documentación (notas, binarios, enlaces).

Flujo recomendado:

1. Crear y subir el tag.
2. Ir a GitHub -> Releases -> Draft a new release.
3. Seleccionar el tag.
4. Escribir notas de versión (cambios, fixes, breaking changes).
5. Publicar release.

## Resumen rápido

Comandos mínimos para una versión oficial:

```bash
git pull origin main
git tag -a v1.0.0 -m "Release v1.0.0"
git push origin v1.0.0
```

Con esto tienes una versión identificable, compartida y lista para release en GitHub.


# REFERENCIA
**Link:** [https://youtu.be/bfofdz9vOJU?si=SlEfseCgVRjQ8_AW](https://youtu.be/bfofdz9vOJU?si=SlEfseCgVRjQ8_AW)



