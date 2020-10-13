## 1. Configuracion del adaptador de red (maquina virtual)
como indica en la practica se esttablece una red interna con el nombre DPLnet
!["p1.img1"](img/punto1-img1.png)
!["p1.img1"](img/punto1-img2.png)
## 2. Configuración del adaptador de red en Windows 7.
Menu Inicio -> Panel de control -> Redes e Internet -> Centro de Redes y recursos compartidos -> Conexión de área local 
-> Propiedades -> Protocolo de Internet versión 4
se establece la ip 10.70.21.120 la máscara la cacula sola\
!["p2.img1"](img/punto2-img1.png)
## 3. Configuración del adaptador de red en Ubuntu Server.
- compruebo si esta habilitada la confiuracion de cloud-init con este comando: cat /etc/cloud/cloud.cfg.d/subiquity-disable-cloudinit-networking.cfg
!["p3.img1"](img/punto3-img1.png)
- accedo al archivo yaml de netplan: vim /etc/netplan/00-installer-config.yaml y establezco la siguiente configuracion
!["p3.img2"](img/punto3-img2.png)
- la aplico con sudo netplan apply\
!["p3.img3"](img/punto3-img3.png)
- compruebo que este todo bien configurado con ip add show\
!["p3.img4"](img/punto3-img4.png)
## 4. Comprobación de la configuración y de funcionamiento.
- desde la máqiona windows hago pin a la maquina ubuntu con este resultado.
 
!["p4.img1"](img/punto4-img1.png)
- desde la maquina ubuntu ejecuto png hacia la máquina windows

 !["p4.img2"](img/punto4-img2.png)