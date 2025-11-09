graph TD

    %% ENTIDADES
    U[Usuario]
    P[Pedido]
    PR[Producto]
    ING[Ingrediente]
    V[Venta]
    A[Actividad]

    %% RELACIONES
    U ---|1,N| P
    P ---|N,N| PR
    P ---|N,N| ING
    P ---|1,1| V
    U ---|1,N| A

    %% Etiquetas de relaciones
    R1[(realiza)]
    R2[(incluye)]
    R3[(usa)]
    R4[(genera)]
    R5[(registra)]

    %% Conexiones con relaciones
    U --- R1 --- P
    P --- R2 --- PR
    P --- R3 --- ING
    P --- R4 --- V
    U --- R5 --- A
