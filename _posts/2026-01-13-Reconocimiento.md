---
title: Reconocimiento Pasivo de Información
date: 2026-01-13 21:02:30 +/-TTTT
categories: [OSINT]
tags: [pentesting]     # TAG names should always be lowercase

description: Herramientas
toc: false
---

![Desktop View](/assets/img/reconocimiento/Que-es-ataque-pasivo-ciberseguridad_-scaled.jpg){: width="400" height="400" }

## 1. Identificación de una dirección IP del host del servidor que está alojando un sitio web 

```
host hackersploit.org

```
![Desktop View](/assets/img/reconocimiento/imagen1.jpeg){: width="400" height="400" }

## 2. Reconocimiento pasivo de una página web mediante pluguins como BuiltWith o Wappalyzer


![Desktop View](/assets/img/reconocimiento/imagen2.jpeg){: width="400" height="400" }
![Desktop View](/assets/img/reconocimiento/imagen3.jpeg){: width="400" height="400" }

## 3. Reconocimiento pasivo con whatweb que es utilizada en pentesting y análisis de seguridad web

```
whatweb hackersploit.org

```

![Desktop View](/assets/img/reconocimiento/imagen4.jpeg){: width="900" height="900" }

## 4. Clonar o descargar sitios web completos para su visualización y análisis en modo offline

```
sudo apt install webhttrack

```

![Desktop View](/assets/img/reconocimiento/imagen5.jpeg){: width="400" height="400" }

## 5. Recopilación de información respecto a un dominio 

![Desktop View](/assets/img/reconocimiento/imagen6.jpeg){: width="400" height="400" }

## 6. Investigar información acerca de un dominio en específico

![Desktop View](/assets/img/reconocimiento/imagen7.jpeg){: width="400" height="400" }

## 7. Identificar registros asociados a un dominio en particular a trasvés de dnsrecon y dnsdumpster para recopilación de información DNS

```
dnsrecon -d hackersploit.org 

```
![Desktop View](/assets/img/reconocimiento/imagen8.jpeg){: width="400" height="400" }
![Desktop View](/assets/img/reconocimiento/image.jpeg){: width="400" height="400" }

## 8. Analizar si hay waf ( web apllicaton firewall ) sobre el sitio web que deseo analizar:

![Desktop View](/assets/img/reconocimiento/imagen10.jpeg){: width="400" height="400" }

## 9. Enumerar subdominios de un sitio web usando OSINT que se hayan filtrado en internet a través de la herramienta sublister:

![Desktop View](/assets/img/reconocimiento/imagen10.jpeg){: width="400" height="400" }

```
sublist3r -d hackersploit.org

```

## 10. Google Dorks

Detectaa posibles paneles administrativos visibles públicamente dentro de un sitio web específico:

```
site:hackersploit.org inurl:admin

```
Localizar páginas administrativas visibles y claramente identificadas dentro de un sitio web, usando el título de la página como indicador:

```
site:hackersploit.org intitle:admin

```
Localiza documentos PDF públicos dentro de un sitio web (pueden ser otros tipos de archivos tambièn), que pueden revelar información valiosa para OSINT y auditorías de seguridad.

```
site:hackersploit.org filetype:pdf

```
Detectar directorios abiertos que pueden exponer archivos sensibles debido a una mala configuración del servidor web:

```
intitle: index of

```
Detecta archivos de texto potencialmente críticos que pueden contener contraseñas expuestas públicamente por mala configuración:

```
inurl: password.txt
inurl: passwd.txt

```

## 11. Enumerar una versión anterior de un sitio web en específico y ver como se veía antes con wayback machine

![Desktop View](/assets/img/reconocimiento/imagen11.jpeg){: width="400" height="400" }

## 12. Repositorio público que recopila Google Dorks (consultas avanzadas) usados para encontrar información sensible expuesta en Internet mediante buscadores

Link: https://www.exploit-db.com/google-hacking-database


![Desktop View](/assets/img/reconocimiento/Screen-Shot-2018-11-23-at-2.17.09-PM.png){: width="400" height="400" }


## 13. Listar subdominios y direcciones IP (theHarvester)


```
theHarvester -d hackersploit.org -b yahoo,duckduckgo,dnsdumpster,bing,urlscan
```

![Desktop View](/assets/img/reconocimiento/imagen12.jpeg){: width="400" height="400" }


## 14. Investigar si algún correo electrónico ha sido filtrado o si ha caído en alguna brecha de datos

Link: https://haveibeenpwned.com/

![Desktop View](/assets/img/reconocimiento/imagen13.jpeg){: width="400" height="400" }

