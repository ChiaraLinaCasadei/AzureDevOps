# Pipelines
Azure Pipelines construye  (build) y testea proyectos para hacerlos accesibles a otros de forma automática.
Trabaja con casi cualquier lenguaje o tipo de proyecto.

Continuous integration (CI) automatiza tests and builds para tu proyecto. CI ayuda a detectar bugs or issues temprano en el ciclo de desarrollo, cuando son fáciles y rápidos de solucionar. Los Items conocidos como artifacts se producen desde sistemas CI. Los artifacts se usar por pipelines de delivery release continuo para lograr deployments automáticos.

Continuous delivery (CD) automáticamente realiza deploys y tests del código en múltiples etapas para ofrecer calidad. Los sistemas de integración continua producen artifacts deployables, que incluyen infrastructura y apps. Los pipelines de release automáticos consumen estos artifacts para lanzar nuevas versiones y fixes al objetivo a elección.

# Use Azure Pipelines because it supports the following scenarios:

* Works with any language or platform
* Deploys to different types of targets at the same time
* Integrates with Azure deployments
* Builds on Windows, Linux, or Mac machines
* Integrates with GitHub
* Works with open-source projects.

|Continuous integration (CI)|Continuous delivery (CD)|
|----|----|
|Increase code coverage|Automatically deploy code to production|
|Build faster by splitting test and build runs|Ensure deployment targets have latest code|
|Automatically ensure you don't ship broken code|Use tested code from CI process|
|Run tests continually||

# Define pipelines using the Classic interface

Crear y configurar pipelines en Azure DevOps web portal con el editor de la interfaz clásica de usuario. Se define un pipeline para build y test del código, y para luego publicar artifacts. Tambien se define un pipeline de release para consumir y deployear esos artifacts a *deployment targets*.

![alt text](https://docs.microsoft.com/en-us/azure/devops/pipelines/media/pipelines-image-designer.png?view=azure-devops)

# Funcionamiento del Pipeline

![alt text](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/media/key-concepts-overview.svg?view=azure-devops)
- A trigger tells a Pipeline to run.
- A pipeline is made up of one or more stages. A pipeline can deploy to one or more environments.
- A stage is a way of organizing jobs in a pipeline and each stage can have one or more jobs.
- Each job runs on one agent. A job can also be agentless.
- Each agent runs a job that contains one or more steps.
- A step can be a task or script and is the smallest building block of a pipeline.
- A task is a pre-packaged script that performs an action, such as invoking a REST API or publishing a build artifact.
- An artifact is a collection of files or packages published by a run.

## Azure Pipelines terms

### Agent
Cuando tu build o deployment corre, el sistema comienza uno o mas trabajos. Un agente está, una trabajo por vez, computando infraestructura con software ya instalado. Por ejemplo, tu trabajo podría estar corriéndolo un agente de Ubuntu, pero que está hosteado por Microsoft.

### Approvals
Approvals son un set de validaciones requeridas antes de que un define a deployment corra. Manual approval es un checkeo común realizado para controlar deployments en ambientes de producción. Cuando los checks son configurados en un ambiente, los pipelines se detendrán antes de comenzar una etapa que se lanza al ambiente, hasta que todos los checks se completen excitosamente.

### Artifact
Un artifact es una colección de archivos o paquetes publicados por una run. Los artifacts están disponibles para futuras tareas, como distribución o deployment.

### Deployment
Para Classic pipelines, es la acción de correr las tareas de una sola etapa, la cual puede incluir correr tests automatizados, deployear artifacts creados en build, y cualquier otra acción especificada para esa etapa.

### Deployment group
Es un set de máquinas con agentes instalados, que realizan deployments. Un deployment group es una agrupación de agentes, como una agent pool. Se pueden setear los deployment targets en un pipeline para un trabajo usando un deployment group.

### Environment
Es una colección de recursos, donde se lanza tu aplicación. Contiene una o más máquinas virtuales, containers, apps web o cualquier servicio utilizado para hostear la aplicación que se está desarrollando. Un pipeline puede lanzar la app a uno o mas environments luego de completar la build y correr todos los tests.

### Job
Una etapa contiene uno o más trabajos. Cada trabajo corre en un agente. Un trabajo representa reglas de ejecución para una serie de pasos. Todos los pasos los corre el mismo agente. Los trabajos son mas útiles cuando se quieren correr una serie de pasos en diferentes Environments. 

Por ejemplo, se pueden buildear dos configuraciones x86 y x64. En este caso, se tiene una etapa y dos trabajos, uno para cada configuración.

### Pipeline
Un pipeline define la integración continua y proceso de deployment para la app. Está compuesto por una o varias etapas. Se lo podría interpretar como un flujo de trabajo que define como correr los pasos de test, build y deployment.

### Release
Para Classic pipelines, un release es un set versionado de artifacts especificados en un pipeline. Una release es un snapshot de toda la información necesaria para llevar a cabo todas las tareas y acciones en el pipeline de release, como etapas, tareas...y políticas como triggers, approvers y opciones de deployment.
Un release puede crearse manualmente, con un deployment trigger, o con una API REST.

### Run
Representa una ejecución de un pipeline. Recopila los logs asociados con correr los pasos y los resultados de los test realizados. Durante una run, los Azure Pipelines procesan el pipeline y luego envían esta Run a uno o más agents. Cada agente correrá trabajos.

### Script
Un script corre código como paso en el pipeline utilizando command line, PowerShell, or Bash. Se puede escribir cross-platform scripts for macOS, Linux, and Windows. A diferencia de una tarea (task), un script es un código personalizado acorde al pipeline.

### Stage
Una stage es una regla lógica en el pipeline. Se puede usar para marcar la separación de asuntos (como Build, QA y producción). Cada stage contiene uno o más trabajos. Al definir múltiples stages en un pipeline, por default, corren una seguida de otra. Se puede especificar las condiciones en las que corre una stage. 

Cuando te pienses si es necesaria una stage, pregúntate:

* Hay grupos separados que manejen diferentes partes del pipeline? Por ejemplo, un test manager podría gestionar los Jobs de testing, y otro gestionar los relacionados a production deployment. En este caso, tiene sentido tener stages distintas para testing y production.
* Hay un set de approvals conectados para un Job o set de Jobs específicos?  Si es así, se pueden usar stages para subdividir los jobs en grupos lógicos que requieran approvals.
* Existen jobs que necesiten correr por un tiempo largo? Si se tiene parte de un pipeline con un tiempo de ejecución muy largo, tiene sentido dividirla en su propia Stage.

### Step
Un step es la unidad mas básica de un pipeline. Por ejemplo, un pipeline puede consistir de steps de testing y steps de build. Un step puede ser un script o task. Una task es un script pre-elaborado que te es ofrecido.

### Task
Una task es un cloque de construcción para definir la automatización en un pipeline. Es un script o procedimiento almacenado que se abstrajo con un set de entradas (inputs).

### Trigger
Es algo que se configura para indicar al pipeline cuando correr. Se puede configurar un pipeline para correr junto con un push a un repositorio, a un horario planificado, o luego de que se complete una build. Todas estas acciones son triggers.

### Library
Una Library incluye archivos seguros y grupos de variables. Los archivos seguros son una manera de almacenar archivos y compartirlos entre los pipelines. Se podría necesitar guardar un archivo a nivel DevOps y luego usarlo durante build o deployment. En ese caso, se puede guardar el archivo en Library y usarlo cuando sea necesario. Los grupos de variables almacenan valores y claves que puede ser necesario pasar a un pipeline o múltiples.


