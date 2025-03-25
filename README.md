# Escenarios de redes de distribución de contenidos
## Descripción
El objetivo de este mini-proyecto es desarrollar un escenario de red de distribución de contenidos (CDN) basado en proyectos como Apache Traffic Control y Apache Traffic Server. El escenario de red deberá desplegarse utilizando la herramienta de virtualización Virtual Networks over Linux (VNX). Como resultado del proyecto se espera un escenario que permita analizar el plano de control de una CDN.

## Diseño del escenario
![Diagrama del Escenario](escenario_Red.drawio.png)

## Funcionamiento
### 1. Clonar el repositorio y levantar el escenario

```
git clone https://github.com/phernandez024/MPRO-CDN
```
```
cd MPRO-CDN
sudo vnx -f scenario.xml --create
```
### 2. Instalar ATS en la imagen VNX

- Parar los escenarios VNX.
- Arrancar la imagen en modo directo con:

```
vnx --modify-rootfs /usr/share/vnx/filesystems/vnx_rootfs_lxc_ubuntu64-20.04-v025-vnxlab/
```

- Instalamos ATS
  
```
sudo apt update
sudo apt install trafficserver
halt -p
```

### Profesor: Carlos M. Lentisco Sánchez

