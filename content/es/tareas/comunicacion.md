---
title: "Comunicación cliente servidor"
date: 2021-11-11T19:39:33+02:00
draft: false
---
## Proceso de carga de una página web

![Foto de perfil](/images/pc.png)

En está página vamos a describir el proceso de carga desde que un usuario teclea una url en el navegador hasta que recibe la información de ese sitio web.


{{<mermaid align="left">}}
graph LR;
  Cliente-->|solicitud| Servidor;
{{< /mermaid >}}

{{<mermaid align="left">}}
graph LR;
  Servidor-->|respuesta| Cliente;
{{< /mermaid >}}

LA web se compone de :

**Servidor**: donde están los datos y la lógica de la aplicación.
**Cliente**: donde se encuentra el usuario final con su navegador.
**Red**: los protocolos de comunicación http o https.

Un cliente (un navegador web) solicita un recurso a un servidor web a través de una interfaz, usando un protocolo.

De esa url, dependiendo del protocolo (https por ejemplo), sabremos por qué puerto va a ir la solicitud.
Después consultará al DNS para que nos diga la IP de esa máquina, y una vez que tenga la IP hará la solicitud al puerto.

![Modelo cliente-servidor](/images/comunicacion1.jpeg)

Cuando llega la solicitud al servidor y localiza el recurso a mostrar, hará lo que tenga que hacer. Por ejemplo: el módulo correspondiente para ejecutar el lenguaje de programación, la conexión con la base de datos, la conexión con el webservice...

COn toda esta información, responderá al cliente en el puerto que esté abierto.

EL cliente, en su máquina será quien gestione el css y ejecutará la parte javascript.

Cuando tenga toda la información se la mostrará al navegador (cliente).


