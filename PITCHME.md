@title[Dirhunt]

![TIP](https://raw.githubusercontent.com/Nekmo/dirhunt/develop/docs/_static/logo.png)
<br>
@css[project-name](DIRHUNT)
@css[template-note](Busca directorios sin fuerza bruta)

---?image=assets/image/bg/gray.jpg&position=top&size=100% 20%
@title[sobre-mi]

@snap[north text-white span-100]
@size[1.5em](Mi perfil en Github)
@snapend

![TIP](assets/image/github_nekmo.png)


Note:
Buenas, soy **Juan José**, conocido en Github como **Nekmo** y llevo 13 años desarrollando en Python; estoy 
especializado en seguridad informática en Hispasec Sistemas.

---?image=assets/image/bg/orange.jpg&position=bottom&size=100% 20%
@title[github-dirhunt]

@snap[south text-white span-100]
@size[1.5em](Repositorio de Dirhunt en Github)
@snapend

![TIP](assets/image/github_dirhunt.png)

Note:
A parte, en mi tiempo libre desarrollo Dirhunt, una herramienta para descubrir contenido de aplicaciones web, la cual 
es software libre y puede encontrarse en Github. 

---?image=assets/image/bg/blue.jpg&position=left&size=40% 100%
@title[github-stars]

@snap[west west-30 text-18 text-bold text-italic text-white span-30]
Más de 600 estrellas
@snapend

@snap[east]
@img[github-stars span-100](assets/image/github_stars.png)
@snapend

Note:
Ha tenido una buena acogida y a día de hoy se puede considerar un proyecto maduro.

---?image=assets/image/bg/blue.jpg&position=right&size=70% 100%
@title[otras-herramientas]


@snap[east span-50 text-24 text-white text-bold]
¿En qué se diferencian?
@snapend

Note:
¿Pero en qué se diferencia esta herramienta?

(listar otras alternativas como Cansina)

---?color=#36454F
@title[fuerza-bruta]

```text
http://dominio/AAAAAAA.php
               AAAAAAB.php
               AAAAAAC.php
```
@[1](Meec! 404: Not found.)
@[2](Meeeeec! 404: Not found.)
@[3](MEEEEEEEEEC!! 429: To Many Requests.)


Note:
Estas herramientas normalmente realizan fuerza bruta desde un diccionario, lo cual requiere muchos intentos. Vamos, 
**algo que podría hacer un mono**.

---?image=assets/image/monkey.webp
@title[mono]
   
@snap[north-east text-white]
O más bien, este mono
@snapend

---?image=assets/image/bg/purple.jpg&position=center&size=100% 65%
@title[como-funciona]

@snap[center-center span-100 text-white]
@size[2.1em](Cómo funciona)
@snapend

Note:
¿Pero cómo funciona Dirhunt y qué es lo que hace lo hace diferente?

---
@title[peticiones-dirhunt]

![TIP](assets/image/peticiones-dirhunt.png)

Note:
En cambio, Dirhunt es un crawler que analiza el contenido para encontrar nuevas rutas.

---?color=black
@title[procesado-peticiones]

@snap[north-west span-40]
@box[bg-green text-white box-wide-padding](1. Páginas#Se procesa el contenido)
@snapend

@snap[north-east span-40]
@box[bg-orange text-white box-wide-padding rounded](2. Enlaces#Nuevas páginas y assets)
@snapend

@snap[south-east span-40]
@box[bg-pink text-white box-wide-padding](3. Assets#Se procesan y busca más rutas)
@snapend

@snap[south-west span-40]
@box[bg-blue text-white box-wide-padding waved](4. Carpetas#Se analizan las carpetas a los paths)
@snapend

@snap[midpoint]
@fa[refresh fa-3x]
@snapend


Note:
Recorre los directorios de los assets de la página. Sigue los enlaces internos de la web para encontrar nuevas 
páginas. **¿Y para qué sirve esto?**

---?image=assets/image/bg/black.jpg&position=top&size=100% 20%
@title[asciinema]

@snap[north text-white span-100]
@size[1.5em](En acción)
@snapend

@snap[south span-80]
[![asciicast](https://asciinema.org/a/xPJXT0MhrvlZ8lJYJYkjxlice.png)](https://asciinema.org/a/xPJXT0MhrvlZ8lJYJYkjxlice)
@snapend


---?image=assets/image/bg/pink.jpg&position=top&size=100% 20%
@title[otras-herramientas]

@snap[north-west span-100 text-white]
@size[1.5em](Usos)
@snapend

@snap[center-west list-content-concise span-100]
@ul
- Revelar los directorios del sitio.
- Detectar plugins e información del software.
- Encontrar malware y ficheros de configuración.
- ... Entre otras cosas.
@ulend
@snapend

Note:
 (leer listado) ... Por ejemplo, tengo un amigo que lo usa para obtener información de   
sitios web para SEO.

---?color=#222222
@title[uso-practico]

@snap[north span-100 text-white]
@size[1.5em](Uso práctico)
@snapend

@snap[west span-35 text-shell]
@size[2.7em](Shells)
@snapend

@img[east span-70](assets/image/shell.png)


---?image=assets/image/bg/pink.jpg&position=bottom&size=100% 20%
@title[index-of]

@snap[zoom-08]
![TIP](assets/image/index_of.png)
@snapend

@snap[south text-white span-100]
@size[1.5em](Index Of, de lo más útil)
@snapend

Note:
Pero cuando Dirhunt es especialmente potente, es en aquellos sitios con el Index Of habilitado. 

---?image=assets/image/bg/green.jpg&position=center&size=100% 65%
@title[otras-fuentes]

@snap[center-center span-100 text-white]
@size[1.2em](¿Pero qué pasa si no hay assets, enlaces ni Index Of habilitado?)
@snapend

Note:
Pero por si no hay formas de obtener enlaces ni carpetas de la página principal, también tiene otros trucos:

---?image=assets/image/bg/blue.jpg&position=left&size=40% 100%
@title[otras-fuentes-google]

@snap[west west-30 text-18 text-bold text-white span-30]
Google
@snapend

@snap[east]
![TIP](assets/image/google_search.png)
@snapend

Note:
También realiza una búsqueda en Google con el dominio para obtener carpetas.

---?image=assets/image/bg/purple.jpg&position=right&size=40% 100%
@title[otras-fuentes-virustotal]

@snap[east span-30 text-align-left text-24 text-white text-bold]
Virus Total
@snapend

@snap[west zoom-08]
![TIP](assets/image/virustotal_search.png)
@snapend

Note:
Busca en VirusTotal por el dominio.

---?image=assets/image/bg/blue.jpg&position=left&size=40% 100%
@title[otras-fuentes-robots]

@snap[west text-18 text-bold text-white span-30]
Robots.txt
@snapend


```text
User-agent: googlebot
Disallow: /directory1/
Disallow: /directory2/
Allow: /directory2/subdirectory1/
```


Note:
El robots.txt suele tener directorios interesantes, y también los usa para encontrar más directorios.

---
@title[previo-resultados]

@snap[west span-40]
@size[2.7em](Detecta y filtra)
@snapend


@snap[north-east span-60 fragment]
@box[bg-pink text-white box-narrow-padding](Falsos 404.#Si una carpeta devuelve 404, pero tiene subarchivos.)
@snapend

@snap[east span-60 fragment]
@box[bg-orange text-white box-narrow-padding](Páginas en blanco.#Suelen usarse para ocultar en directorios.)
@snapend

@snap[south-east span-60 fragment]
@box[bg-purple text-white box-narrow-padding](Filtrar.#Devolver sólo los falsos 404, que usan páginas en blanco, etc.)
@snapend


---?image=assets/image/bg/yellow.jpg&position=top&size=100% 20%
@title[reporte-resultados]

@snap[north text-white span-100]
@size[1.5em](Reporte de resultados)
@snapend

![TIP](assets/image/results.png)

Note:
Finalmente, los resultados son mostrados al final junto con un resumen, y el tamaño y la fecha si el fichero viene de  
un Index Of.

---
@title[opciones-peticion-2]

@snap[east span-40 text-align-left]
@size[2.3em padding-left-05](Opciones petición)
@snapend

@snap[north-west span-60 fragment]
@box[bg-pink text-white box-narrow-padding](Proxies.#Define uno o varios proxies.)
@snapend

@snap[west span-60 fragment]
@box[bg-orange text-white box-narrow-padding](Delay.#Define un delay entre peticiones.)
@snapend

@snap[south-west span-60 fragment]
@box[bg-purple text-white box-narrow-padding](Proxies incluidos.#Búsqueda automática de proxies gratuitos, aleatorios o por países.)
@snapend


---?color=#36454F
@title[instalar]


```
$ sudo pip3 install dirhunt
```

@snap[south]
O haz tu fork de [Nekmo/dirhunt](https://github.com/Nekmo/dirhunt) en Github.
@snapend


---
@title[presentación]

## ¿Y la presentación?

[github: Nekmo/dirhunt-presentacion](https://github.com/Nekmo/dirhunt-presentacion)

---
@title[contactar]


@snap[west contact-links]
@css[contact-name](Nekmocom)<br>
<a href="https://github.com/gitpitch/gitpitch">
@fa[github-square pad-right-icon]@css[git-handle](Nekmo)
</a><br>
<a href="https://twitter.com/nekmocom">
@fa[twitter-square pad-right-icon]@css[twitter-handle](@nekmocom)
</a><br>
<a href="mailto: david@gitpitch.com">
@fa[envelope-o pad-right-icon]@css[contact-email](contacto@nekmo.com)
</a>
@snapend

@snap[east span-50]
![](assets/image/contact-1.png)
@snapend

@snap[north-east template-note text-gray]
Formas de contacto.
@snapend
