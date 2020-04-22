@startuml Ejercicio1
left to right direction
skinparam packageStyle rectangle
actor Fabrica
actor Socios
actor Cliente
rectangle FabricaEmbutidos{
    (Productos) -- Socios : Establece precio
    Fabrica -- (Productos) : Aporta
    Fabrica -- (Socios) : FormadoPor
    Cliente -- (Plataforma) : Compra a traves de
    Socios -- (Plataforma) : Tienen
    Productos -- (Plataforma) : Vendidos en
    (Plataforma) <... (Tienda propia) : extends
    (Plataforma) <... (Tienda de fabrica) : extends
    (Plataforma) <... (App Web) : extends
    (App Web) <. (Precio Productos) : include
    (App Web) <. (Catálogo Productos) : include
}
@enduml