---
layout: post
title: Estudio y comparativa de las 9 plataformas CTF más completas del mercado
---

En este artículo se realiza un estudio del escenario actual en relación a las plataformas CTF que se encuentran disponibles en el mercado mediante el análisis y la comparación de algunas de ellas. A través de este estudio se muestra la variedad de enfoques en los que las plataformas establecen su contenido tanto gratuito como de pago. Así mismo, se comparan las características comunes de las páginas analizadas para ofrecer una visión general de las carencias y virtudes de cada una, así como de sus diferencias.

### TryHackMe

Tryhackme corresponde a una de las plataformas de hacking más conocidas en el mundo y se encuentra enfocada en proporcionar desafíos y contenidos didácticos tanto de forma gratuita como bajo suscripción. La página se basa en 3 conceptos clave tanto para el aprendizaje como para la práctica de conocimientos. Estos conceptos son pathways, módulos y salas. 

Los pathways ofrecidos corresponden a un conjunto de módulos consecutivos que se enfocan en un mismo nivel de experiencia o campo de la ciberseguridad. Estos módulos, se pueden realizar sin necesidad de completar el pathway. Cada uno de los módulos de aprendizaje se centra en herramientas como *Burp Suite* y *Metasploit*, metodologías como escalada de privilegios y búsqueda de vulnerabilidades o conocimientos relacionados con la criptografía y los fundamentos de Windows.

Las salas son un conjunto de actividades a completar basadas en máquinas, documentos o binarios y se pueden encontrar o no dentro de un módulo. Estas actividades pueden ir desde el modelo de desafío CTF hasta analizar tráfico de red, un documento o máquina y responder a las preguntas que realizan. En esta sección se encuentran las máquinas CTF disponibles que en muchas ocasiones no solo piden la flag de determinados usuarios sino también otros datos como por ejemplo la versión de algunos servicios que funcionan en la máquina. En alguna de estas salas se les ofrecen pistas a los jugadores o incluso se establecen una serie de pasos o vídeos para explotar la máquina con fines didácticos.

En la siguiente figura se observa una tarea perteneciente a una sala donde en la parte derecha se encuentra un caso práctico explicado sobre un ataque web y a la izquierda un cuestionario sobre la ejecución del caso práctico.

![_config.yml]({{ site.baseurl }}/images/ImagenModuloTryhackme.png)

Cuando los participantes se registran en la página, indican el nivel de experiencia que poseen en base al cuál les recomendará un contenido u otro. El perfil de usuario dentro de la plataforma irá incrementando de nivel así como la posición dentro del ranking global conforme se vayan ganando puntos en la realización de actividades.

Tryhackme brinda una VPN para poder conectarse a la red en la que se encuentran las máquinas vulnerables y aparte, ofrece una máquina virtual Kali Linux accesible a través de la web.


#### Ventajas
  - Contiene módulos variados de distintos campos de la ciberseguridad como el análisis de malware y los fundamentos del hacking web.
  - Se encuentra enfocado a un perfil más didáctico y por ello puede ser un entorno muy útil para usuarios principiantes.
  - Máquina virtual en la nube accesible desde la web para realizar los desafíos. 

#### Desventajas
  - La mayoría de las máquinas y módulos avanzados y por ende los pathways, están disponibles bajo  suscripción.
  - La máquina virtual en la nube que suministra la plataforma, tiene un tiempo limitado de uso si no eres usuario premium.
  - A día de hoy por defecto los usuarios no están aislados entre sí a través de la VPN que ofrece Tryhackme por lo que un usuario puede ser atacado por otro.
