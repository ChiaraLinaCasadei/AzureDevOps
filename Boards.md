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

Epic

An Epic is a large user story that is so big that it is impossible to estimate its effort or even a user story that is too large to fit into a single sprint. Usually, it represents a business initiative to be accomplished.
Ex: Increase customer engagement, Improve and simplify the user experience, Implement new architecture to improve performance, Engineer the application to support future growth, Support integration with external services, Support mobile apps.

Feature

A feature represents a shippable software component and reflects a service that fulfills some critical stakeholder needs.
Ex: Add view options to the new work hub, Add mobile shopping cart, Support text alerts, Refresh the web portal with a new look and feel.

User Story, Product backlog item or Requirement

A user story is an informal, short requirement (usually three sentences) written from an end user’s perspective by the stakeholders (managers, end-users, project sponsors, etc.). The purpose of the user story is to articulate how a workpiece will deliver a particular value to the software.
Usually, user stories look like:
As a <role>, I can <goal or need>, so that <why>
Ex: I want to invite my friends so that we can enjoy this service together.I want to organize my work so that I can feel more in control. I want to understand my colleagues’ progress, so I can better report our successes and failures.
  
Task
  
A task is a smaller item to track activity and contains all the information needed to accomplish part of an issue, user story, requirement.
During the sprint planning meeting, the team breaks down each user story into manageable tasks and estimates tasks in hours to plan the sprint and decide how many user stories it can take on.

Bug
  
When a bug is founded during the test phase, it is tracked by a bug work item that describes its repro steps, which should provide what you need to reproduce the bug and its behavior. 

Impediment or Issue
  
Issues (Agile) and impediments (Scrum) are unplanned activities that may block work from getting done.
During the daily standup meeting, the team members report if they have encountered any impediments. If so, they are tracked and managed until their resolution and closure.
Since their resolution may require additional work beyond what is tracked for actual requirements, they can be split into tasks.
  
Change request
  
This work item is specific for the CMMI process template and refers to a change request work item used to track all changes that deviate from the original requirement’s baseline.
For example, if a user’s meeting uncovers new requirements, a change request should be created to propose updating the requirements baseline.
  
Review
  
The review work item is used to track formal meetings or reviews from other parts. It can be a review for quality purposes or to recap something.
  
Risk
  
The risk work item is used to describe an event in which outcome varies from the desired result. This work item provides fields to define the probability of occurrence, mitigate the impact, and contingency plans for recovery in the event of an occurrence.
  
  

Distintos Work Items para cada Setup de Boards

* Epic (Basic, Agile, Scrum, and CMMI)
* Feature (Agile, Scrum, and CMMI)
* User Story (Agile), Product backlog item (Scrum), Requirement (CMMI)
* Task (Basic, Agile, Scrum, and CMMI)
* Impediment (Scrum), Issue (Agile and Basic)
* Bug (Agile, Scrum, and CMMI)

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

El sprint me permite ver todas las US de esa iteracion y ordenarlas por prioridades.
Un lapso de tiempo de 2 a 3 semanas. Durante ese lapso deben resolverse los diferentes WorkItems planificados. Es una buena forma de estimar la capacidad de trabajo de cada integrante del equipo.

En Azure es una combinaciones de Boards y BackLogs. Es como el tablero de Boards, tiene los WItems que se pueden arrastrar y soltar (TaskBoards), pero no muestra todos, sino específicamente los de ese Sprint, tambien llamado Iteración. 





