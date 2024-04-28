## ¡Hola!
Aca vamos a tratar de reunir toda la informacion acerca de la materia de Ingenieria de Software, incluida en el programa de la carrera de Ingenieria en Computacion dictada en la Universidad Nacional de Rio Negro.
## ¿De que trata esta materia?
Esta materia comprende la totalidad del desarrollo de un software, yendo desde la documentacion y practicas sociales, hasta la aplicacion del mismo.
## ¿Que podemos encontrar en esta organizacion?
Aca vas a encontrar gente comprometida, que busca en cada trabajo sacar lo mejor de si. En los repositorios vas a ver contenido relacionado al proyecto que se este llevando a cabo en la catedra del presente año.
### DFD (Diagrama de flujo de datos)

```mermaid
%%{init: {"flowchart": {"defaultRenderer": "elk"}} }%%

graph LR;

A((Determinar </br> ubicacion </br> del evento))
B((Determinar </br> ubicacion </br> de la materia))
C((Suministrar y/o </br> actualizar datos))
D((Asignar prioridad </br> de eventos))
E((Asignar prioridad </br> de materias))
F((Solucionar </br> colisiones </br> horario-evento))
G((Solucionar </br> colisiones </br> materia-materia))

Vista[Vista Publica]

Directores --> D
Directores --> E

Alumnos --> Vista
Profesores --> Vista
ND[No docentes] --> Vista

style Directores fill: lightblue
style Alumnos fill: lightblue
style Profesores fill: lightblue
style ND fill: lightblue

D --> TablaDeEventos
E --> TablaDeMaterias

style TablaDeEventos fill:lightgreen
style TablaDeAulas fill:lightgreen
style TablaDeProfesores fill:lightgreen
style TablaDeMaterias fill:lightgreen

style Vista fill: yellow

TablaDeEventos --> A
TablaDeAulas --> A
TablaDeMaterias --> B --> Directores --> C
TablaDeAulas --> B
B --> G --> Vista
A --> F --> Vista
Directores --> Vista

C -.-> TablaDeEventos
C -.-> TablaDeProfesores
C -.-> TablaDeAulas
C -.-> TablaDeMaterias
```
