![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.001.png)

Os equipos ned, rob serán os servidores dns para o dominio stark.lan (Debian) e tywin para lanister.lan (Windows)

Instala no equipo tyrion (Windows) o rol de servidor DHCP coa seguinte configuración: (deberás ter apagados os servidores DHCP do punto anterior)

![](imagenes/imagen.png)

Un ámbito para os equipos da rede privada lanister, con un intervalo de exclusión.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.003.jpeg)

Deberás crear unha reserva estática que estará no rango de enderezos do seu ámbito correspondente.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.004.jpeg)

Establece os nomes de dominio e servidores DNS primario de cada zona.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.005.jpeg)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.006.jpeg)

Deberás actualizar a zona primaria no servidor DNS tywin.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.007.png)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.008.png)

Engade outro ámbito para a rede primaria stark (necesitas outra interface de rede) que actualice a zona prinaria DNS definida no equipo arya.

![](imagenes/imagen.png)

Instala no equipo jaime un servizo DHCP failover para a subrede lanister.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.009.jpeg)

Necesitarás polo menos tres clientes (Cercei,Joffrey, Myrcella) para a rede lannister e un para a rede stark (jon).

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.010.jpeg)

Inclúe capturas de:

- Configuración dos ambitos e rangos de enderezos
- Configuración de opcións
- Configuración da actualización
- Vídeo no que o cliente renova a concesión, e se ve a zona DNS unha vez que o DHCP actualiza o DNS. Tamén o cliente debe ser capaz de resolver o seu propio nome (non FQDN).
- Clientes das dúas subredes, amosando DNS, router e enderezo IP.
- Configuración dos servidores failover
- Capturas dos clientes obtendo enderezos cos dous servidores failover encendidos, e con un acendido e outro apagado (de forma alterna)

Elimina a interface de rede 192.168.11.8 de tyrion, e configura o servizo DHCP Relay no router. Comproba que os equipos da rede stark.lan reciben a configuración de rede de xeito correcto. Inclúe as capturas necesarias.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.011.jpeg)

Actualizacion arya zona directa

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.012.jpeg)

Actualizacion arya zona inversa

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.013.jpeg)

Registro JON automatico, zona directa.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.014.jpeg)

Registro JON automatico zona inversa.

CONFIFURACION DHCP CLIENTES

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.015.jpeg)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.016.jpeg)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.017.jpeg)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.018.jpeg)

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.019.jpeg)

Conmutación por error del dhcp jaime. (Para el dhcp failover)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.020.jpeg)

DHCP desde 192.168.12.8

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.021.png)

Parando el DHCP 192.168.12.8

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.022.jpeg)

DHCP desde el failover 192.168.12.9

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.023.jpeg)

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.024.jpeg)

Configuracion DHCP recibida por el DHCP Relay

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.025.jpeg)

Configuracion DHCP dada desde el DHCP principal.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.026.jpeg)

Cliente recibiendo configuracion DHCP desde servidor principal.

![](imagenes/Aspose.Words.814dc5e8-61fb-4c3d-8542-6b66b214cfe7.002.jpeg)
