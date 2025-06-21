# TP Integrador - Computación Aplicada

Este repositorio contiene la entrega del Trabajo Práctico Integrador realizado sobre una máquina virtual con Debian.

---

## Integrantes

- Cesar Torrico  
- Juan Nicolás Su  
- Aixa Aylén Ugartemendia  
- Kimberly Tirado

---

## Contenido

- **Script de backup:** `/opt/scripts/backup_full.sh`
- **Directorios comprimidos:**  
  `root.tar.gz`, `etc.tar.gz`, `opt.tar.gz`, `proc.tar.gz`, `www_dir.tar.gz`, `backup_dir.tar.gz`
- **Automatización de backups con `cron`**
- **Servicios configurados:** Apache, MariaDB, SSH

---

## Topología del sistema

### Sistema base

- VM Debian 11 con IP estática `192.168.1.50`

---

## Servicios

- Apache sirviendo contenido desde `/www_dir`
- MariaDB con base de datos importada desde `/root/db.sql`
- SSH habilitado para acceso remoto (con autenticación por clave pública)

---

## Backups

- **Script principal:** `/opt/scripts/backup_full.sh`
- **Cron programado:**
  - Todos los días a las **00:00** → backup de `/var/log`
  - Lunes, miércoles y viernes a las **23:00** → backup de `/www_dir`

---

## Disco adicional

- Partición de **3 GB** montada en `/www_dir`
- Partición de **6 GB** montada en `/backup_dir`

---

## Red

- Configuración de red estática definida en `/etc/network/interfaces`
