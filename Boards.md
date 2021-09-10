# ¿Qué es?
Azure DevOps es la propuesta de Microsoft, la cual provee muchas herramientas para mejorar el producto o software.
Se divide en Organizaciones y Proyectos.
Dentro de estas herramientas, podemos encontrar:

## Boards
Son herramientas ágiles para que lo que sea que desarrollemos en el ámbito Azure DevOps pueda planificarse, visualizarse y discutirse a nivel equipo.
Hay diferentes "setups" para Boards, los principales son 4:
1) Basic: Flujo de trabajo flexible y simple.
2) Agile: Flujo de trabajo Ágil con elementos más detallados. Ya arrancan a aparecer Epics, Feature, User Story...
3) Scrum: Flujo de trabajo regido por este Framework.
4) CMMI: Proyectos más formales donde la toma de decisiones debe ser auditable. Incluye Reviews y eso.

Cada setup de board tiene diferentes "work items".

La sección Boards de AzureDevOps posee diferentes herramientas:

### Work Item
El work item es un tag que me indica qué es o qué hace un determinado requerimiento del sistema.
Los tipos de work items se basan en el proceso utilizado cuando se creó el proyecto (cualquiera de los 4 de arriba).

En cada work item podemos agregar información, archivos adjuntos, y otros elementos que ayuden a guiarnos para realizarlo como se debe.
Por lo general, los que definen estos work items son el Scrum Master y el Product Owner.

---

Tipos de Work Items y cuando usarlos

* Features -> para funcionalidades que el cliente desea implementar. Deben completarse en uno o más sprints.
* User Story -> para requerimientos, luego agregarles más detalles. Deben completarse en un sprint.
* Bugs -> para capturar defectos de código.
* Epics -> se entregará trimestralmente para un objetivo importante.
* Task ->
* Test Case ->

Epic > Feature > User Story

Las User Stories se asignan a las Features para un seguimiento del progreso en la gestión del proyecto.

---

Es un buscador de elementos de trabajo, pero su objetivo es filtrar los WorkItems relacionados a nosotros, o nuestra sección de trabajo.

Cada WorkItem puede ser marcado para seguir su actividad y cambios, para eso es el filtro Following.

Cuando nosotros modificamos uno recientemente (cambio de status, comentario agregado), aparecen bajo el filtro My Activity.

Para manipular el resultado de la busqueda, está la sección "My Queries", aunque lo que está por defecto es muy útil para empezar. 


### Boards

Es una lista general de WorkItems organizado por prioridades. Contiene todos los del proyecto.

### BackLogs

Tiene todos los WorkItems, pero agrupados por iteraciones.
Siempre usar BackLogs para cambiar un WorkItem de una iteraciones a otra, porque así tambien se mueven sus tareas asociadas (hijos), cosa que puede no suceder si lo hacemos manualmente, y nos traerá problemas.

### Sprint

Un lapso de tiempo de 2 a 3 semanas. Durante ese lapso deben resolverse los diferentes WorkItems planificados. Es una buena forma de estimar la capacidad de trabajo de cada integrante del equipo.

En Azure es una combinaciones de Boards y BackLogs. Es como el tablero de Boards, tiene los WItems que se pueden arrastrar y soltar (TaskBoards), pero no muestra todos, sino específicamente los de ese Sprint, tambien llamado Iteración. 





