---
title: '¿Qué es cloud computing?'
date: 2022-02-08
tags: ['cloud computing', 'software engineering', DevOps]
draft: false
summary: 'Introducción a los fundamentos del cloud computing y su importancia clave en la industria'
---

# ¿Qué es cloud computing?

El término *cloud computing* es uno de los que generan más confusión para quienes van iniciando en el mundo del desarrollo en nuestros días. En universidades no se usa todavía mucho este concepto. Yo mismo pase mucho tiempo escuchándolo pero sin entender bien a qué se refería. En este blogpost pretendo explicar los fundamentos clave del **cloud computing** para así tener un contexto general que nos ayude a entender el *state of the art* del desarrollo de software actual. 

> **Disclaimer:** dentro del post se usa el término en inglés ***cloud*** o en español ***nube*** indistintamente.
> 

## Que es cloud computing?

Una de las razones por la que el concepto de cloud computing es difícil de digerir es porque de igual manera es difícil de definir. Como es común en temas de software engineering puede significar varias cosas. En términos prácticos, y de acuerdo a la forma que más se usa en la actualidad podemos decir que cloud computing es: la disponibilidad de recursos computacionales que ofrece en internet un proveedor de servicios cloud. Estos recursos pueden ser bases de datos, networking, almacenamiento, etc. 

> 💡  ¿Se te viene uno a la mente en este momento? Pista: Amazon, Google, Microsoft ofrecen estos servicios.
> 

## **Antecedentes del cloud computing**

Conforme el número de usuarios de la web fue aumentando a principios del siglo XXI fue necesario la construcción de *data centers* alrededor del mundo que pudieran manejar millones de requests por día. *Data centers* son edificios específicamente construidos para albergar cientos de servidores. Estos servidores permitieron el soporte, y disponibilidad en todo el mundo, de los primeros productos basados en cloud como la tienda de amazon, gmail, etc.

En los primeros años de los 2000s los ingenieros de amazon propusieron que separar la arquitectura de la infraestructura permitiría mayor flexibilidad al momento de buscar la escalabilidad y redundancia de sus servicios. 

Una vez probado el modelo en amazon se pensó que ofrecer esta modalidad sería de gran interés para otras compañías. Así nació **AWS** *Amazon Web Services* que es el servicio cloud mas usado en la actualidad. 

## Qué podemos hacer con cloud computing?

En la actualidad una vasta cantidad de compañías están moviendo sus servicios a la nube. Startups que están iniciando optan por tener todas las operaciones de su negocio en estos servicios. 

> 💡 **¿Por qué?** Como veremos repetidamente a los largo del post, tiene que ver principalmente con una lógica de costo-beneficio para un proyecto/negocio.
> 

Vamos a revisar algunas de las mas cruciales. 

### **Storage**

Debido a la gran cantidad de *data* que manejan las aplicaciones modernas los días en que las compañías tenían sus gabinetes donde guardaban su información están quedando atrás. La capacidad de almacenamiento de los servicios en la nube son muy superiores a los que una compañía por sí sola puede tener. Por ejemplo, imagina una ***start-up*** que va iniciando y tiene un capital limitado. En términos de escalabilidad también resulta en costos más reducidos utilizar almacenamiento *on demand,* es decir, subir la capacidad conforme tu aplicación lo va requiriendo.

### **Analytics**

Para analizar un gran cantidad de *raw data* necesitamos una gran cantidad de poder de computo.   Utilizar este servicio, a un bajo costo, es una ventaja competitiva para cualquier negocio. 

### **Infrastructure**

Para una compañía tener sus propios servidores para sustentar sus aplicaciones requiere una fuerte inversion, costo de mantenimiento y operación. **¿**Para qué comprar inicialmente una oficina si la puedes rentar?

## Por que usar cloud computing?

Cómo hemos visto hasta el momento utilizar servicios en la nube tiene una predominante razón de negocio costo-beneficio. 

Tener tu propia infraestructura requiere la compra, configuración, mantenimiento de servidores que corran nuestros servicios.

Los proveedores de cloud tienen sus data centers en diversas locaciones alrededor del mundo. Esto quiere decir que tu servicio puede tener alta disponibilidad en todo el mundo.  

## Cuales son las desventajas del cloud computing?

Como en cada decisión en el desarrollo de software hay algunos trade-offs que considerar. Si bien, utilizar servicios cloud es mas óptimo en términos de costo-beneficio, nuestra operación depende de servicios de terceros. 

Por ejemplo cuando un servicio de un proveedor cloud falla las compañías que los usan tienen poco que hacer. La falla en cuestión y su arreglo no depende de ellos. 

Los datos de un negocio están alojados en un servidor de un tercero. 

El manejo de servicios cloud puede ser complejo en operación. Se necesita un entrenamiento especifico para usar la infraestructura de cada proveedor.  

Esto es algo a sopesar para los tomadores de desiciones en una compañía. 

## Cuales son las opciones de trabajo en cloud computing?

Con el incremento de la utilización de servicios cloud en la industria, han surgido en los últimos años nuevos roles. Cada uno de estos se especializa en diferentes aspectos del uso, en una compañía, de los diferentes servicios cloud. 

Vamos a revisar algunos de los mas populares para que tengamos una idea la próxima vez que los escuchemos en juntas, cursos, ofertas de trabajo, etc.

### **Cloud Developer**

Se encarga de desarrollar funcionalidades mediante la integración de servicios cloud en una aplicación. Comúnmente, utilizan lenguajes de programación como Go o python. 

### **Cloud Administrator**

Crea y maneja los servicios a utilizar por el cloud developer. Se enfoca más en la configuración y mantenimiento. 

### **Cloud Architect**

Este rol es el responsable de diseñar y construir sistemas cloud. Es decir, determina los servicios a usar y como se conectan entre sí. Es responsable de la estrategia a un alto nivel. 

### **SecOps (Security Operations) / Cloud Security Engineer**

Como su nombre lo expresa, este role se encarga de reducir las vulnerabilidades de nuestra infraestructura en la nube. Evita ataques externos. Y, protege los datos de la organización. Esto se logra previniendo un mal uso de esta controlando el acceso a los servicios cloud. 

Este rol requiere de un avanzado conocimiento en redes, privacidad de datos y mejores prácticas en términos de seguridad informática. 

### **FinOps (Financial Operations) / Cloud Financial Engineer**

Se encarga de optimizar los costos de mantenimiento de los servicios en la nube. Imagina una empresa con millones de usuarios diarios y por consiguiente la necesidad de infraestructura que soporte tal operación. Tiene sentido tener roles especializados que se encarguen de utilizar los recursos, en términos de costos, de la mejor manera.

### **DevOps (Development Operations) / Site Reliability Engineer**

Este rol que se ha vuelto muy popular en los últimos años requiere todo un post en sí mismo que vendrá en un futuro próximo. Por el momento vamos a dar una visión general.

El DevOps combina sus conocimientos en infraestructura y desarrollo, con énfasis en la automatización, para crear y mejorar procesos que optimicen un sistema. El DevOps necesita un fuerte conocimiento de las etapas de desarrollo así como de las herramientas - o ***tooling -*** que se usan durante estas. Algunas de estas herramientas son: *kubernetes*, *Docker, Git, Jenkins.*

Estos son algunas de las tareas importantes de un DevOps:

- **CI/CD Pipelines:** Se refiere a una serie de pasos para realizar cambios a un proyecto automáticamente, hacer built, testing y deployed.
- **Monitoring:** Proporcionar un flujo de información de los sistemas a los desarrolladores.
- **Resiliency:** Asegurar que los sistemas funcionen incluso en condiciones adversas.

> 💡 La clave de un DevOps es incrementar la productividad de todo el equipo de ingeniería.
> 

## Tipos de servicios cloud

Con la explosión de servicios cloud que se ofertan en los últimos años es fácil confundirse sobre lo que ofrece cada proveedor. Para solventar este hecho, podemos seleccionarlos en cuatro categorías de servicios. 

### **Software as a Service (SaaS)**

El ***software as a service*** o ***saas*** son aplicaciones que están disponibles en internet. El usuario no necesita instalar nada en su propia computadora. Todo el procesamiento y guardado de datos suceden en la nube.  

Los beneficios palpables son que un negocio pequeño puede tener acceso a software a un ínfimo precio de lo que costaría un desarrollo propio. Ademas no necesita instalaciones, configuraciones, mantenimiento ni actualizaciones. 

**Ejemplos**

- Google Docs
- Dropbox
- Gmail

### **Platform as a Service (PaaS)**

Imaginemos que tenemos una aplicación que queremos desplegar en internet pero nuestro conocimiento en infraestructura y operación es escaso. S*ería* bueno tener un servicio que simplificara el despliegue de nuestro desarrollo en internet y que así este disponible para todo el mundo. 

Bueno, eso es justo lo que busca resolver una PaaS.

**Ejemplos**

- Heroku
- Vercel
- Azure app service
- AWS Elastic BeanStalk

### **Infrastructure as a Service (IaaS)**

Como su nombre lo indica, ***infrastructure as a service*** nos ofrece la oportunidad de manejar la infraestructura que necesitamos de manera virtual a través de tooling y APIs. Se podría decir que ofrece un manejo más directo y configurable, que una ***PaaS,*** para cumplir con las necesidades de una empresa. Por lo mismo, se requiere de un conocimiento más especializado para administrar la infraestructura. 

**Ejemplos**

- Amazon EC2 (Elastic Cloud Compute)
- Google Compute Engine
- Azure Virtual Machines

## Cloud providers

Al principio de este post mencionamos que cloud computing se refería a los servicios que ofrecen en internet diversos proveedores. 

Un proveedor cloud es una compañía que ofrece su infraestructura y poder de computo a otras compañías. 

Algo importante a entender es que los proveedores tiene un modelo de pago ***pay-per-use***. Esto significa que la compañía usuaria del servicio paga de acuerdo a lo que utiliza. 

Los principales proveedores de servicios en la nube. 

### **AWS (Amazon Web Services)**

Tal vez el mas conocido y el que domina el mercado actualmente. También, fue de los primeros en ofrecer este tipo de servicios. Su oferta es la más amplia del mercado por lo que se requiere de una amplio conocimiento de esta. 

Una desventaja es que la complejidad en la estructura de precios es muy alta. 

### **Microsoft Azure**

El servicio en la nube de Microsoft también tiene una amplia oferta con cientos de servicios disponibles. La desventajas que reportan algunos usuarios son trainings no tan buenos para el manejo de la plataforma y un deficiente servicio al cliente. 

### **GCP (Google Cloud Platform)**

Ofrece una estructura de precios sencilla y ofrece los precios más reducidos. Tiene herramientas muy especializadas para machine learning y big data. Por otro lado ofrece menos servicios que aws o azure. También algo a remarcar es que tiene menos data centers a través del mundo. 

### Digital Ocean

Es el que uso yo en mi día a día. El target de Digital Ocean son grupos reducidos de developers. Busca la rapidez y facilidad de uso por parte de estos para crear aplicaciones en la nube. 

Otros servicios que podríamos listar y que tienen sus propias especializaciones son: Oracle cloud, Red Hat Cloud Services, Alibaba Cloud. 

---

Estos fueron algunos de los fundamentos del ***cloud computing*** que nos ayuda a tener ******un ******contexto ******amplio de esta importante área que domina la industria del desarrollo actual. En futuros posts profundizaremos en algunos de estos temas.