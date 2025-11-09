stateDiagram-v2
    [*] --> Activo

    Activo --> Editando : administrador_modifica
    Editando --> Activo : cambios_guardados

    Activo --> EnPromocion : activar_promocion
    EnPromocion --> Activo : terminar_promocion

    Activo --> Deshabilitado : desactivar_producto
    Deshabilitado --> Activo : reactivar_producto
