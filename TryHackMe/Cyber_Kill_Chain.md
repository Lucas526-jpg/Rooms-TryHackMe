# Careers in cyber

## Introduccion

El término «cadena de destrucción» es un concepto militar relacionado con la estructura de un ataque. Consiste en la identificación del objetivo, la decisión y la orden de atacar el objetivo y, finalmente, la destrucción del objetivo.

En esta sala exploraremos las siguientes fases del ataque:Reconocimiento,armamento,entrega,explotación,instalación,mando y control,acciones sobre los objetivos.

## Reconocimiento

El reconocimiento consiste en descubrir y recopilar información sobre el sistema y la víctima. La fase de reconocimiento es la fase de planificación para los adversarios.

### Preguntas

¿Cómo se llama la herramienta Intel Gathering Tool, que es una interfaz web para las herramientas y recursos comunes de inteligencia de código abierto?  
Respuesta: OSINT Framework  
¿Cuál es la definición del proceso de recopilación de correos electrónicos durante la fase de reconocimiento?  
Respuesta: email harvesting  

## Armamento

La mayoría de los atacantes suelen utilizar herramientas automatizadas para generar el malware o recurren a la DarkWeb para comprarlo. Los actores más sofisticados escribirían su propio malware personalizado para que la muestra de malware fuera única y evitara la detección en el objetivo.

- El malware es un programa o software diseñado para dañar, interrumpir o obtener acceso no autorizado a un ordenador.
- Un exploit es un programa o código que aprovecha la vulnerabilidad o fallo de una aplicación o sistema.
- Un payload es un código malicioso que el atacante ejecuta en el sistema.

### Pregunta

Este término se refiere a un grupo de comandos que realizan una tarea específica. Se pueden considerar como subrutinas o funciones que contienen el código que la mayoría de los usuarios utilizan para automatizar tareas rutinarias. Sin embargo, los actores maliciosos tienden a utilizarlos con fines maliciosos y los incluyen en documentos de Microsoft Office. ¿Puede proporcionar el término para ello?

RESPUESTA: macro

## Entrega

- Correo electrónico de phishing: después de realizar el reconocimiento y determinar los objetivos del ataque, el actor malicioso crearía un correo electrónico malicioso dirigido a una persona específica (ataque de spearphishing) o a varias personas de la empresa,El correo electrónico contendría un payload o malware. 
- Distribuir memorias USB infectadas en lugares públicos como cafeterías, aparcamientos o en la calle.
- Ataque Watering Hole es un ataque dirigido diseñado para atacar a un grupo específico de personas comprometiendo el sitio web que suelen visitar y redirigiéndolos a un sitio web malicioso elegido por el atacante.

### Pregunta

¿Cómo se llama el ataque cuando se realiza contra un grupo específico de personas y el atacante busca infectar el sitio web que dicho grupo visita constantemente?

RESPUESTA:watering hole attack

Los responsables de la respuesta ante incidentes responden de forma productiva y eficaz a las brechas de seguridad. Sus responsabilidades incluyen la creación de planes, políticas y protocolos que las organizaciones deben aplicar durante y después de los incidentes.  
Sus responsabilidades son:  
1. Desarrollar y adoptar un plan de respuesta a incidentes exhaustivo y viable.
2. Mantener sólidas prácticas de seguridad y apoyar las medidas de respuesta a incidentes.
3. Elaborar informes tras los incidentes y prepararse para futuros ataques, teniendo en cuenta las lecciones aprendidas y las adaptaciones que se deben realizar a partir de los incidentes.

## Explotacion

Para acceder al sistema, un atacante necesita explotar la vulnerabilidad, ya sea con ataques de phishing o un exploit  del "dia cero"(es un exploit desconocido que expone una vulnerabilidad en el software o el hardware).

Estos son algunos ejemplos de cómo un atacante lleva a cabo la explotación:

- La víctima activa el exploit al abrir el archivo adjunto del correo electrónico o al hacer clic en un enlace malicioso.
- Utilizando un exploit de día cero.
- Explotando vulnerabilidades de software, hardware o incluso humanas.
- Un atacante activa el exploit para vulnerabilidades basadas en el servidor.

Tras obtener acceso al sistema, el actor malicioso podía explotar vulnerabilidades del software, del sistema o del servidor para escalar privilegios o moverse lateralmente por la red.

### Pregunta

¿Puede proporcionar el nombre de un ciberataque dirigido a una vulnerabilidad de software desconocida para los proveedores de antivirus o software?

Respuesta:Zero-day

## Instalacion

Una puerta trasera persistente permitirá al atacante acceder al sistema que comprometió en el pasado, ya que una vez que el atacante obtiene acceso al sistema, querrá volver a acceder al sistema si pierde la conexión con él, si es detectado y se le retira el acceso inicial, o si el sistema se actualiza posteriormente.

La persistencia se puede lograr a través de:

- Instalación de un shell web en el servidor web: Un shell web es un script malicioso escrito en lenguajes de programación de desarrollo web como ASP, PHP o JSP que utiliza un atacante para mantener el acceso al sistema comprometido.
- Instalación de una puerta trasera en el equipo de la víctima: Por ejemplo, el atacante puede utilizar Meterpreter para instalar una puerta trasera en el equipo de la víctima.
- Creación o modificación de servicios de Windows:Un atacante puede crear o modificar los servicios de Windows para ejecutar scripts o cargas maliciosas de forma regular como parte de la persistencia, el atacante también puede enmascarar la carga maliciosa utilizando un nombre de servicio que se sabe que está relacionado con el sistema operativo o con software legítimo.
- Añadiendo la entrada a las «claves de ejecución» para el payload malicioso en el Registro o en la carpeta de inicio. Al hacerlo, el payload se ejecutará cada vez que el usuario inicie sesión en el equipo.

En esta fase, el atacante también puede utilizar la técnica Timestomping para evitar ser detectado por el investigador forense y también para hacer que el malware parezca parte de un programa legítimo. La técnica Timestomping permite al atacante modificar las marcas de tiempo del archivo, incluyendo las horas de modificación, acceso, creación y cambio.

### Preguntas

¿Puede indicar la técnica utilizada para modificar los atributos de tiempo de los archivos con el fin de ocultar los nuevos archivos o los cambios realizados en los archivos existentes?

Respuesta:Timestomping

¿Puede nombrar el script malicioso que un atacante instala en el servidor web para mantener el acceso al sistema comprometido y permitir el acceso remoto al servidor web?

Respuesta: Web shell

## COMANDO Y CONTROL

Después de conseguir persistencia y ejecutar el malware en el equipo de la víctima, un ciberdelincuente abre el canal C2 (Comando y Control) a través del malware para controlar y manipular remotamente a la víctima. Este término también se conoce como C&C o C2 Beaconing, como un tipo de comunicación maliciosa entre un servidor C&C y el malware en el host infectado. El host infectado se comunicará constantemente con el servidor C2.

El punto final comprometido se comunicaría con un servidor externo configurado por un atacante para establecer un canal de comando y control. Después de establecer la conexión, el atacante tiene control total sobre la máquina de la víctima.

Los canales C2 más comunes utilizados por los adversarios hoy en día:

- Los protocolos HTTP en el puerto 80 y HTTPS en el puerto 443: este tipo de baliza mezcla el tráfico malicioso con el tráfico legítimo y puede ayudar al atacante a evadir los cortafuegos.
- DNS (servidor de nombres de dominio). La máquina infectada realiza solicitudes DNS constantes al servidor DNS que pertenece a un atacante. Este tipo de comunicación C2 también se conoce como túnel DNS.

### Pregunta

¿Qué es la comunicación C2 en la que la víctima realiza solicitudes DNS periódicas a un servidor DNS y un dominio que pertenecen a un atacante?

Respuesta:DNS Tunneling

## ACCIONES SOBRE LOS OBJETIVOS

Después de pasar por seis fases del ataque, un ciberdelincuente finalmente puede alcanzar sus objetivos, lo que significa actuar sobre los objetivos originales. Con acceso práctico al teclado, el atacante puede lograr lo siguiente:

- Recopilar las credenciales de los usuarios.
- Realizar una escalada de privilegios (obtener acceso elevado, como el acceso de administrador de dominio desde una estación de trabajo, aprovechando la configuración incorrecta).
- Reconocimiento interno (por ejemplo, un atacante interactúa con el software interno para encontrar sus vulnerabilidades).
- Movimiento lateral a través del entorno de la empresa.
- Recopilar y extraer datos confidenciales.
- Eliminar las copias de seguridad y las instantáneas de sombra. Shadow Copy es una tecnología de Microsoft que permite crear copias de seguridad, instantáneas de archivos informáticos o volúmenes.
- Sobrescribir o corromper datos.
### Preguntas

¿Puede proporcionar una tecnología incluida en Microsoft Windows que permita crear copias de seguridad o instantáneas de archivos o volúmenes en el ordenador, incluso cuando están en uso?

Respuesta:Shadow Copy

