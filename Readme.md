# TP Integrador - Computación Aplicada

Este repositorio contiene la entrega del Trabajo Práctico Integrador realizado sobre una VM Debian.

## Integrantes

- Cesar Torrico
- Juan Nicolás Su
- axi
- kimberly Tirado

## Contenido

- Script de backup: `/opt/scripts/backup_full.sh`
- Directorios comprimidos: `root.tar.gz`, `etc.tar.gz`, etc.
- Automatización de backups con `cron`
- Servicios configurados: Apache, MariaDB, SSH

## Cómo probar

1. Ejecutar el script:
   ```bash
   ./backup_full.sh /var/log /backup_dir
   ```
