# Unidad 0


## Objetivos
* Describir el ciclo de vida del desarrollo de software.
* Definir DevOps
* Identificar las prácticas de DevOps que aceleran el ciclo de vida de desarrollo de software
* Identificar patrones comunes de arquitectura de software.
* Identificar procesos de despliegue en los patronces de arquitectura de software.


## Introducción

## Ciclo de vida del software

El Ciclo de vida de desarrollo de sistemas comprende procesos, análisis y actividades del desarrollo de una solución de software desde la concepción de la idea, hasta la puesta en producción donde los usuarios acceden finalmente al software. Adicionalmente este software se contempla que deberá ser mantenido en el tiempo con actualizaciones, mejoras, etc.

![Ciclo de vida](https://www.viewnext.com//wp-content/uploads/2018/06/7fases_SDLC_infografia.jpg)

Este gráfico aunque representativo de los procesos da la impresión de ser finito, es decir, que en algun momento el software deja de ser atendido.

Esta es la realidad para muchas soluciones de software, pero si la plataforma es lo suficientemente flexible, nada impide que pudiera seguir por decadas en el mismo proceso.

Como referencia, hay software en los mercados de valores, la banca e incluso la industria aeronautica que tiene mas de 40 años, y aun se mantiene, aunque imagino que no tan regularmente como antes.

## Que es DevOps?

*DevOps es un conjunto de prácticas y estrategias del proceso de construcción de software donde convergen las actividades de desarrollo (development) y operaciones (operations)*. El desarrollo como tal (hacer código en un determinado lenguaje) y los procesos de operaciones son desplegar el software en una infraestructura para usarlo, probarlo, mejorarlo, etc.

La propuesta de DevOps está ligada a los procesos, es decir a las diferentes actividades que debe realizar una organización desde que se genera código fuente, hasta que este código fuente llega a los usuarios finales (internos o externos).

![Ciclo en DevOps y herramientas](https://i1.wp.com/geniusitt.com/wp-content/uploads/2018/08/DevOpstools-1.png)

Otras metodologías más formales de apoyo, complemento, soporte son: Agile, Lean, Kanban, etc. El objetivo principal en de todas ellas es finalmente hacer las cosas de manera eficiente, eficaz y sumado a esto: con el menor error humano (por medio de la automatización).

Una de las herramientas principales en las prácticas de DevOps es formalizar todo lo que se puede: código fuente, estado de las máquinas, configuraciones, librerías, etc. en un repositorio de código.

Algunas aplicaciones desarrolladas para ambiente de nube (Cloud Native Apps) llevan incluso este proceso a considerar que cada proyecto debe tener su repositorio propio y único donde se centraliza toda la información del mismo. La organización entonces tiene varios repositorios de código fuente desde donde se obtiene, compila(si es pertinente), configura el ambiente y despliega para su uso.

Esto lo ahondaremos en la [Unidad 1](../01/)

## Arquitectura de software

> En el comienzo el arquitecto creo el software, y todo estaba en un solo lugar, y vio que esto era bueno

Se dice que un sistema o solución de software monolítico es aquel donde la capa de interfaz de usuario, la logica de negocios e incluso la capa de acceso a los datos están combinadas en un mismo programa.[1](https://es.wikipedia.org/wiki/Aplicaci%C3%B3n_monol%C3%ADtica "Wikipedia")

Dado que los sistemas monolíticos son muy dificiles de mantener, la tendencia es desarrollar algo modular.

La tendencia actual en el procesos de desarrollo es descomponer el problema mas grande (sistema) en problemas mas pequeños (pequeños módulos). Eso indica que el mantenimiento se realiza de manera modular también sin afectar al sistema como un todo. 

Los microservicios son las expresión de esta tendencia. Es software que realiza una tarea muy particular, granular y contenida, normalmente son API. La interfaz de usuario consumen estos microservicios.

Como cada microservicio es una software autónomo, las actualizaciones o mantinimiento del mismo no afecta el funcionamiento de los demás componentes del sistema.

![Microservicios](https://miro.medium.com/max/724/1*1y2jFl5j58kDBpV5bzqCbQ.png)

*Tanto el software monolítico como el modular pueden ser desarrollados usando las prácticas de DevOps* 

## Patrones de despliegue

Cuando el software está listo para ser desplegado, un ambiente "de producción" se prepara. En ese ambiente se instalan todos los componentes que requiere el software para funcionar. El equipo de operaciones es el encargado de preparar ese ambiente.

Ese ambiente, cuando está listo, y en uso, rara vez se toca. Citando el famoso adagio del administrador de sistemas:

> Si funciona, no lo toques.

Realmente si se realizan cambios a este ambiente o al menos en teoría debería ser asi: actualizaciones de sistema operativo, librerías, motor de bases de datos, etc.

Este concepto lo diferencio de los cambios del software propiamente dicho. Sino de la plataforma subyacente en la que se ejecuta el software
 
Es una buena práctica, aunque no tan común, manejar un ambiente de pre-producción (**Staging**), que es un ambiente idéntico al de producción y se utiliza para desplegar cambios en el software como tal.

Esta buena practica se le dice despliegue azul-verde (**blue-green deployment**)

![Blue Green Deployment](https://cdn2.hubspot.net/hubfs/5416872/thumbnail.jpg)

Estos ambientes, producción y staging, se intercambian regularmente.

### Las 3 capas

Una aplicación de microservicio normalmente (no siempre) estaría compuesto de 3 (tres) capas:

- Presentación
- Aplicación
- Base de datos

Es muy común que las organizaciones usen el mismo motor de bases de datos, aunque usen "sets de datos"(tablas,columnas) particulares de los datos para cada microservicio.

### Las bases de datos tienen un tratamiento particular

Realizar cambios a la base de datos es un tema muy particular que sale del alcance de este curso, requiere de un curso aparte.

Hay herramientas que permiten la migración del esquema, los cambios e incluso volver atrás a los cambios (roll-back) sin afectar los conjuntos de datos e información ya presente.

## Referencias

### Enlaces

* [Ciclo de vida de sistemas](https://www.viewnext.com/el-ciclo-sdlc-en-7-fases)
* [Resumen de que es y para que sirve DevOps](https://www.programaenlinea.net/que-es-y-para-que-sirve-devops)
