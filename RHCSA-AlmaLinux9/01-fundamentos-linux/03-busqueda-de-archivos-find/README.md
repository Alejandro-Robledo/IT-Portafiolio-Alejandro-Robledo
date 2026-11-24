# 03 - Búsqueda de archivos y directorios con find

## Objetivo

Aprender a localizar archivos y directorios mediante el comando `find`, utilizando criterios de búsqueda por nombre, tipo de elemento y ubicación.

## Entorno

- Sistema operativo: AlmaLinux 9.9.
- Shell: Bash.
- Directorio de trabajo: `/home/vagrant/practicas-rutas`.

## 1. Búsqueda por nombre exacto

```bash
find . -name "router.txt"
```

Busca un archivo llamado exactamente `router.txt` dentro del directorio actual y sus subdirectorios.

## 2. Búsqueda por extensión

```bash
find . -name "*.txt"
```

El comodín `*` permite encontrar archivos cuyo nombre termina en `.txt`.

## 3. Búsqueda por tipo de elemento

Archivos regulares:

```bash
find . -type f
```

Directorios:

```bash
find . -type d
```

Tipos utilizados:

- `f`: archivo regular.
- `d`: directorio.

## 4. Búsqueda sin distinguir mayúsculas y minúsculas

```bash
find . -iname "ROUTER.TXT"
```

La opción `-iname` permite buscar nombres sin distinguir entre mayúsculas y minúsculas.

## 5. Búsqueda utilizando comodines

```bash
find . -type f -name "*router*"
```

Permite encontrar archivos cuyo nombre contiene la palabra `router`, independientemente de lo que aparezca antes o después.

## 6. Limitar la ubicación de búsqueda

```bash
find ./documentos -type f -name "*.txt"
```

La búsqueda comienza específicamente en `documentos`, evitando recorrer otras ramas de la estructura.

## Resultados verificados

Durante la práctica se localizaron los siguientes archivos:

- `informe1.txt`
- `router.txt`
- `switch.txt`
- `informe-final.txt`
- `router-backup.txt`
- `switch-backup.txt`

También se identificaron los directorios de la estructura mediante `find . -type d`.

## Errores de sintaxis identificados

Durante los ejercicios se detectaron y corrigieron errores relacionados con:

- Separación incorrecta de argumentos.
- Diferencias entre `-type` y `-name`.
- Uso de `-name` frente a `-iname`.
- Interpretación de comodines.

Estos errores permitieron comprender cómo Bash interpreta los argumentos y cómo utilizar los mensajes de error para corregir comandos.

## Conocimientos adquiridos

- Búsqueda recursiva de archivos.
- Identificación de directorios y archivos.
- Búsqueda por nombre y extensión.
- Uso de comodines.
- Restricción de búsquedas a ubicaciones específicas.
- Interpretación de errores de sintaxis.

## Evidencias

Se incorporarán capturas reales de las búsquedas ejecutadas en AlmaLinux 9.

---

**Estado:** Fundamentos completados.
