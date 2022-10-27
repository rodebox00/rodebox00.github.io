---
layout: post
title: Estudio y comparativa de las 9 plataformas CTF más completas actualmente
---

En este artículo se realiza un estudio del escenario actual en relación a las plataformas CTF que se encuentran disponibles en el mercado mediante el análisis y la comparación de algunas de ellas. A través de este estudio se muestra la variedad de enfoques en los que las plataformas establecen su contenido tanto gratuito como de pago. Así mismo, se comparan las características comunes de las páginas analizadas para ofrecer una visión general de las carencias y virtudes de cada una, así como de sus diferencias.

### 1. TryHackMe

Tryhackme corresponde a una de las plataformas de hacking más conocidas en el mundo y se encuentra enfocada en proporcionar desafíos y contenidos didácticos tanto de forma gratuita como bajo suscripción. La página se basa en 3 conceptos clave tanto para el aprendizaje como para la práctica de conocimientos. Estos conceptos son pathways, módulos y salas. 

Los pathways ofrecidos corresponden a un conjunto de módulos consecutivos que se enfocan en un mismo nivel de experiencia o campo de la ciberseguridad. Estos módulos, se pueden realizar sin necesidad de completar el pathway. Cada uno de los módulos de aprendizaje se centra en herramientas como *Burp Suite* y *Metasploit*, metodologías como escalada de privilegios y búsqueda de vulnerabilidades o conocimientos relacionados con la criptografía y los fundamentos de Windows.

Las salas son un conjunto de actividades a completar basadas en máquinas, documentos o binarios y se pueden encontrar o no dentro de un módulo. Estas actividades pueden ir desde el modelo de desafío CTF hasta analizar tráfico de red, un documento o máquina y responder a las preguntas que realizan. En esta sección se encuentran las máquinas CTF disponibles que en muchas ocasiones no solo piden la flag de determinados usuarios sino también otros datos como por ejemplo la versión de algunos servicios que funcionan en la máquina. En alguna de estas salas se les ofrecen pistas a los jugadores o incluso se establecen una serie de pasos o vídeos para explotar la máquina con fines didácticos.

En la siguiente figura se observa una tarea perteneciente a una sala donde en la parte derecha se encuentra un caso práctico explicado sobre un ataque web y a la izquierda un cuestionario sobre la ejecución del caso práctico.

{:refdef: style="text-align: center;"}
![My Image]({{ site.baseimg }}/images/plataformas/ImagenModuloTryhackme.png)
{: refdef}

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


### 2. Vulnhub

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


### 3. Root Me

Root Me  es una plataforma que ofrece recursos para el aprendizaje en seguridad informática tanto en forma de desafíos como de máquinas CTF a resolver. A la hora de registrarse, la página proporciona tres tipos de accesos:

  - Visitante. Esta suscripción estándar es la dedicada al acceso gratuito dentro de la plataforma. Con este tipo de cuenta se pueden realizar ejercicios gratuitos así como visualizar soluciones de los desafíos proporcionadas por otros usuarios.

  - Contribuidor. Se trata de una suscripción anual de pago en la cual el usuario puede contribuir tanto ofreciendo soluciones corregidas de los ejercicios como participando en la creación de los mismos. Además, también puede participar en el testeo de desafíos en proceso de validación y ser recompensado por ello. A través de la aportación a la plataforma, un usuario contribuidor se puede convertir en premium de tres formas distintas: 1) pagando; 2) mediante la creación desafíos con más de 100 puntos; 3) mediante el desarrollo de al menos 3 desafíos.

  - Premium. Una suscripción premium también corresponde a una suscripción de pago con características muy similares al tipo de cuenta contribuidor. El miembro premium tiene como aspectos relevantes el acceso anticipado a los desafíos creados y la posibilidad de que ante la creación de nuevos retos por parte del mismo, este reciba una compensación económica.

Los desafíos que proporciona Root Me se basan en campos de la ciberseguridad tales como esteganografía, análisis forense, criptografía, redes, cracking, etc. Al iniciar los desafíos se otorgarán los recursos que se necesitan para resolver el mismo. Estos recursos podrán ser archivos descargables, cadenas encriptadas, imágenes, capturas de tráfico o entornos web que deberán ser explotados. Las diferentes soluciones existentes de estos desafíos pueden ser accesibles por el participante una vez que consiga resolver el reto propuesto.

Root Me favorece el despliegue de las máquinas CTF (algunas de las cuales provienen de Vulnhub) en salas. Estas salas permiten que varios jugadores puedan competir entre sí uniéndose a la misma y seleccionando por consenso una máquina a explotar. Las máquinas seleccionadas estarán disponibles para ser explotadas durante un tiempo máximo y serán accesibles través de una URI proporcionada.

El entorno de Root Me se apoya en la comunidad ofreciendo diversos foros de discusión y permitiendo el envío de mensajes entre usuarios. La plataforma fomenta el uso de estas funcionalidades a la hora de obtener información sobre un reto o máquina a resolver. Además, proporciona a los usuarios una sección sobre herramientas para distintas especialidades de la ciberseguridad y una pequeña guía sobre cada una de ellas.

En relación con la conexión por parte de los usuarios a las máquinas y los desafíos, la plataforma no ofrece ningún tipo de VPN sino que cuando un usuario se autentica en la web, esta guarda la dirección IP del usuario y le permite el acceso a través del firewall.

#### Ventajas
  - Ofrece varios idiomas dentro de la página web.
  - Facilita la comunicación con la comunidad.
  - Suministra documentación sobre algunas herramientas.
  - La conexión por parte del usuario resulta cómoda ya que no debe preocuparse por el uso de una VPN.
  - El acceso final a los contenidos es gratuito.

#### Desventajas
  - La plataforma es francesa, por lo que muchos foros y documentación se encuentran en francés.
  - Algunas de las máquinas proporcionadas provienen de otras plataformas por lo que no ofrece una novedad amplia de las mismas.
  - Al no ofrecer una VPN, cualquier usuario que se encuentre en una sala resolviendo una máquina podría descubrir la dirección IP de los usuarios de la misma sala que atacan la máquina.


### 4. picoCTF

La plataforma picoCTF  ha sido desarrollada por la universidad Carnegie Mellon y está basada en el modelo de desafíos CTF. Aunque es accesible para cualquier usuario mayor de 13 años, se encuentra enfocada sobre todo a los estudiantes de secundaria y bachiller (middle school y high school, respectivamente). Todos los contenidos proporcionados por picoCTF son gratuitos y todos los usuarios registrados tienen el mismo tipo de acceso.

El entorno de picoCTF tiene a disposición de los usuarios 4 secciones destacadas:

  - Learn. Este apartado está dedicado al aprendizaje a través de la aportación de guías, videotutoriales y recursos externos. También se enfoca hacia la comunidad mediante la disponibilidad de un foro para profesores y un canal de discord para cualquier usuario.

  - Practice. En esta sección se encuentra picoGym, el cual contiene todos los desafíos CTF disponibles y está dedicado al entrenamiento de los usuarios. 

  - Compete. picoCTF realiza uno o varios torneos al año y permite tanto a los alumnos de una institución como a los usuarios generales inscribirse en ellos y competir en la resolución de desafíos. A través de esta sección también se pueden ver los resultados finales de los torneos ya realizados. 

  - Classrooms: Como se comentaba anteriormente, picoCTF se encuentra enfocado a estudiantes. Por ello, la plataforma ofrece a los profesores de estos alumnos, o a cualquier otro usuario, crear clases donde se pueda observar el progreso de los miembros que se han unido a ellas.

Los desafíos que se encuentran en picoGym corresponden a todos aquellos que han sido publicados por la plataforma, incluidos aquellos que se han empleado en los torneos. Para todos estos retos, se obtienen los puntos asociados a los mismos y se consideran como superados al indicar únicamente la flag correspondiente. Al igual que otras plataformas, existen retos asociados a diferentes temáticas de la ciberseguridad como análisis forense, criptografía, explotación web, etc. Muchos de estos retos contendrán pistas que ayudarán a su resolución y para algunos se entregarán unos recursos adicionales  (programas, binarios, imágenes, etc) como se observa en la próxima figura. Como alternativa, también se puede entregar una dirección en la que se encuentra un servicio o sistema a explotar.

![_config.yml]({{ site.baseurl }}/images/plataformas/imagenpicoCTF.png)

Para completar los desafíos, el usuario puede usar su propio equipo o una máquina virtual sin interfaz gráfica que facilita la página web a través de la cual se pueden realizar la mayoría de los desafíos.

#### Ventajas
  - Acceso gratuito a todos los contenidos.
  - Ideal para profesores de todos los niveles educativos.

#### Desventajas
  - No proporciona máquinas a explotar sino únicamente desafíos.
  - picoCTF está enfocada sobre todo para principiantes, por lo que jugadores de un alto nivel pueden no verse atraídos por la plataforma.

### 5. echoCTF.RED

echoCTF.RED  se trata de una de las páginas menos conocidas en cuanto a desafíos CTF, aunque contiene una gran cantidad de recursos de calidad. Consiste en una plataforma open source que ofrece tanto desafíos como máquinas CTF a resolver de forma gratuita.

Dentro de echoCTF.RED, las máquinas CTF con vulnerabilidades a explotar se denominan targets. Estos targets tienen una sección dedicada dentro de la página donde se indica para cada uno de ellos el nombre, el número de flags que tiene asociado, el número de servicios que corren sobre el target y cuantos han sido descubiertos, el nivel de dificultad, el progreso del usuario, la IP del target, el número de usuarios que lo han resuelto y si se puede conseguir o no el acceso al usuario root. También, para algunos targets y de forma didáctica, echoCTF.RED ofrece la posibilidad de acceder a writeups redactados por los usuarios pero descontando el 50% de la puntuación total que se puede adquirir. Cabe destacar que el contador de los servicios descubiertos por el usuario se incrementará automáticamente cuando este los descubra a través del análisis de puertos o cualquier otro mecanismo.

Además, echoCTF.RED agrupa targets (que no se encuentran en la sección dedicada a targets) con características comunes en redes. De esta forma se pueden encontrar redes con targets específicos que usan *memcached*, enfocados a principiantes, con vulnerabilidades CVE como se presenta en la siguiente figura, con implementaciones DevOps o focalizados en la escalada de privilegios.

![_config.yml]({{ site.baseurl }}/images/plataformas/red de echoCTF.png)

Como se comentaba anteriormente, también se proporcionan una serie de retos. En conjunto, estos retos suman un total de 9 y, aunque son pocos en comparación con otras plataformas, contienen varios pasos a completar. Algunos de estos desafíos están relacionados con targets y otros con categorías como análisis de código, análisis de binarios, docker, análisis forense e ingeniería inversa.

echoCTF.RED ofrece una sección de Dashboard en la que se ofrecer una visión general de la información actualizada de la plataforma y del progreso personal de los miembros tanto en desafíos como en targets. Por último, la plataforma ofrece una VPN para la conexión de los usuarios con los targets y un canal de discord para permanecer en contacto con la comunidad.

#### Ventajas
  - Máquinas constantemente activas sin necesidad de ser iniciadas.
  - Facilidad de realizar múltiples targets simultáneamente.
  - Gran número de targets, actualmente 86.
  - Interfaz intuitiva y sencilla.
  - Visualización sencilla de writeups.

#### Desventajas
  - Escasez de desafíos.
  - Comunidad pequeña.
  - Imposibilidad de participación hoy en día por parte de equipos.

### 6. OverTheWire

Entre las plataformas que tienen como objetivo aprender en base a la práctica de conceptos, se encuentra OverTheWire . Esta corresponde a una plataforma totalmente gratuita y sin ningún tipo de inscripción basada única y exclusivamente en una serie de desafíos denominados Wargames.

Estos Wargames están conformados por varios niveles ordenados de menor a mayor dificultad en los que para cada transición entre estos existe una sección que contiene la información necesaria para realizarla y pasar al siguiente nivel. Cada avance de nivel dentro de un mismo desafío puede precisar del uso de técnicas de diversos campos, como por ejemplo análisis de código o criptografía.

Para avanzar de un nivel a otro, los desafíos de OverTheWire tienen para cada uno un usuario dentro del sistema a explotar. De esta forma, los recursos que deben ser vulnerados para conseguir la contraseña de un usuario se encuentran en el usuario del nivel anterior. Algunos Wargames están enfocados hacia usuarios principiantes o en temas concretos como la seguridad web o la seguridad del código.  

La plataforma también ofrece otros Wargames en forma de máquina virtual para la realización de los desafíos en local. Para los retos proporcionados de forma online, todos menos uno (Wargame Natas, accesible por web) son accesibles a través del protocolo SSH por un puerto y dominio específico. De esta forma, cuando se progresa de un nivel a otro superior, se accede al mismo dominio y puerto pero con el usuario del nivel correspondiente.

Al igual que otras plataformas, OverTheWire se apoya en un canal de discord dedicado a la comunidad.

#### Ventajas
  - Facilidad para conectarse a los desafíos.
  - Progreso incremental dentro de los Wargames.
  - Wargames para los usuarios experimentados y principiantes.

#### Desventajas
  - No cuenta con la creación de perfiles para los usuarios.
  - Algunos enlaces de las imágenes ISO se encuentran caídos.
  - Muchas transiciones entre niveles no tienen ningún tipo de información o ayuda por lo que si se necesita, esta tiene que ser buscada en la comunidad.
  - Apenas 12 Wargames accesibles de forma online.

### 7. Web Security Academy

Web Security Academy es un entorno controlado específico de hacking web desarrollado por PortSwigger, empresa creadora de la herramienta *Burp Suite* y que se encuentra accesible a través de su página web. Todos los recursos proporcionados son gratuitos y accesibles a través de la inscripción como usuario en la página. 

Web Security Academy posee como ejes principales de la plataforma, tanto los topics como los labs. Los topics hacen referencia a conceptos relacionados con la seguridad web como inyecciones SQL, vulnerabilidades de autenticación, vulnerabilidades de control de acceso y escalado de privilegios, etc. Estos topics están constituidos por un texto explicativo que puede ir acompañado de vídeos o de laboratorios que están relacionados con el topic. Además, un topic puede tener subtopics que forman parte del topic principal y extienden los contenidos del mismo. La plataforma también ofrece un *Learning Path* donde se agrupan los topics en base a características comunes y se enumeran en un orden adecuado para el progreso del usuario. 

Los labs contienen su propio apartado dentro de la página y se tratan de laboratorios en los que se pone en práctica los conceptos de hacking expuestos en los topics, por lo que cada lab se encuentra relacionado con uno. A la hora de acceder a uno de estos labs, la página redireccionará al usuario a un entorno controlado donde deberá realizar la explotación de la vulnerabilidad. Una vez efectuada la explotación de la brecha de seguridad en cuestión, el lab se establecerá como resuelto para el usuario y este incrementará su nivel. Cada lab tiene adjuntado su solución, la cual puede ser vista en cualquier momento de la resolución y algunos también contienen soluciones realizadas por la comunidad en forma de vídeo.

En base a los contenidos de hacking que proporciona, la compañía Portswigger ofrece también una certificación de pago enfocado a los usuarios de Web Security Academy. Con esta certificación, se proporciona un examen de prueba e información sobre el funcionamiento y la preparación de cara al examen. Aparte, enfocándose en la comunidad, la página ofrece varios foros de debate.

#### Ventajas
  - Contenido gratuito y actualizado.
  - Gran cantidad de labs.
  - Documentación extensa.

#### Desventajas
  - Solo provee recursos relacionados con la seguridad en el entorno web.
  - Muchos de los labs propuestos tienen como solución o son preparados para el uso de *Burp Suite*, lo que provoca que no se incite al uso de otras herramientas.

### 8. Pentester Lab

Pentester Lab  ofrece dos tipos de versiones para los usuarios, una gratuita y otra de pago, Pentester Lab Pro. Los dos tipos de versiones se diferencian en el acceso o no a ciertos contenidos. En general, la plataforma proporciona ejercicios a resolver de distintos ámbitos. 

Los ejercicios que Pentester Lab propone contienen una estructura similar a la mostrada en la próxima figura. Cada uno contiene un apartado llamado Course donde se explicará o no la vulnerabilidad a explotar sobre la que trata el ejercicio. Normalmente estos ejercicios también suelen contener un vídeo sobre su resolución, la explicación de la solución o una sección donde introducir una flag correspondiente. Algunos ejercicios contienen también archivos adjuntos relacionados con la resolución del ejercicio y otros se pueden resolver mediante el uso de una consola proporcionada o a través de la web sin necesidad del uso de una VPN.  

![_config.yml]({{ site.baseurl }}/images/plataformas/FotoPentesterLab.png)

Estos ejercicios con características comunes se agrupan entre sí en badges. Por ello, existen badges enfocados en la evasión de la autenticación, en la seguridad a nivel de sistema operativo, sobre Android, etc. Una vez que el usuario completa un badge, la plataforma emite un certificado que indica la resolución del badge. Además, dentro de la sección *Progress*, los badges son ordenados en base a una secuencia sugerida por la plataforma.

Dentro del entorno web, la página también contiene un blog enlazado donde se publican artículos sobre ciberseguridad y una sección con conceptos de informática enlazados a Wikipedia.

#### Ventajas
  - Gran cantidad de ejercicios y recursos de distintos temas en la versión Pro.
  - Badges sobre temas poco frecuentes.
  - Proporciona una certificación sobre la completitud de un badge.

#### Desventajas
  - Mayoría de ejercicios de pago.
  - No ofrece ningún foro o canal para la comunidad.

### 9. Hack The Box

En cuanto a máquinas CTF, HTB es una de las plataformas más importantes del mercado. Aunque es más conocida por las máquinas que ofrece, también proporciona junto con otros servicios, retos de hacking ético de diversas temáticas. Sobre los planes de suscripción, HTB ofrece tres tipos, uno gratuito, uno *Vip* y otro *Vip+*. Estos planes se detallarán en el apartado de análisis sobre HTB. De forma paralela, la plataforma gestiona una academia gratuita llamada *HTB Academy*, la cual es enlazada desde algunas secciones de la página. 

En relación con las máquinas albergadas en HTB, el entorno ofrece tanto retiradas como activas. Las máquinas activas corresponden a aquellas disponibles para ser explotadas, en cambio, las máquinas retiradas son aquellas que ya no están disponibles y de las que existen writeups accesibles. Una gran diferencia que existe entre la versión gratuita y las versiones *Vip* es que la versión gratuita solo tiene acceso a las 2 últimas máquinas retiradas y las versiones *Vip* a todas. Cabe destacar que las instancias de las máquinas son atacadas por multitud de usuarios salvo para los miembros *Vip+* que tienen sus propias instancias.

Los desafíos que se encuentran disponibles son de diversos temas tales como hardware o análisis forense. Al igual que con las máquinas disponibles, existen retos retirados que solo son accesibles para usuarios *VIP* y *Vip+*. Dentro de la página también se puede encontrar una sección llamada *Battlegrounds*, la cual permite a varios equipos realizar una batalla. Estas batallas pueden consistir en por ejemplo, atacar las máquinas del rival y defender aquellas que pertenecen al equipo.

Para la resolución de una máquina, el jugador debe conectarse a ella y realizar la serie de ataques de vulneración a través de la VPN disponible. Al igual que otras plataformas, HTB facilita una máquina virtual con interfaz gráfica accesible mediante el navegador enfocada para atacar las instancias. 

Con respecto a la comunidad, HTB suministra tanto foros como un canal de discord y la posibilidad de enviar mensajes privados entre usuarios.

#### Ventajas
  - Gran comunidad activa.
  - Publicación de una máquina nueva cada Sábado.
  - Publicación de un nuevo desafío cada viernes.
  - Gran cantidad de contenidos.

#### Desventajas
  - Imposibilidad de acceso a writeups de máquinas activas.
  - Acceso limitado a máquinas y desafíos retirados.



### Comparación de las distintas plataformas CTF existentes

Todas las plataformas evaluadas anteriormente tienen como característica común que están enfocadas al entrenamiento y progreso de las técnicas de hacking ético y ciberseguridad. Aunque algunas de estas páginas se centran en multitud de aspectos y campos de la ciberseguridad, existen otras como Web Security Academy, enfocada exclusivamente en la seguridad web. 

Uno de los aspectos relevantes y por el que muchos usuarios se decantan a la hora de elegir una plataforma, es la existencia de contenido didáctico, ya sea enfocado a la resolución de ejercicios o sobre tópicos en general. Dentro de las páginas que ofrecen este contenido, se encuentran TryHackMe, picoCTF, Pentester Lab, Web Security Academy y Hack The Box. Que estas páginas ofrezcan un contenido didáctico acerca más a los usuarios inexpertos del mundo de la ciberseguridad. En cambio, que algunas como picoCTF estén demasiado enfocadas a principiantes y al control de la progresión de los miembros, hace que no sean tan atractivas para los usuarios más avanzados. Además, algunas como HTB y Web Security Academy mantienen el contenido actualizado, a diferencia de otras como OverTheWire.

Dentro de los recursos más valorados por los usuarios de estas plataformas, se encuentran las máquinas CTF, las cuales son ofrecidas por TryHackMe, Vulnhub, Root Me, echoCTF.RED y Hack The Box. Vulnhub, se diferencia de todas las demás proveedoras en que única y exclusivamente se dedica a las máquinas CTF. En concreto, a proveer máquinas que pueden ser descargadas. El resto, ofrecen estas máquinas de forma online siendo accesibles a través de una VPN (excepto Root Me). En relación con los writeups, tanto HTB como echoCTF.RED los brindan a través de su página web.

En relación con los desafíos CTF, todas excepto Vulnhub contienen de varios temas. Algunas poseen desafíos sobre contenidos poco frecuentes tales como hardware para HTB o Android para Pentester Lab. La inmensa mayoría de los entornos salvo la ya mencionada Vulnhub y Web Security Academy dedicada a desafíos web, abarcan retos sobre los temas más comunes, criptografía, red, reversing, análisis forense, etc y se consiguen resolver capturando una o más flags. Aunque echoCTF.RED incluye varios de estos temas, ofrece a los usuarios un número escaso de desafíos. 

Para realizar los desafíos y las máquinas, algunas plataformas como TryHackMe, Pentester Lab, HTB o picoCTF ofrecen una máquina virtual evitando que el usuario tenga que tener una en local. Aunque la máquina virtual que presenta TryHackMe, Pentester Lab y HTB es más sofisticada, el acceso a esta se encuentra limitado si el usuario no es un usuario de pago. Estas tres páginas corresponden concretamente a aquellas cuyo contenido no es totalmente gratuito aunque suministran contenido gratuito de calidad a pesar de que el ofrecido por Pentester Lab es escaso. 

La mayoría de los entornos estudiados a excepción de Vulnhub y Pentester Lab, ofrecen una comunidad de discusión a los usuarios. Esta comunidad, al igual que los contenidos didácticos, es de gran utilidad para los jugadores principiantes y un gran apoyo para la resolución de dudas o problemas relacionados con la plataforma. Así mismo, tanto Vulnhub como OverTheWire carecen de la posibilidad de que se registren usuarios, por lo que el progreso de los jugadores no es tan visible como en otras plataformas, así como la comunicación entre ellos.

A continuación, mediante la siguiente tabla se puede observar de un modo más visual las características y diferencias de las distintas plataformas.

{:refdef: style="text-align: center;"}
![My Image]({{ site.baseimg }}/images/plataformas/TablaComparativa.png)
{: refdef}
