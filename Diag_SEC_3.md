sequenceDiagram
    participant C as Cajero
    participant S as Sistema
    participant V as RegistroVentas

    C->>S: Registrar pago (efectivo/tarjeta)
    S->>S: Calcular total
    S->>V: Guardar venta
    V-->>S: Confirmación
    S-->>C: Mostrar ticket final
