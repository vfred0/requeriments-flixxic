# Índice    
- [Introducción](#introducción)
- [Objetivos](#objetivos)
- [Proceso unificado de desarrollo (RUP)](#proceso-unificado-de-desarrollo-rup)
- [Modelo del dominio](#modelo-del-dominio)
- [Disciplina de requisitos](#disciplina-de-requisitos)
  - [Actores y casos de uso](#actores-y-casos-de-uso)
    - [Casos de uso para los administradores](#casos-de-uso-para-los-administradores)    
    - [Casos de uso para los usuarios](#casos-de-uso-para-los-usuarios)
    - [Contexto de casos de uso](#contexto-de-casos-de-uso)
  - [Especificar casos de uso](#especificar-casos-de-uso)
  - [Prototipar la interfaz de usuario](#prototipar-la-interfaz-de-usuario)
- [Disciplina de análisis](#disciplina-de-análisis)
  - [Analizar la arquitectura](#analizar-la-arquitectura)
- [Disciplina de diseño](#disciplina-de-diseño)
  - [Diseñar la arquitectura](#diseñar-la-arquitectura)  
- [Referencias](#referencias)

# Introducción 
En este proyecto, desarrollaré Flixxic, una aplicación web de películas y series, con el objetivo de adquirir experiencia en el desarrollo de software y mejorar mis habilidades en tecnologías como Git, GitHub, Angular, Java y Spring Boot y otras tecnologías. Para lograr este propósito, implementaré el proceso de desarrollo RUP y profundizaré en las arquitecturas de aplicaciones web.

# Objetivos
- Crear una aplicación web de películas y series.
- Ganar experiencia en el desarrollo de software.
- Mejorar mis habilidades con Git, GitHub, Angular, Java y Spring Boot y demás tecnologías.
- Aprender a utilizar el proceso de desarrollo RUP.
- Profundizar en las arquiteturas de aplicaciones web.

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
Es el flujo de trabajo (realización de casos de uso que incluye roles, actividades y artefactos) cuyo principal propósito es dirigir el desarrollo hacia el sistema correcto describiendo los requisitos del sistema de tal forma que se alcance el acuerdo entre el cliente, usuarios y desarrolladores sobre lo que el sistema debería hacer. (Master EscuelaIT)

## Actores y casos de uso
Los actores son los usuarios que interactúan con el sistema y los casos de uso son las acciones que pueden realizar los actores.

Para el caso de Flixxic, los actores serán administradores y usuarios. Los administradores son los que se encargan de gestionar el contenido, mientras que los usuarios son los que interactúan con el contenido.

### Casos de uso para los administradores

| Autenticación | Gestión del contenido |
| --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/admin/authentication.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/admin/content-management.svg?raw=true) |

### Casos de uso para los usuarios

Los usuarios podrán realizar las siguientes interacciones con el contenido:

| Autenticación | Gestión del perfil | Notificaciones |
| --------- | --------- |--------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/authentication.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/profile-management.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/notifications.svg?raw=true) |

| Ver detalles, buscar y filtrar | Comentar | Calificar |
| --------- | --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/view-search-filter.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/comments.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/reviews.svg?raw=true) |

| Favoritos | Ver más tarde | Historial |
| --------- | --------- | --------- |
| ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/favorites.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/watch-later.svg?raw=true) | ![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/content-interaction/history.svg?raw=true) |

#### Contexto de casos de uso

El siguiente diagrama de contexto de casos de uso representa el flujo de interacción entre los diferentes casos de uso del sistema.

Administradores

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/admin/use-cases-context-v2.svg?raw=true)

Usuarios 

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/1-actors-use-cases/user/use-cases-context-v2.svg?raw=true)

## Especificar casos de uso
Detalles de los casos de uso relacionados con la interacción que hace el usuario con el sistema y con la autenticación.

### Administradores

Autenticación

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/2-use-cases-specifications/admin/authentication.svg?raw=true)

Gestión del contenido

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/2-use-cases-specifications/admin/content-management.svg?raw=true)

### Usuarios

Autenticación

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/2-use-cases-specifications/user/authentication.svg?raw=true)

Interacción con el contenido

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/2-use-cases-specifications/user/content-interaction.svg?raw=true)


Gestión del perfil

![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/1-requeriments/2-use-cases-specifications/user/profile-management.svg?raw=true)

## Prototipar la interfaz de usuario
Los prototipos se encuentran realizados con figma y se pueden ver en los siguientes enlaces:
- Prototipo Desktop:  https://is.gd/zOKUJ5
- Prototipo Mobile: https://is.gd/SptDMP

## Disciplinas de análisis
### Analizar la arquitectura
La estructura de la aplicación será por modelos, vistas y controladores. 
![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/2-analysis/architecture-analysis.svg?raw=true)

## Disciplinas de diseño
### Diseñar la arquitectura 
![](https://github.com/vfred0/requirements-flixxic/blob/main/images/docs/3-design/architecture.svg?raw=true)

# Referencias
Para llevar a cabo este proyecto, he utilizado como referencia los siguientes proyectos y agradezco a los autores por compartirlos:

- [Gestor de taller mecánico AgrimManager](https://www.notion.so/Gestor-de-taller-mec-nico-AgrimManager-a8d44826c2494e15bcb235fc1019938d#cd3ccf181d9c4a1b9253416cd9b74f57)
- [HalteroCMS](https://github.com/zuldare/mastercloud_pfm_halterocms)
- [Master EscuelaIT](https://github.com/USantaTecla-0-general/3-publicaciones)