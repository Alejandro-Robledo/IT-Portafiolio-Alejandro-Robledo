# 02 - Rutas, archivos y directorios

## Objetivo

Aprender a navegar por el sistema de archivos Linux y administrar archivos y directorios desde la terminal Bash, utilizando rutas absolutas y relativas.

## Entorno

- Sistema operativo: AlmaLinux 9.9.
- Usuario: `vagrant`.
- Máquina virtual: `RHCSA-server-lab-new`.
- Directorio de trabajo: `/home/vagrant/practicas-rutas`.

## 1. Navegación entre directorios

Comandos utilizados:

| Comando | Función |
|---|---|
| `pwd` | Muestra el directorio actual. |
| `ls` | Lista archivos y directorios. |
| `ls -l` | Muestra información detallada. |
| `ls -la` | Incluye archivos ocultos. |
| `cd /ruta` | Accede a una ubicación. |
| `cd ..` | Sube al directorio padre. |
| `cd ~` | Regresa al directorio personal. |

## 2. Rutas absolutas y relativas

**Ruta absoluta:** comienza desde el directorio raíz `/`.

Ejemplo:

```bash
cd /home/vagrant/practicas-rutas/descargas
```

**Ruta relativa:** se interpreta desde el directorio actual.

Ejemplo:

```bash
cd ../../../../../../descargas
```

El operador `..` representa el directorio padre y permite subir un nivel en la jerarquía.

## 3. Creación de archivos y directorios

Comandos practicados:

```bash
mkdir practica
mkdir -p proyectos/linux/administracion
touch informe1.txt
echo "Mi primer archivo de Linux" > informe1.txt
cat informe1.txt
```

- `mkdir`: crea directorios.
- `mkdir -p`: crea estructuras de directorios.
- `touch`: crea archivos vacíos.
- `echo`: genera texto.
- `>`: redirige la salida y reemplaza el contenido del archivo.
- `cat`: muestra el contenido.

## 4. Copia y renombrado

```bash
cp archivo.txt /ruta/destino/
mv archivo.txt archivo-final.txt
```

También se practicó copiar un archivo y asignarle otro nombre en una misma operación:

```bash
cp origen.txt destino/archivo-copia.txt
```

Se verificaron los resultados utilizando `ls -l`.

## 5. Estructura de directorios utilizada

Durante los ejercicios se creó y utilizó la siguiente estructura:

```text
practicas-rutas/
├── descargas/
│   ├── informe-final.txt
│   ├── router-backup.txt
│   └── switch-backup.txt
├── documentos/
│   └── informes/
│       ├── informe1.txt
│       └── practicas-rutas/
│           └── proyectos/
│               └── redes/
│                   └── configuracion/
│                       ├── router.txt
│                       └── switch.txt
└── proyectos/
    └── linux/
        └── administracion/
```

## 6. Verificación

Se utilizaron los comandos `pwd`, `ls`, `ls -l` y `tree` para comprobar las ubicaciones, archivos y directorios creados.

## Conocimientos adquiridos

- Navegación por el sistema de archivos.
- Diferencias entre rutas absolutas y relativas.
- Creación de directorios y archivos.
- Visualización de contenido.
- Copia y renombrado de archivos.
- Verificación de resultados desde Bash.

## Evidencias

Las capturas de pantalla se incorporarán una vez seleccionadas y verificadas desde el laboratorio.

---

**Estado:** Completado.
