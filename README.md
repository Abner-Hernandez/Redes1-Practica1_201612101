# Topologia de red
La topologia a Utilizar es de tipo estrella la cual cuenta con la siguiente configuracion.

1. Router C3725
   - Conexión Interfaz f0/0 con Switch_1 (8 puertos) en puerto ethernet 0
   - Conexión Interfaz f0/1 con Switch_2 (8 puertos) en puerto ethernet 0
   - Configuración Interfaz f0/0 Dirección de Red 192.168.11.0/24 Dirección 192.168.11.0/24.
   - Configuración Interfaz f0/1 Dirección de Red 192.168.10.0/24 Dirección 192.168.10.0/24
2. Switch_1 8 puertos
   - Conexión puerto ethernet 1 con Maquina Virtual (Tiny_Linux) en puerto ethernet 0
   - Conexión puerto ethernet 2 con VPC (PC2) en puerto ethernet 0
3. Switch_2 8 puertos
   - Conexión puerto ethernet 1 con VPC (PC3) en puerto ethernet 0
   - Conexión puerto ethernet 2 con VPC (PC4) en puerto ethernet 0
4. VPCS
   - PC2 direccion ip 192.168.11.30 mascara subred 255.255.255.0
   - PC3 direccion ip 192.168.10.15 mascara subred 255.255.255.0
   - PC4 direccion ip 192.168.10.30 mascara subred 255.255.255.0
4. Maquina Virtual
   - Tiny_Linux direccion ip 192.168.11.15 mascara subred 255.255.255.0
   
![Network's Topology](Images/topologia.PNG?raw=true "Title")

# Desarrollo Topologia
Herramientas de desarrolo para la topologia
1. Software GNS3 en su version 2.2.12
2. VMware workstation
3. Tiny Linux SO

## Configuración Router C3725
La configuracion interfacez 0/0, 0/1, para esto primero es entrar en el modo configuracion del router para este caso necesitamos uso del comando 'configure terminal' luego pasamos a seleccionar la interfaz con 'interface fastEthernet0/0' luego podemos configurar varios parametros al puerto como es su velocidad, direccion ip entre otros, en este caso configuramos la direccion ip 'ip address 192.168.10.0 255.255.255.0', luego de configurar las dos Fast Ethernet del router podemos verificar dicha configuracion con 'show ip interface brief'

# Glosario
**Topología de red**
Es un mapa físico o lógico que describe el diseño/estructura de una red para intercambiar datos. sea en el plano físico o lógico. El concepto de red puede definirse como conjunto de nodos interconectados. 

**Nodo**
Es el punto en el que una curva se intercepta a sí misma. Lo que un nodo es concretamente depende del tipo de red en cuestión.

**Host**
Es un ordenador que funciona como el punto de inicio y final de las transferencias de datos. Más comunmente descrito como el lugar donde reside un sitio web. Un host de Internet tiene una dirección de Internet única (direción IP) y un nombre de dominio único o nombre de host.

**Router**
Es un dispositivo encargado de gestionar el flujo de datos de una red local o de internet, decidiendo a qué dirección IP va a enviar el paquete de datos, lo cual contribuye a que todas las computadoras que forman parte de la red compartan la misma señal de internet, bien sea a través de cable, ADSL, o Wifi.

**Switch**
Es un dispositivo que permite la conexión de diferentes dispositivos a la red, para que puedan comunicarse entre sí y con otras redes.

**Ethernet**
Es un estándar de redes de área local para computadores, es el encargado de definir las características de cableado y señalización; de nivel físico y los formatos de tramas de datos del nivel de enlace de datos del modelo OSI

**Fast Ethernet**
Es el nombre de una serie de estándares de IEEE de redes Ethernet de 100 Mbps (megabits por segundo). El nombre Ethernet viene del concepto físico de ether. En su momento el prefijo fast se le agregó para diferenciarla de la versión original Ethernet de 10 Mbps.

**Dirección IP**
Es un conjunto de números que identifica, de manera lógica y jerárquica, a una Interfaz en la red (elemento de comunicación/conexión) de un dispositivo (computadora, laptop, teléfono inteligente) que utilice el protocolo, que corresponde al nivel de red del modelo TCP/IP.1.

**VPC**
Es una nube privada que se ubica dentro de una nube pública que le permite aprovechar los beneficios de una red virtualizada, a la vez que utiliza los recursos de la nube pública.

**Máquina virtual**
Es un software que simula un sistema de computación y puede ejecutar programas como si fuese una computadora real.
