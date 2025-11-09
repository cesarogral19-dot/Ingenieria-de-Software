stateDiagram-v2
    [*] --> Capturando
    Capturando --> Corrigiendo : cajero_edita_pedido
    Corrigiendo --> Capturando : corrección_terminada
    Capturando --> Confirmado : confirmar_pedido

    Confirmado --> EnPreparación : enviado_a_cocina
    EnPreparación --> Listo : cocinero_marca_listo
    Listo --> Entregado : entregar_pedido

    Entregado --> [*]
