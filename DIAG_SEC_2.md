sequenceDiagram
    participant S as Sistema
    participant I as Inventario
    participant A as Administrador

    S->>I: Solicitar cantidades actuales
    I-->>S: Retornar cantidades
    S->>I: Descontar ingredientes usados
    I-->>S: Confirmar nuevo inventario
    I->>A: Enviar alerta de ingrediente bajo

