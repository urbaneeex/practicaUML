@startuml Ejer2
skinparam packageStyle rectangle
left to right direction 
actor profesor
actor  alumno
rectangle  Moodle {
   alumno -- (Curso): accede usuario
   (Curso) <... (Contenido): extends
   (Curso) <... (Examenes): extends
   (Curso) <... (Actividades): extends
   (Contenido) <... (Nota media curso): include
   (Actividades) <... (Nota media curso): include
   (Examenes) <... (Nota media curso): include
   profesor -- (Materia): administra 
   (Materia) <. (Curso):include
   (Materia) <... (Administra Examenes): extends
   (Materia) <... (Administra Contenido): extends
   (Materia) <... (Administra Actividades): extends
   (Materia) <... (Administra Participantes): extends
   (Administra Participantes) <.. (Eliminar integrantes): extends
   (Administra Participantes) <.. (Añadir integrantes): extends
   (Administra Participantes) <.. (Modificar integrantes): extends
   (Administra Examenes) <. (Califica notas): include
   (Curso) <. (Chat con profesor) : include
   (Curso) <. (Calendario escolar) : include

}
@enduml