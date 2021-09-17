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

Crear y configurar pipelines en Azure DevOps web portal con el editor de la interfaz clásica de usuario. Se define un pipeline para build y test del código, y para luego publicar artifacts. Tambien se define un pipeline de release para consumir y deployear esps artifacts to *deployment targets*.


