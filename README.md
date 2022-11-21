# Automatically Update Ubuntu 22.04 LTS using Unattended upgrades.

1. Actualización del sistema manualmente para actualizar el caché del índice del paquete APT.

```console
$ sudo apt update
```

2. Install Unattended Upgrades on Ubuntu 22.04

```console
$ sudo apt install unattended-upgrades
```

3. Check Service status

```bash
$ systemctl status unattended-upgrades --no-pager -l
#Para detener.
$ sudo systemctl stop unattended-upgrades
#Para Start.
$ sudo systemctl start unattended-upgrades
```

*****

# Configurar actualizaciones desatendidas en Ubuntu 22.04

- Hay dos archivos de configuración disponibles para personalizar y controlar el funcionamiento de la herramienta de actualizaciones desatendidas.
    - 20auto-upgrades
    - 50unattended-upgrades

## 20auto-upgrades

1. Editar archivo.

```console
$ sudo nano /etc/apt/apt.conf.d/20auto-upgrades
```

2. With the following contents:

```console
APT::Periodic::Update-Package-Lists "1";
APT::Periodic::Unattended-Upgrade "1";
```

## 50unattended-upgrades

1. Editar archivo.

```console
$ sudo nano /etc/apt/apt.conf.d/50unattended-upgrades
```

2. More info -> <https://www.how2shout.com/linux/automatically-update-ubuntu-22-04-lts-using-unattended-upgrades/>