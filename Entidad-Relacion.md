erDiagram

    USUARIO {
        int id_usuario PK
        string nombre
        string usuario
        string contraseña
        string rol
    }

    ACTIVIDAD {
        int id_actividad PK
        string descripcion
        datetime fecha_hora
        int id_usuario FK
    }

    PRODUCTO {
        int id_producto PK
        string nombre
        string descripcion
        float precio
        boolean promocion
    }

    INGREDIENTE {
        int id_ingrediente PK
        string nombre
        int cantidad_disponible
        int cantidad_minima
    }

    PEDIDO {
        int id_pedido PK
        datetime fecha_hora
        float total
        string estado
        int id_usuario FK
    }

    PEDIDO_PRODUCTO {
        int id_pedido FK
        int id_producto FK
        int cantidad
    }

    PEDIDO_INGREDIENTE {
        int id_pedido FK
        int id_ingrediente FK
        int cantidad_usada
    }

    VENTA {
        int id_venta PK
        int id_pedido FK
        float total
        string forma_pago
        datetime fecha
    }

    USUARIO ||--o{ PEDIDO : "realiza"
    PEDIDO ||--o{ PEDIDO_PRODUCTO : "incluye"
    PRODUCTO ||--o{ PEDIDO_PRODUCTO : "pertenece"
    PEDIDO ||--o{ PEDIDO_INGREDIENTE : "usa"
    INGREDIENTE ||--o{ PEDIDO_INGREDIENTE : "descontado"
    PEDIDO ||--|{ VENTA : "genera"
    USUARIO ||--o{ ACTIVIDAD : "registra"
