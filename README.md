# Índice    
- [Introducción](#introducción)
- [Objetivos](#objetivos)
- [Proceso unificado de desarrollo (RUP)](#proceso-unificado-de-desarrollo-rup)
- [Modelo del dominio](#modelo-del-dominio)
- [Disciplina de requisitos](#disciplina-de-requisitos)
  - [Actores y casos de uso](#actores-y-casos-de-uso)
    - [Casos de uso para los administradores](#casos-de-uso-para-los-administradores)    
    - [Casos de uso para los usuarios](#casos-de-uso-para-los-usuarios)
- [Referencias](#referencias)

# Introducción 
En este proyecto, desarrollaré Flixxic, un sitio web y aplicación móvil enfocados en películas y series, con el objetivo de adquirir experiencia en el desarrollo de software y mejorar mis habilidades en tecnologías como Git, GitHub, Angular, Java y Spring Boot y otras tecnologías. Para lograr este propósito, implementaré el proceso de desarrollo RUP y profundizaré en las arquitecturas de aplicaciones web y móviles.

# Objetivos
- Crear un sitio web y una aplicación móvil de películas y series.
- Ganar experiencia en el desarrollo de software.
- Mejorar mis habilidades con Git, GitHub, Angular, Java y Spring Boot y demás tecnologías.
- Aprender a utilizar el proceso de desarrollo RUP.
- Profundizar en las arquiteturas de aplicaciones web y móviles.

# Proceso unificado de desarrollo (RUP)
El proceso de desarrollo Rational Unified Process (RUP) es un conjunto de actividades que ayudan a transformar los requisitos de un usuario en un sistema software. Además, RUP también es un marco de trabajo genérico que puede especializarse para una gran variedad de sistemas software.

Los tres aspectos más importantes en RUP son:
 1. Que está dirigido por casos de uso
 2. Está centrado en la arquitectura y 
 3. Es un proceso iterativo incremental. 

Además, se utiliza UML para preparar los esquemas que representan el sistema software. 

Al final un proyecto que hace uso de RUP se ve de la siguiente manera:
![RUP](https://github.com/vfred0/requirements-flixxic/blob/main/images/rup/disciplines.png?raw=true)

En dónde se obtiene 5 disciplinas o flujos, los cuales son los modelos de: 
- Casos de uso
- Análisis
- Diseño 
- Despliegue
- Implementación
- Pruebas

y cada disciplina se divide en 4 fases: 
- Inicio
- Elaboración
- Construcción 
- Transición

![RUP](https://github.com/vfred0/requirements-flixxic/blob/main/images/rup/phases.png?raw=true)

Al final, no estaré siguiendo al pie de la letra el proceso de desarrollo RUP, pero si tomaré en cuenta los aspectos más importantes.

# Modelo del dominio
Describe los conceptos más importantes del contexto del sistema como son:
- Objetos de negocio
- Objetos del mundo real y conceptos que un sistema necesita hacer un seguimiento
- Eventos que suceden o que sucederán en el sistema

Asimismo nos permite tener un vocabulario común entre los desarrolladores, clientes y usuarios, con la finalidad de evitar malentendidos.

Para el caso de Flixxic, el modelo del dominio se ve de la siguiente manera:
![Modelo de dominio](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/0-domain-model/domain-model.svg?raw=true)

# Disciplina de requisitos
## Actores y casos de uso
Los actores son los usuarios que interactúan con el sistema y los casos de uso son las acciones que pueden realizar los actores.

Para el caso de Flixxic, los actores serám administradores y usuarios. Los administradores son los usuarios que se encargan de gestionar el contenido, mientras que los usuarios son los que interactúan con el contenido.

### Casos de uso para los administradores

| Autenticación | Gestión del contenido |
| --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/admin/authentication.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/admin/content-management.svg?raw=true) |

### Casos de uso para los usuarios

Los usuarios podrán realizar las siguientes interacciones con el contenido:

| Autenticación | Gestión del perfil | Notificaciones |
| --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/authentication.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/profile-management.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/notifications.svg?raw=true) |

| Ver detalles, buscar y filtrar | Comentar | Calificar |
| --------- | --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/view-search-filter.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/comments.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/reviews.svg?raw=true) |

| Favoritos | Ver más tarde | Historial |
| --------- | --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/favorites.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/watch-later.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/history.svg?raw=true) |

# Referencias
Para llevar a cabo este proyecto, he utilizado como referencia los siguientes proyectos y agradezco a los autores por compartirlos:

- [Gestor de taller mecánico AgrimManager](https://www.notion.so/Gestor-de-taller-mec-nico-AgrimManager-a8d44826c2494e15bcb235fc1019938d#cd3ccf181d9c4a1b9253416cd9b74f57)
- [HalteroCMS](https://github.com/zuldare/mastercloud_pfm_halterocms)
- [Master EscuelaIT](https://github.com/USantaTecla-0-general/3-publicaciones)