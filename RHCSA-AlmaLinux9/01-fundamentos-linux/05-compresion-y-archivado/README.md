# 05 - Compresión y archivado de archivos

## Objetivo

Practicar la creación, inspección, compresión y extracción de archivos mediante las herramientas `tar`, `gzip`, `zip` y `unzip` en Linux.

## Entorno

- Sistema operativo: AlmaLinux 9
- Entorno virtualizado: VirtualBox y Vagrant
- Usuario de práctica: vagrant
- Directorio de trabajo: `~/practicas-compresion`

## Herramientas utilizadas

| Comando | Función |
|---|---|
| `tar` | Agrupar archivos y directorios en un archivo TAR. |
| `gzip` | Comprimir archivos mediante gzip. |
| `zip` | Crear archivos ZIP comprimidos. |
| `unzip` | Listar y extraer archivos ZIP. |
| `tree` | Visualizar estructuras de directorios. |
| `ls -lh` | Consultar tamaños y detalles de archivos. |
| `cat` | Visualizar el contenido de archivos. |

## Prácticas realizadas

### 1. Preparación del entorno

Se creó una estructura de trabajo con archivos de texto para realizar las pruebas de archivado y compresión.

```bash
mkdir -p ~/practicas-compresion/documentos
```

Se generaron los archivos `servidor.txt` y `rhcsa.txt` dentro del directorio `documentos/`.

### 2. Archivado mediante TAR

Se creó un archivo TAR que contiene el directorio de práctica:

```bash
tar -cvf documentos.tar documentos/
```

Se verificó su contenido mediante:

```bash
tar -tf documentos.tar
```

### 3. Compresión mediante GZIP

Se comprimió el archivo TAR conservando el original:

```bash
gzip -k documentos.tar
```

Se verificó el archivo comprimido y su tamaño mediante:

```bash
ls -lh
gzip -l documentos.tar.gz
```

Se observó una reducción del tamaño del archivo TAR mediante gzip.

### 4. Inspección y extracción de TAR.GZ

Se consultó el contenido del archivo comprimido sin extraerlo:

```bash
tar -tzf documentos.tar.gz
```

Se realizó la extracción en un directorio específico:

```bash
mkdir recuperacion
tar -xvzf documentos.tar.gz -C recuperacion/
```

También se creó `respaldo.tar.gz` utilizando:

```bash
tar -czf respaldo.tar.gz documentos/
```

Se verificó su extracción en otro directorio:

```bash
mkdir recuperacion-respaldo
tar -xvzf respaldo.tar.gz -C recuperacion-respaldo/
```

### 5. Compresión y extracción mediante ZIP

Se creó un archivo ZIP incluyendo recursivamente el directorio de práctica:

```bash
zip -r documentos.zip documentos/
```

Se inspeccionó el contenido sin extraerlo:

```bash
unzip -l documentos.zip
```

Se realizó la extracción en un directorio independiente:

```bash
mkdir recuperacion-zip
unzip documentos.zip -d recuperacion-zip/
```

Finalmente, se verificó la estructura y el contenido de los archivos extraídos.

## Conocimientos adquiridos

- Diferencias entre archivado y compresión.
- Creación y consulta de archivos TAR.
- Compresión mediante GZIP.
- Creación y extracción de archivos TAR.GZ.
- Extracción en directorios específicos utilizando `-C`.
- Creación, inspección y extracción de archivos ZIP.
- Verificación de estructuras y contenidos después de la extracción.
- Comprensión básica de los resultados de compresión.

## Evidencias

Se incorporarán capturas de pantalla de las ejecuciones realizadas en el laboratorio.

## Estado

**Completado.**
