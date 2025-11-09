sequenceDiagram
    participant A as Admin
    participant S as Sistema
    participant BD as BaseDatos

    A->>S: Agregar/editar producto
    S->>S: Validar datos (precios, ingredientes)
    S->>BD: Actualizar menú
    BD-->>S: Confirmación
    S-->>A: Cambios aplicados
