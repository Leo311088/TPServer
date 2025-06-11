# TPServer
#integrantes GRUPO 4
-LEONARDO HERRERA
-THIAGO NICOLAS ARMAS (sin participación)
-YONATAN EZEQUIEL RODRIGUEZ BENITEZ DO SANTOS (sin participación)
-MATIAS SCHWEITZER (sin participación)

## Explicación del Diagrama Topológico
El diagrama representa la infraestructura implementada durante el desarrollo del Trabajo Práctico Integrador sobre Debian en VirtualBox.

### 1. VirtualBox
- Hipervisor utilizado para virtualizar el sistema Debian.
- Administra CPU, RAM, almacenamiento y red de la VM.

### 2. VM Debian (TPServer)
- Nombre: TPServer
- Sistema operativo: Debian GNU/Linux.
- IP fija: 172.20.10.13

### 3. Servicios configurados en la VM
- **Apache + PHP 7.4**: Servidor web funcionando sobre /www_dir (index.php, logo.png).
- **MariaDB**: Base de datos 'ingenieria' creada y poblada.
- **Script de backup (backup_full.sh)**: Ubicado en /opt/scripts/backup_full.sh.
- **Cron**: Automatiza backups diarios de /var/log y backups de /www_dir los lunes, miércoles y viernes.
- **fstab**: Gestiona el montaje automático de las particiones adicionales.

### 4. Almacenamiento adicional
Se agregó un segundo disco virtual de 10 GB particionado en:

| Partición | Tamaño | Punto de Montaje | Uso |
|-----------|--------|-------------------|-----|
| /dev/sdc1 | 3 GB   | /www_dir          | Archivos web de Apache |
| /dev/sdc2 | 6 GB   | /backup_dir       | Destino de backups |

### 5. Red
- Configuración de red con IP fija 172.20.10.13.
- Acceso a los servicios desde el host físico a través del navegador.


  
