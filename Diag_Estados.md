stateDiagram-v2
    [*] --> Disponible

    Disponible --> Bajo : cantidad < mínimo
    Bajo --> Agotado : cantidad = 0
    Agotado --> Reabasteciendo : administrador_agrega_existencias
    Reabasteciendo --> Disponible : inventario_actualizado

    Disponible --> Descontando : pedido_confirmado
    Descontando --> Disponible : descuento_completado

    Bajo --> Reabasteciendo : agregar_ingredientes
