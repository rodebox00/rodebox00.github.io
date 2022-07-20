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


### Vulnhub

Vulnhub  es una plataforma que se aleja del marco común del resto de plataformas que proporcionan máquinas CTF ya que a diferencia de ellas no existe suscripción alguna y las máquinas deben instalarse y explotarse en local. El entorno de Vulnhub permite que los creadores de máquinas puedan agrupar aquellas máquinas que sean de una misma temática. 

Las imágenes se pueden descargar tanto en extensión *.ova* como *.torrent* y una vez descargadas, ejecutadas en una máquina virtual. Cada imagen proporcionada por Vulnhub contiene una descripción documentada por los creadores donde indican las características y el nivel de dificultad, así como alguna pista para su resolución. También existe una sección por cada imagen donde se determinan las configuraciones de red de la misma con el fin de facilitar el despliegue.

#### Ventajas
  - El usuario no necesita ningún tipo de registro.
  - Tiempo ilimitado para la explotación de la máquina.
  - Características innatas de las máquinas virtuales (creación de instantáneas, aislamiento del sistema operativo anfitrión, etc).

#### Desventajas
  - Necesidad de espacio en disco local para almacenar las imágenes y las posteriores máquinas virtuales.
  - No existe un control de las posibles amenazas de seguridad para el usuario final que podría contener una imagen subida a la plataforma.
  - Ausencia de comunidad dentro de la plataforma.
  - El proceso de publicación como creador de una imagen es lento.


### Root Me

Root Me  es una plataforma que ofrece recursos para el aprendizaje en seguridad informática tanto en forma de desafíos como de máquinas CTF a resolver. A la hora de registrarse, la página proporciona tres tipos de accesos:

  - Visitante: Esta suscripción estándar es la dedicada al acceso gratuito dentro de la plataforma. Con este tipo de cuenta se pueden realizar ejercicios gratuitos así como visualizar soluciones de los desafíos proporcionadas por otros usuarios.

  - Contribuidor: Se trata de una suscripción anual de pago en la cual el usuario puede contribuir tanto ofreciendo soluciones corregidas de los ejercicios como participando en la creación de los mismos. Además, también puede participar en el testeo de desafíos en proceso de validación y ser recompensado por ello. A través de la aportación a la plataforma, un usuario contribuidor se puede convertir en premium de tres formas distintas: 1) pagando; 2) mediante la creación desafíos con más de 100 puntos; 3) mediante el desarrollo de al menos 3 desafíos.

  - Premium: Una suscripción premium también corresponde a una suscripción de pago con características muy similares al tipo de cuenta contribuidor. El miembro premium tiene como aspectos relevantes el acceso anticipado a los desafíos creados y la posibilidad de que ante la creación de nuevos retos por parte del mismo, este reciba una compensación económica.

Los desafíos que proporciona Root Me se basan en campos de la ciberseguridad tales como esteganografía, análisis forense, criptografía, redes, cracking, etc. Al iniciar los desafíos se otorgarán los recursos que se necesitan para resolver el mismo. Estos recursos podrán ser archivos descargables, cadenas encriptadas, imágenes, capturas de tráfico o entornos web que deberán ser explotados. Las diferentes soluciones existentes de estos desafíos pueden ser accesibles por el participante una vez que consiga resolver el reto propuesto.

Root Me favorece el despliegue de las máquinas CTF (algunas de las cuales provienen de Vulnhub) en salas. Estas salas permiten que varios jugadores puedan competir entre sí uniéndose a la misma y seleccionando por consenso una máquina a explotar. Las máquinas seleccionadas estarán disponibles para ser explotadas durante un tiempo máximo y serán accesibles través de una URI proporcionada.

El entorno de Root Me se apoya en la comunidad ofreciendo diversos foros de discusión y permitiendo el envío de mensajes entre usuarios. La plataforma fomenta el uso de estas funcionalidades a la hora de obtener información sobre un reto o máquina a resolver. Además, proporciona a los usuarios una sección sobre herramientas para distintas especialidades de la ciberseguridad y una pequeña guía sobre cada una de ellas.

En relación con la conexión por parte de los usuarios a las máquinas y los desafíos, la plataforma no ofrece ningún tipo de VPN sino que cuando un usuario se autentica en la web, esta guarda la dirección IP del usuario y le permite el acceso a través del firewall.
