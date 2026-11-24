# 04 - Filtros, pipelines y redirecciones

## Objetivo

Practicar herramientas de procesamiento de texto en Linux, utilizando filtros, pipelines y redirecciones para buscar información, analizar archivos y almacenar resultados.

## Entorno

- Sistema operativo: AlmaLinux 9
- Entorno virtualizado: VirtualBox y Vagrant
- Usuario de práctica: vagrant
- Archivo de trabajo: `registro.txt`

## Herramientas utilizadas

| Comando / operador | Función |
|---|---|
| `grep` | Buscar patrones de texto. |
| `grep -i` | Buscar sin distinguir mayúsculas y minúsculas. |
| `grep -n` | Mostrar coincidencias con números de línea. |
| `head` | Mostrar las primeras líneas de un archivo. |
| `tail` | Mostrar las últimas líneas de un archivo. |
| `cut` | Extraer campos de texto. |
| `sort` | Ordenar líneas. |
| `uniq -c` | Contar líneas repetidas consecutivamente. |
| `wc -l` | Contar líneas. |
| `\|` | Enviar la salida de un comando al siguiente. |
| `>` | Crear o sobrescribir archivos mediante redirección. |
| `>>` | Agregar contenido al final de un archivo. |

## Prácticas realizadas

### 1. Búsqueda de texto con grep

Se utilizaron diferentes opciones para localizar registros específicos dentro de `registro.txt`.

```bash
grep "ERROR" registro.txt
grep "WARNING" registro.txt
grep "vagrant" registro.txt
grep -i "error" registro.txt
grep -n "ERROR" registro.txt
```

Se comprobó la búsqueda por patrones, la búsqueda sin distinción de mayúsculas y minúsculas y la identificación de números de línea.

### 2. Pipelines

Se combinaron comandos para procesar información de manera consecutiva.

```bash
grep "ERROR" registro.txt | wc -l
grep "ERROR" registro.txt | sort
cat registro.txt | wc -l
```

Se verificó que el archivo contiene tres registros de error y diez líneas en total.

### 3. Redirecciones

Se generó un archivo con los registros de error mediante redirección de salida.

```bash
grep "ERROR" registro.txt > errores.txt
```

Posteriormente, se agregó contenido al archivo sin sobrescribir los datos existentes:

```bash
echo "Registro de prueba" >> errores.txt
```

Se verificó el contenido final mediante `cat`.

### 4. Visualización parcial de archivos

Se utilizaron los siguientes comandos:

```bash
head -n 3 registro.txt
tail -n 3 registro.txt
```

Se visualizaron las primeras y últimas tres líneas del archivo.

### 5. Extracción y procesamiento de campos

Se extrajo el primer campo de cada registro, correspondiente al tipo de mensaje:

```bash
cut -d ' ' -f1 registro.txt
```

Luego se combinaron herramientas para ordenar y contar los registros:

```bash
cut -d ' ' -f1 registro.txt | sort | uniq -c
```

Resultado verificado:

| Tipo de registro | Cantidad |
|---|---:|
| ERROR | 3 |
| INFO | 5 |
| WARNING | 2 |

## Conocimientos adquiridos

- Filtrado de información mediante patrones de texto.
- Uso de opciones de `grep`.
- Visualización parcial de archivos.
- Extracción de campos utilizando delimitadores.
- Ordenamiento y conteo de registros.
- Combinación de comandos mediante pipelines.
- Redirección de salida y almacenamiento de resultados.
- Análisis básico de archivos de registro (logs).

## Evidencias

Se incorporarán capturas de pantalla de las ejecuciones realizadas en el laboratorio.

## Estado

**Completado.**
