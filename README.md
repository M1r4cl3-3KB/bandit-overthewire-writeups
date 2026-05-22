# 🛡️ OverTheWire: Bandit Solutions & Write-ups

¡Bienvenido a mi repositorio de documentación para los laboratorios de **Bandit (OverTheWire)**! Este proyecto nació con el objetivo de consolidar y demostrar mis habilidades prácticas en la administración, auditoría y aseguramiento de sistemas operativos basados en **Linux**, utilizando mi entorno personalizado en **Arch Linux**.

En lugar de solo almacenar contraseñas, cada nivel cuenta con una guía detallada paso a paso, explicando el *por qué* de cada comando y el concepto de seguridad subyacente.

---

## 🎯 ¿Qué demuestro en este Repositorio?

A través de la resolución de estos 33 niveles, pongo en práctica conceptos fundamentales que aplican directamente al trabajo diario en un **SOC (Centro de Operaciones de Seguridad)** y **NOC (Centro de Operaciones de Red)**:

*   **Principio de Menor Privilegio & Permisos:** Manipulación avanzada de permisos estándar (`chmod`, `chown`), análisis de bits especiales (`SUID`, `SGID`) y evasión de restricciones de shell.
*   **Análisis de Archivos y Forense Básico:** Filtrado masivo de texto e inspección de strings (`grep`, `awk`, `sed`, `strings`, `cut`), localización de archivos ocultos por atributos específicos (`find`) y análisis de metadatos/tipos de datos (`file`).
*   **Criptografía y Conectividad Segura:** Uso avanzado de SSH, intercambio de llaves públicas/privadas, transferencia segura de archivos y encadenamiento de comandos remotos.
*   **Redes y Sockets:** Interacción directa con puertos de red locales y remotos utilizando herramientas de diagnóstico esenciales (`nc`, `telnet`, `openssl s_client`, `nmap`).
*   **Compresión y Ofuscación:** Desempaquetado y descompresión de archivos multi-capa (`tar`, `gzip`, `bzip2`, `xxd`).

---

## 🗺️ Índice Interactivo de Niveles

Cada enlace te llevará a la documentación detallada del nivel, los comandos utilizados, la explicación del reto y la captura de pantalla de mi terminal en Arch Linux:

### 📁 Bloque Inicial (Fundamentos de Consola y Permisos)
*   [Nivel 00 al 05](./nivel01.md) *<!-- Ajusta los nombres de tus archivos según cómo los guardaste -->*
*   [Nivel 05 al 10](./nivel05.md)
*   [Nivel 10 al 15](./nivel06.md)

### 📁 Bloque Intermedio (Criptografía, Sockets y Redes)
*   [Nivel 16 al 20](./nivel16.md)
*   [Nivel 21 al 25](./nivel21.md)

### 📁 Bloque Avanzado (Evasión de Shells y Lógica de Programación)
*   [Nivel 26 al 30](./nivel26.md)
*   [Nivel 31 al 33](./nivel31.md)

---

## 🛠️ Mi Entorno de Trabajo
Toda la resolución, automatización de scripts y auditoría de estos niveles fue ejecutada localmente desde mi máquina principal configurada con:
*   **OS:** Arch Linux (Instalación minimalista CLI)
*   **WM:** bspwm (Gestor de ventanas optimizado por atajos de teclado)
*   **Terminal:** Kitty
