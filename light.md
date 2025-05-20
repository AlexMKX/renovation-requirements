# Пример управления светом с модулем размещенным в помещении.
1. Выключатель коммутирует DI вход модуля (низковольтный логический вход)
2. Модуль соответственно коммутирует лампы подключенные к R1-R4.

Допускается использование фиксирующихся выключателей, а не только кнопок.

```mermaid
graph LR
    Выключатель --> |DI0| ESC3B04 --> |R1| Лампа1
    ESC3B04 --> |R2| Лампа2
    ESC3B04 --> |R3| Лампа3
    ESC3B04 --> |R4| Лампа4

    subgraph ESC3B04
        direction LR
        DI0[DI0] --- DI1[DI1] --- DI2[DI2] --- DI3[DI3] --- DI4[DI4]
        R1[R1] --- R2[R2] --- R3[R3] --- R4[R4]
    end

    style ESC3B04 fill:#f9f,stroke:#333,stroke-width:2px
    style Выключатель fill:#bbf,stroke:#333,stroke-width:2px
    style Лампа1 fill:#bfb,stroke:#333,stroke-width:2px
    style Лампа2 fill:#bfb,stroke:#333,stroke-width:2px
    style Лампа3 fill:#bfb,stroke:#333,stroke-width:2px
    style Лампа4 fill:#bfb,stroke:#333,stroke-width:2px
