sequenceDiagram
    participant C as Cajero
    participant S as Sistema
    participant I as Inventario
    participant K as Cocinero

    C->>S: Capturar pedido (tipo de crepa, extras, precio)
    S->>S: Validar información
    C->>S: Confirmar pedido
    S->>S: Asignar número de pedido
    S->>I: Descontar ingredientes
    I-->>S: Confirmación de descuento
    S->>K: Enviar pedido a cocina
    K-->>S: Actualizar estado (en preparación)
    S-->>C: Mostrar número de pedido y estado
