
# Práctica 1.1 — Jerarquía del sistema de archivos Linux

## Objetivo

Reconocer la estructura jerárquica del sistema de archivos Linux, identificar los principales directorios del sistema y practicar comandos básicos de navegación desde la terminal Bash.

## Entorno

- Sistema operativo: AlmaLinux 9.9.
- Máquina virtual: RHCSA-server-lab-new.
- Usuario: vagrant.
- Virtualización: Oracle VirtualBox.
- Aprovisionamiento: Vagrant.

## 1. Identificación del directorio de trabajo

### Comando

```bash
pwd
```

### Resultado

```text
/home/vagrant
```

El comando `pwd` (Print Working Directory) permite identificar el directorio de trabajo actual.

En este ejercicio, la terminal se encontraba en el directorio personal del usuario `vagrant`.

## 2. Visualización de archivos y directorios

### Comandos utilizados

```bash
ls
ls -la
```

El comando `ls` permite listar los elementos de un directorio.

La opción `-a` permite visualizar elementos ocultos, mientras que `-l` muestra información detallada, como permisos, propietarios, tamaño y fecha de modificación.

Durante la exploración se identificaron archivos de configuración del entorno Bash, el directorio `.ssh` y otros archivos ocultos del usuario.

## 3. Exploración de la raíz del sistema

### Comandos utilizados

```bash
ls /
ls -lah /
```

La raíz `/` contiene los directorios principales del sistema Linux.

Durante la exploración se identificaron directorios como:

- `/boot`: archivos relacionados con el arranque.
- `/dev`: archivos de dispositivos.
- `/etc`: configuración del sistema.
- `/home`: directorios personales de usuarios.
- `/root`: directorio personal del superusuario.
- `/usr`: aplicaciones, utilidades y recursos del sistema.
- `/var`: información variable y registros.
- `/proc`: información virtual de procesos y kernel.
- `/sys`: información virtual de dispositivos y kernel.
- `/tmp`: archivos temporales.

## 4. Enlaces simbólicos

Durante la exploración se identificaron los siguientes enlaces simbólicos:

| Enlace | Destino |
|---|---|
| `/bin` | `/usr/bin` |
| `/lib` | `/usr/lib` |
| `/lib64` | `/usr/lib64` |
| `/sbin` | `/usr/sbin` |

Estos enlaces forman parte de la organización del sistema conocida como Usr Merge.

## 5. Visualización de la jerarquía

### Comando

```bash
tree -L 1 /
```

El comando `tree` permite visualizar la jerarquía de directorios.

La opción `-L 1` limita la profundidad de visualización a un nivel.

## 6. Navegación por directorios

Comandos utilizados:

```bash
cd /
cd /etc
cd /home/vagrant
cd ~
cd ..
```

- `cd`: permite cambiar el directorio de trabajo.
- `cd /`: accede a la raíz.
- `cd ~`: accede al directorio personal del usuario.
- `cd ..`: permite subir un nivel en la jerarquía.

## 7. Observaciones

Durante la práctica se reconoció la estructura principal del sistema de archivos Linux, se identificaron archivos ocultos y enlaces simbólicos, y se realizaron ejercicios de navegación por diferentes directorios.

## 8. Conclusión

Esta práctica permitió familiarizarse con la jerarquía de directorios Linux y los comandos esenciales para explorar el sistema desde la terminal.

Comprender la organización del sistema de archivos constituye una base fundamental para continuar con tareas de administración Linux.

---

**Estado:** Completado.
