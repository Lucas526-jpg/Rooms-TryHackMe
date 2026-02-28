<section align="center">

# OWASP Top 10 2025: IAAA Failures

![Dificultad](https://img.shields.io/badge/Dificultad-Informativa-green?style=for-the-badge)
![Plataforma](https://img.shields.io/badge/Plataforma-TryHackMe-blue?style=for-the-badge)

</section>

## Índice
* [Enlace a la room](#enlace-a-la-room)
* [Introducción](#introducción)
* [¿Qué es la IAAA?](#qué-es-la-iaaa)
* [A01:Control de acceso fallido](#a01control-de-acceso-fallido)
* [A07:Fallos de autenticación](#a07fallos-de-autenticación)
* [A09:Registro y alerta de fallos](#a09registro-y-alerta-de-fallos)
* [Conclusión](#conclusión)

<section align="center">

## Enlace a la room
[![Room Link](https://img.shields.io/badge/Room-TryHackMe-red?style=for-the-badge&logo=tryhackme)](https://tryhackme.com/room/owasptopten2025one?utm_campaign=social_share&utm_medium=social&utm_content=share-completed-room&utm_source=copy&sharerId=67efdcfbe20c00d943ceceb9)


## Introducción

</section>

Esta room tiene como objetivo el aprendizaje y comprension sobre owasp top 10 que tienen como falla la implementacion del IAAA(Identidad, Autenticación, Autorización y Responsabilidad).

<section align="center">

## ¿Qué es la IAAA?

</section>
IAAA es una forma sencilla de entender cómo se verifican los usuarios y sus acciones en las aplicaciones.

Los cuatro elementos son:

- Identidad : la cuenta única (por ejemplo, ID de usuario/correo electrónico) que representa a una persona o servicio.
- Autenticación : comprobar la identidad (contraseñas, OTP, claves de acceso).
- Autorización : lo que esa identidad puede hacer.
- Responsabilidad : registro y alerta sobre quién hizo qué, cuándo y desde dónde.

### Responda las preguntas a continuación

- ¿Qué significa IAAA?

Respuesta: Identity, Authentication, Authorisation, Accountability

<section align="center">

## A01:Control de acceso fallido

</section>

El control de acceso fallido ocurre cuando el servidor no controla correctamente quién puede acceder a qué en cada solicitud. Un caso común es  IDOR (Referencia directa a objeto insegura): si al cambiar un ID (como ?id=7 → ?id=6) se pueden ver o editar los datos de otra persona, el control de acceso se ve afectado.

En la práctica, esto se manifiesta como una escalada de privilegios horizontal (mismo rol, cosas de otro usuario) o vertical (saltar a acciones solo de administrador) porque la aplicación confía demasiado en el cliente.

### Responda las preguntas a continuación

- Si no tiene acceso a más roles pero puede ver los datos de otros usuarios, ¿qué tipo de escalada de privilegios es esta?

Respuesta: Horizontal

- ¿Cuál es la nota que encontraste al ver la cuenta del usuario que tenía más de $1 millón?

Para obtener la respuesta, accede a la pagina estatica y cambia los id, juega con eso y lo encontraras!

<section align="center">

## A07:Fallos de autenticación

</section>

Los fallos de autenticación ocurren cuando una aplicación no puede verificar ni vincular de forma fiable la identidad de un usuario. Algunos problemas comunes son:

- enumeración de nombre de usuario
- Contraseñas débiles o adivinables (sin límites de bloqueo o velocidad)
- Fallas lógicas en el flujo de inicio de sesión/registro
- sesión insegura o manejo de cookies

Si alguno de estos está presente, un atacante a menudo puede iniciar sesión como otra persona o vincular una sesión a la cuenta incorrecta.

### Responda las preguntas a continuación

- ¿Qué es la bandera en el admintablero del usuario?

Para obtener la respuesta, crea una cuenta nueva y confude el servidor con la palabra aDmiN

<section align="center">

## A09:Registro y alerta de fallos

</section>

Cuando las aplicaciones no registran ni alertan sobre eventos relevantes para la seguridad, los defensores no pueden detectar ni investigar ataques. Un buen registro facilita la rendición de cuentas (poder demostrar quién hizo qué, cuándo y desde dónde). En la práctica, las fallas se manifiestan como la falta de eventos de autenticación, registros de errores imprecisos, la ausencia de alertas sobre ataques de fuerza bruta o cambios de privilegios, una retención corta o registros almacenados donde los atacantes pueden manipularlos.

### Responda las preguntas a continuación

- Parece que un atacante intentó realizar un ataque de fuerza bruta, ¿cuál es la IP del atacante?

Para encontrar la ip del atacante, busca en la pagina estatica la ip que se repite varias veces seguidas con un color rojo

- ¡Parece que lograron acceder a una cuenta! ¿Cuál es el nombre de usuario asociado a esa cuenta?

Baja un poco y veras un codigo de estado 200 en un inicio de sesion, ahi esta el usuario

- ¿Qué acción intentó realizar el atacante con la cuenta? Indique el punto final al que accedió.

El registro debajo del inicio de sesion aparece el directorio al cual se accedio.

<section align="center">

## Conclusión

</section>

Acaba de comprender los fundamentos de la identidad, la autenticación, la autorización y la responsabilidad en aplicaciones web y cómo pueden causar varias de las categorías de vulnerabilidades descritas en el Top 10 de OWASP : 2025. Las ideas clave que debe tener en cuenta son:

- A01 Control de acceso roto: Aplicar comprobaciones del lado del servidor en cada solicitud
- A07 Errores de autenticación: aplicar índices únicos en el formato canónico, limitar la velocidad/bloquear la fuerza bruta y rotar sesiones en caso de cambios de contraseña/privilegios.
- A09 Registro y alertas de fallas: registre todo el ciclo de autenticación (error/éxito, cambios de contraseña/2FA/rol, acciones de administrador), centralice los registros fuera del host con retención y alerte sobre anomalías (por ejemplo, ráfagas de fuerza bruta, elevación de privilegios).
