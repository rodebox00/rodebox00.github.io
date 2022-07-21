---
layout: post
title: Metodología basada en la resolución de Máquinas CTF
---

Actualmente, la realización de una auditoría de seguridad se lleva a cabo en base a una determinada metodología. Para la resolución de máquinas específicas, en esta sección se detalla la metodología a utilizar. Para cada una de las fases que la componen, se nombran una serie de herramientas que ayudan al desarrollo de la misma en distintos escenarios. En la siguiente figura se presenta un resumen cronológico de las fases que componen la metodología.

{:refdef: style="text-align: center;"}
![My Image]({{ site.baseimg }}/images/GraficoDeTransiciones.png)
{: refdef}

### 1. Enumeración

La enumeración corresponde a la fase inicial en la que se analizan y exploran los puertos abiertos de la máquina víctima así como los servicios que corren en ella. El objetivo principal es trata de recolectar información de utilidad que nos ayude en las próximas fases, sobre todo en el análisis de vulnerabilidades.

Mediante el uso de técnicas y herramientas, en la fase de enumeración podremos descubrir subdominios web, directorios, nombres de usuarios, servicios activos, herramientas y frameworks empleados, puertos abiertos, el sistema operativo en uso, etc. Algunas de estas herramientas se exponen a continuación.

  - **Nmap**. Se trata de una de las herramientas de escaneo de redes y equipos más potente y conocida. A través de ella podremos enumerar los puertos y servicios de una máquina víctima. También nos permite el uso de potentes scripts de enumeración sobre servicios, como *http-enum* el cual enumera los directorios más famosos de las aplicaciones web en la máquina objetivo o *vuln*, cuyo propósito es descubrir las vulnerabilidades CVE presentes.
  - **Wfuzz**. Esta herramienta permite la enumeración de recursos en aplicaciones web mediante la técnica de fuzzing. Esta técnica hace uso de diccionarios para descubrir subdominios, ficheros o directorios mediante peticiones al servidor web y analizando la cabecera de respuesta.
  - **WhatWeb**. Esta herramienta nos permite extraer datos de una página web, como por ejemplo, las tecnologías que se encuentran funcionando así como paquetes o librerías de JavaScript entre otros. La información recolectada nos sirve como primer paso para enfocar el desarrollo del proceso de resolución.


### 2. Análisis de vulnerabilidades

En esta fase se buscarán vulnerabilidades asociadas a las herramientas o servicios encontrados durante la enumeración. La finalidad de este análisis será poder encontrar alguna vulnerabilidad a explotar que nos permita la intrusión en la máquina víctima.

Una gran cantidad de las vulnerabilidades encontradas corresponderán a vulnerabilidades CVE, de las cuales, para un amplio número de estas, existirán exploits relacionados. Estas vulnerabilidades CVE estarán asociadas con herramientas y servicios que se encuentran en el mercado y cuyas versiones se encuentran desactualizadas.

El otro grupo de vulnerabilidades a explotar pertenecerá a aquellas que dependen de malas configuraciones o de servicios de desarrollo propio. En relación con estos últimos, mediante el estudio del comportamiento se pueden explotar vulnerabilidades tales como RCE o RFI.

Cabe destacar que, durante la resolución de una máquina, se pueden llegar a realizar varias transiciones entre la fase de enumeración y esta. Esto se debe a que con frecuencia en cada resultado obtenido durante la enumeración se explore algún tipo de vulnerabilidad relacionada. Algunas herramientas que se emplean en esta fase, son listadas a continuación.

  - **Nessus**. Es un programa avanzado de escaneo de vulnerabilidades sobre un objetivo. El tipo de análisis que se desea realizar se selecciona a través de plantillas de escaneo. De esta forma se pueden ejecutar escaneos centrados en aplicaciones web, malware, directorio activo, etc. Una vez realizado el escaneo, *Nessus* nos reporta información de utilidad así como vulnerabilidades asociadas si las hubiere.
  - **Nikto**. Corresponde a una herramienta de análisis de vulnerabilidades web. Este programa nos informará sobre vulnerabilidades existentes en un objetivo, así como información relevante que nos pueda conducir a la explotación del servicio web. Entre este tipo de información se encuentran archivos y directorios, versión del gestor de contenidos, software del servidor, etc.
  - **Ghidra**. Es un programa enfocado principalmente en la puesta en práctica de la ingeniería inversa. Con ella podemos decompilar ejecutables y analizarlos en busca de vulnerabilidades o de información de valor sobre su ejecución. El uso de esta herramienta nos ayudará principalmente en el análisis de vulnerabilidades software de bajo nivel como buffer overflow.


### 3. Explotación e intrusión

Tras descubrir una vulnerabilidad relevante, nos adentramos en la fase de explotación. Está fase resulta ser la más efímera puesto que se trata únicamente de lanzar nuestro ataque una vez que recolectamos la información necesaria. En esta etapa se ejecutarán una serie de pasos manuales de explotación o directamente un exploit. Ambos enfoques permitirán acceder a la máquina como un usuario de ella. El uso de un exploit conllevará en algunos casos el estudio y la modificación del mismo para su correcto funcionamiento.

Una de las vulnerabilidades más explotadas es RCE. Ante esta vulnerabilidad, normalmente desplegaremos una reverse shell (shell inversa) para acceder como un usuario y facilitarnos el desarrollo de la siguiente fase. Una reverse shell se basa en que la máquina víctima se conecta a nosotros proporcionándonos una shell remota. A continuación se muestran algunas de las herramientas que nos ayudan en el proceso de explotación.

  - **Burp Suite**. Esta es una de las herramientas más utilizadas para el hacking y análisis de aplicaciones web. Mediante su uso podemos alterar las peticiones HTTP insertar código malicioso que nos permitan desde obtener información relevante a explotar el servicio web. Una característica destacada de *Burp Suite* es la posibilidad de efectuar un ataque de diccionario.
  - **sqlmap**. Es una herramienta que nos permite automatizar los ataques de inyección SQL y descubrir si un servidor web es vulnerable a este tipo de ataques. Mediante la funcionalidad proporcionada podremos listar las bases de datos existentes, obtener las columnas de una base de datos, obtener usuarios y contraseñas contenidos en una base de datos, etc.
  - **Metasploit**. Es un framework compuesto por numerosas herramientas y ampliamente conocido en el mundo de la seguridad informática. Mediante la consola *msfconsole* podremos hacer uso del framework y realizar numerosas acciones como generar payloads o buscar y ejecutar exploits relacionados con programas, etc. Cabe destacar que mediante esta misma interfaz *msfconsole* también se pueden utilizar herramientas de análisis como *nmap* y *Nessus*.


### 4. Escalada de privilegios

Esta fase corresponde a aquella en la que nos encontramos como un usuario dentro de la máquina víctima y queremos escalar hacia otros que contengan las flags deseadas. Durante este proceso se explotarán fallos de seguridad en el sistema que nos permitirán tomar el control de otro usuario. Dependiendo de la máquina será necesario escalar una o más veces hacia otro usuario. Por normal general, conforme escalamos nos acercamos más a la obtención de la flag root.

El enfoque que se debe usar en esta fase es el de intentar llevar a cabo un abuso de los privilegios asociados al usuario o el de intentar explotar alguna vulnerabilidad contenida en algún servicio o programa que opera en local.

Cabe destacar que el objetivo de la escalada de privilegios implica estudio detallado de los contenidos y procesos del sistema. Este análisis será facilitado con el uso de herramientas adecuadas.

  - **linPEAS**. Es un potente script que nos busca posibles vías de escalada de privilegios a nivel de sistema operativo Linux. También existe ofrece una versión similar para Windows denominada *winPEAS*. Este nos mostrará toda la información del sistema, ficheros, programas y configuraciones que puedan servir de utilidad para realizar la escalada de privilegios. Adicionalmente, nos mostrará vulnerabilidades CVE y exploits útiles.
  - **Mimikatz**. Es una poderosa herramienta de código abierto usada para elevar privilegios en sistemas Windows. Su principal función es extraer de memoria RAM contraseñas en texto claro, hashes o tickets de kerberos entre otros. De esta forma podremos realizar ataques como *pass the hash* o *pass the ticket*. Cabe destacar que Mimikatz necesita permisos de administrador local para analizar la RAM del sistema.
  - **pspy**. Se trata de un programa que nos permite ver todos los procesos en ejecución dentro de la máquina sin necesidad de ser usuario root. De este modo podemos descubrir y analizar tareas periódicas o programas de otros usuarios en ejecución que de forma indirecta nos permitan realizar una escalada de privilegios.

### 5. Redacción de informes

La fase de redacción de informes corresponde a una fase opcional en la resolución de máquinas CTF. En estos documentos se detallan los pasos realizados en cada fase para la obtención de las flags. Los informes se deben apoyar en el uso de capturas que plasmen los procedimientos seguidos junto con las herramientas empleadas y las evidencias. La construcción de estos se puede realizar de forma paralela al proceso de resolución de la máquina. Estos informes suelen ser conocidos como writeups.

Cabe destacar que en una situación real la redacción de informes serviría para notificar a superiores y/o clientes de los posibles fallos de seguridad encontrados. De forma adicional, se podrían incluir sugerencias y acciones para solucionar dichos fallos.
