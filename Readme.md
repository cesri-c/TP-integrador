# TP Integrador - Computación Aplicada

Este repositorio contiene la entrega del Trabajo Práctico Integrador realizado sobre una VM Debian.

## Integrantes

- Cesar Torrico
- Juan Nicolás Su
- Aixa Aylén Ugartemendia
- kimberly Tirado

## Contenido

- Script de backup: `/opt/scripts/backup_full.sh`
- Directorios comprimidos: `root.tar.gz`, `etc.tar.gz`, etc.
- Automatización de backups con `cron`
- Servicios configurados: Apache, MariaDB, SSH

## Topología del sistema

- **VM Debian 11** con IP estática `192.168.1.50`
- **Servicios:**
  - Apache sirviendo desde `/www_dir`
  - MariaDB con base importada
  - SSH habilitado para acceso remoto
- **Backup:**
  - Script `/opt/scripts/backup_full.sh`
  - Cron:
    - Todos los días a las 00:00 backup de `/var/log`
    - Lunes, miércoles y viernes a las 23:00 backup de `/www_dir`
- **Disco adicional:**
  - Partición de 3GB montada en `/www_dir`
  - Partición de 6GB montada en `/backup_dir`
- **Red configurada en `/etc/network/interfaces`**
