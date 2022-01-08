# Unidad 1

## Objetivos
* Definir DevOps
* Indentificar las ventajas de las prácticas de DevOps
* Crear un repositorio en un sitio de hospedaje de código.
* Agregar un colaborador a un repositorio de código.
* Agregar, editar, eliminar cambios de manera colaborativa en un repositorio de código fuente.

## Introducción

> Ningún desarrollador o programador es tan bueno como su equipo. Sólos somos buenos, juntos somos mejores.

Los proyectos de desarrollo de software por lo general utilizan un Software de control de versiones (VCS, version control system)

En nuestro curso, estaremos usando **Git**, que es un software distribuído de control de versiones, que es uno de las más completos y más usados en la industria.

Uno de los portales más usados para hospedar gratuitamente código fuente (y otras informaciones) es [GitHub](https://github.com), existen además otros como [GitLab](https://gitlab.com), [BitBucket](https://bitbucket.com), entre otros.

Para el propósito de esta clase usaremos [GitHub](https://github.com), pero siéntase libre de usar el que le parezca más amigable, el código fuente estará disponible de manera abierta, y las herramienatas (en general) son estándares de la industria.

Uno de los fundamentos del uso de sistemas distribuidos y estándares de la industria es que cada uno puede gestionarlo desde donde le sea más cómodo.

## Que es DevOps?

DevOps es un conjunto de prácticas del proceso de construcción de software donde convergen el proceso de desarrollo como tal (hacer código en un determinado lenguaje) y el desplegar el software en una infraestructura para usarlo, probarlo, mejorarlo, etc.

La propuesta de DevOps está ligada a los procesos, es decir a las diferentes actividades que debe realizar una organización desde que se genera código fuente, hasta que este código fuente llega a los usuarios finales (internos o externos).

Otras metodologías más formales de apoyo, complemento, soporte son: Agile, Lean, Kanban, etc. El objetivo principal en de todas ellas es finalmente hacer las cosas de manera eficiente, eficaz y con el menor error humano (por medio de la automatización).

Una de las herramientas principales en las prácticas de DevOps es formalizar todo lo que se puede: código fuente, estado de las máquinas, configuraciones, librerías, etc. en un repositorio de código.

Algunas aplicaciones desarrolladas para ambiente de nube (Cloud Native Apps) llevan incluso este proceso a considerar que cada proyecto debe tener su repositorio propio y único donde se centraliza toda la información del mismo. La organización entonces tiene varios repositorios de código fuente desde donde se obtiene, compila(si es pertinente), configura el ambiente y despliega para su uso.

## Git

Git, siendo un sistema de versionamiento distribuido, puede tener varias copias de la misma información en diferentes lugares. Cada uno de estos espacios donde se almacena infomación se llama **repositorio**. Desde el punto de vista del usuario, es sumamente importante considerar el contexto en el que se encuentra en un repositorio antes de hacer cambios.

Por su parte, Git también propone varias herramientas que vamos a usar a lo largo de este curso para gestionar correctamente el código fuente sin que esto signifique tanto problema al largo plazo.

### Contexto

Algunas palabras claves que debemos considerar para indetificar el contexto: repositorio (repo, **repository**), rama (**branch**). Notará que algunas de ellas estan en castellano con su traducción al inglés, normalmente los gestores de repositorio utilizan las expresiones en inglés incluso si la interfaz gráfica pudiera estar en otro idioma. Esto es relevante porque los comandos se respaldan en estas mismas palabras clave.

### Colaboración

En el proceso de colaboración, algunas palabras claves a tomar en cuenta: pedido de integración (**pull request**), descargar (**fetch**, enviar (**pull**).

### Gestión de contenido

En la gestión de contenido, específicamente el código fuente, se consideran algunas términos como: add (**agregar**), guardar (**stash**), **commit**.

Una buena practica, y de suma importancia es la nomenclatura clara y consistente en los nombres de todo lo anterior y de los mensajes en cada unos de los **commits** que se realicen en el repositorio.

## Ejericio 1

Realizar el [Ejericicio 1](Unidad01-Ejercicio01.md), necesitará realizar el trabajo con un compañero del curso.

## Flujo de trabajo (workflow)

Cada organización, grupo de trabjo y persona, tiene su flujo de trabajo, es decir la forma (procesos) de hacer las cosas (obtener resultados). Uno de los problemas recurrentes en los equipos de trabajos es que se enfocan en los procesos y no en las personas, y es importante saber que uno no existe sin el otro.

Los equipos que se formen en este curso, y el método de colaboración no es una excepción. El curso en sí proveerá de los objetivos a alcanzar y algunas herramientas para optimizar el flujo de trabajo, pero cada equipo finalmente encontrará su forma de trabajo colaborativo, su proceso, su "workflow".

[Este interesante artículo](https://buddy.works/blog/5-types-of-git-workflows) nos dará algo de lúz a las formas básicas y no tan básicas de los flujos de trabajo con código fuente. Uno de los más utilizados, considerado el más amigable es el explicado por Vincent Driessen en su artículo [A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/). De ninguna manera es un "estándar" pero es el que he visto más usado en proyectos colaborativos de gran envergadura.

## Referencias

### Presentaciones

* [Rodolfo Arce - Presentación sobre Git](https://rodolfoarce.com/wp-content/uploads/2013/10/GIT-Universidad-Americana-Oct-2013.pdf)

### Anotaciones

* [Anotaciones de comandos](Anotaciones.md)

## Otros

* [Curso Cloud Native Foundamentals](https://www.udacity.com/course/cloud-native-fundamentals--ud064)
