@startuml

title Mario Bros - Diagrama de Casos de Uso

left to right direction

actor "Jugador" as Jugador
actor "Enemigo\n(IA)" as Enemigo
actor "Administrador" as Admin

rectangle "Mario Bros" {

    usecase "Iniciar juego" as UC1
    usecase "Mover personaje" as UC2
    usecase "Saltar" as UC3
    usecase "Recolectar monedas" as UC4
    usecase "Eliminar enemigo" as UC5
    usecase "Pausar / Reanudar" as UC6
    usecase "Salir del juego" as UC7
    usecase "Gestionar niveles" as UC8

    usecase "Mover a la izquierda" as UC9
    usecase "Mover a la derecha" as UC10

}

Jugador --> UC1
Jugador --> UC2
Jugador --> UC3
Jugador --> UC4
Jugador --> UC5
Jugador --> UC6
Jugador --> UC7

Enemigo --> UC5

Admin --> UC8

UC2 ..> UC9 : <<include>>
UC2 ..> UC10 : <<include>>

@enduml
