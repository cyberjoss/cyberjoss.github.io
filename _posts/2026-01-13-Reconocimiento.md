---
title: Reconocimiento Pasivo de Información
date: 2026-01-13 21:02:30 +/-TTTT
categories: [OSINT]
tags: [pentesting]     # TAG names should always be lowercase

description: Herramientas
toc: false
---

![Desktop View](/assets/img/reconocimiento/Que-es-ataque-pasivo-ciberseguridad_-scaled.jpg){: width="400" height="400" }

## 1. Identificación de una dirección IP del host del servidor que está alojando un sitio web (host):

```
host hackersploit.org

```
![Desktop View](/assets/img/reconocimiento/imagen1.jpeg){: width="400" height="400" }

Herramienta de línea de comandos que permite resolver nombres de dominio a direcciones IP y obtener información sobre los servidores que alojan un sitio web. Se utiliza en la fase de reconocimiento y recopilación de información para identificar la infraestructura de red de un objetivo.

## 2. Reconocimiento pasivo de una página web mediante pluguins (BuiltWith o Wappalyzer):


![Desktop View](/assets/img/reconocimiento/imagen2.jpeg){: width="400" height="400" }
![Desktop View](/assets/img/reconocimiento/imagen3.jpeg){: width="400" height="400" }

Herramientas de reconocimiento pasivo que permiten identificar las tecnologías utilizadas por una página web, como frameworks, lenguajes, CMS, servidores y librerías, sin interactuar directamente con el sistema, apoyando la fase de recolección de información en ciberseguridad.

## 3. Reconocimiento pasivo con whatweb que es utilizada en pentesting y análisis de seguridad web:

```
whatweb hackersploit.org

```

![Desktop View](/assets/img/reconocimiento/imagen4.jpeg){: width="900" height="900" }

Herramienta de reconocimiento web que permite identificar tecnologías, frameworks, CMS y configuraciones utilizadas por un sitio web mediante el análisis de cabeceras y contenido HTTP, apoyando la fase de recolección de información y enumeración en ciberseguridad.

## 4. Clonar o descargar sitios web completos para su visualización y análisis en modo offline:

```
sudo apt install webhttrack

```

![Desktop View](/assets/img/reconocimiento/imagen5.jpeg){: width="400" height="400" }

Herramienta que permite clonar y descargar sitios web completos para su análisis y visualización en modo offline, útil para revisar la estructura, recursos y posibles puntos de interés durante tareas de reconocimiento y análisis web en ciberseguridad.

## 5. Recopilación de información respecto a un dominio:

```
whois hackersploit.org
```

![Desktop View](/assets/img/reconocimiento/imagen6.jpeg){: width="400" height="400" }

Herramienta utilizada para la recopilación de información pública de un dominio, como datos de registro, fechas, servidores DNS y entidad registradora, apoyando la fase de reconocimiento y análisis inicial en ciberseguridad.

## 6. Investigar información acerca de un dominio en específico:

Sitio: https://sitereport.netcraft.com/

![Desktop View](/assets/img/reconocimiento/imagen7.jpeg){: width="400" height="400" }

Plataforma de reconocimiento pasivo que permite investigar información detallada sobre un dominio, como tecnologías utilizadas, servidor web, proveedor de hosting, historial de cambios y estado de seguridad, apoyando la fase de recolección de información y análisis de infraestructura en ciberseguridad.

## 7. Identificar registros asociados a un dominio en particular a trasvés de dnsrecon y dnsdumpster para recopilación de información DNS:

```
dnsrecon -d hackersploit.org 

```
![Desktop View](/assets/img/reconocimiento/imagen8.jpeg){: width="400" height="400" }
![Desktop View](/assets/img/reconocimiento/image.jpeg){: width="400" height="400" }

Herramientas de recopilación de información DNS que permiten identificar registros asociados a un dominio (A, MX, NS, TXT, subdominios), facilitando el análisis de la infraestructura y servicios expuestos durante la fase de reconocimiento en ciberseguridad.

## 8. Analizar si hay waf ( web apllicaton firewall ) sobre el sitio web que deseo analizar:

```
wafw00f hackersploit.org
```

![Desktop View](/assets/img/reconocimiento/imagen10.jpeg){: width="400" height="400" }

Herramienta de reconocimiento web utilizada para detectar la presencia y el tipo de Web Application Firewall (WAF) que protege un sitio web, mediante el análisis de respuestas HTTP, apoyando la fase de identificación de mecanismos de seguridad en ciberseguridad.

## 9. Enumerar subdominios de un sitio web usando OSINT que se hayan filtrado en internet a través de la herramienta sublister:


```
sublist3r -d hackersploit.org

```

![Desktop View](/assets/img/reconocimiento/imagen10.jpeg){: width="400" height="400" }

Herramienta de reconocimiento utilizada para enumerar subdominios asociados a un dominio mediante fuentes OSINT, permitiendo identificar servicios y puntos de entrada potenciales durante la fase de recolección de información en ciberseguridad.

## 10. Google Dorks:

Detectar posibles paneles administrativos visibles públicamente dentro de un sitio web específico:

```
site:hackersploit.org inurl:admin

```
Localizar páginas administrativas visibles y claramente identificadas dentro de un sitio web, usando el título de la página como indicador:

```
site:hackersploit.org intitle:admin

```
Localizar documentos PDF públicos dentro de un sitio web (pueden ser otros tipos de archivos tambièn), que pueden revelar información valiosa para OSINT y auditorías de seguridad.

```
site:hackersploit.org filetype:pdf

```
Detectar directorios abiertos que pueden exponer archivos sensibles debido a una mala configuración del servidor web:

```
intitle: index of

```
Detectar archivos de texto potencialmente críticos que pueden contener contraseñas expuestas públicamente por mala configuración:

```
inurl: password.txt
inurl: passwd.txt

```

## 11. Enumerar una versión anterior de un sitio web en específico y ver como se veía antes:

sitio: https://web.archive.org/

![Desktop View](/assets/img/reconocimiento/imagen11.jpeg){: width="400" height="400" }

Herramienta de reconocimiento pasivo que permite consultar versiones anteriores de un sitio web, analizar su evolución, estructura y contenido histórico, útil para la recolección de información y detección de cambios en auditorías de ciberseguridad.

## 12. Repositorio público que recopila Google Dorks (consultas avanzadas) usados para encontrar información sensible expuesta en Internet mediante buscadores:

Sitio: https://www.exploit-db.com/google-hacking-database

![Desktop View](/assets/img/reconocimiento/Screen-Shot-2018-11-23-at-2.17.09-PM.png){: width="400" height="400" }

Repositorio público que recopila Google Dorks (consultas avanzadas) utilizadas para identificar información sensible expuesta en Internet, como archivos, paneles o configuraciones inseguras, apoyando tareas de OSINT y reconocimiento en ciberseguridad.

## 13. Listar subdominios y direcciones IP:

```
theHarvester -d hackersploit.org -b yahoo,duckduckgo,dnsdumpster,bing,urlscan
```

![Desktop View](/assets/img/reconocimiento/imagen12.jpeg){: width="400" height="400" }

Herramienta de reconocimiento OSINT utilizada para listar subdominios, direcciones IP y correos electrónicos asociados a un dominio, consultando múltiples fuentes públicas, apoyando la fase de recolección de información y mapeo de la superficie de ataque en ciberseguridad.

## 14. Investigar si algún correo electrónico ha sido filtrado o si ha caído en alguna brecha de datos

Link: https://haveibeenpwned.com/

![Desktop View](/assets/img/reconocimiento/imagen13.jpeg){: width="400" height="400" }

Plataforma de reconocimiento pasivo que permite verificar si un correo electrónico ha sido comprometido en filtraciones o brechas de datos públicas, ayudando a evaluar riesgos de exposición de credenciales e información sensible en ciberseguridad.

