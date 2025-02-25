```mermaid
flowchart TD
    classDef inicio fill:#FF9900,stroke:#FF6600,stroke-width:2px,color:white,font-weight:bold
    classDef decision fill:#6C8EBF,stroke:#7A7AC5,stroke-width:2px,color:white,font-weight:bold
    classDef outbound fill:#D4E8D4,stroke:#82B366,stroke-width:2px,color:#333,font-weight:bold
    classDef inbound fill:#FFE6CC,stroke:#D79B00,stroke-width:2px,color:#333,font-weight:bold
    classDef funnel fill:#DAE8FC,stroke:#6C8EBF,stroke-width:2px,color:#333,font-weight:bold
    classDef cierre fill:#F8CECC,stroke:#B85450,stroke-width:2px,color:#333,font-weight:bold
    classDef exito fill:#006633,stroke:#00CC66,stroke-width:3px,color:white,font-weight:bold
    
    A["SISTEMA DE ADQUISICIÓN DE CLIENTES"]:::inicio --> B{"¿OUTBOUND DOMINADO?"}:::decision
    B -->|NO| C["FASE OUTBOUND (Obligatoria)"]:::outbound
    B -->|SÍ| D["FASE INBOUND (Automatización)"]:::inbound
    
    C --> C1["Email en frío"]:::outbound
    C --> C2["LinkedIn en frío"]:::outbound
    C --> C3["Llamadas en frío"]:::outbound
    C --> C4["Loom/videos personalizados"]:::outbound
    
    C1 & C2 & C3 & C4 --> C5["Recolección de datos"]:::outbound
    C5 --> C6["Observación del proceso completo"]:::outbound
    C6 --> C7["Creación de sistema replicable"]:::outbound
    C7 --> B
    
    D --> D1["Email Software Automatizado"]:::inbound
    D --> D2["Setter/Delegación"]:::inbound
    D --> D3["Marca Personal"]:::inbound
    D --> D4["Anuncios Pagados"]:::inbound
    
    D1 & D2 & D3 & D4 --> E["FUNNEL DE CONVERSIÓN"]:::funnel
    
    E --> E1["VSL"]:::funnel
    E --> E2["Webinar"]:::funnel
    E --> E3["Free Training"]:::funnel
    E --> E4["Case Story"]:::funnel
    E --> E5["Demo Funnel"]:::funnel
    
    E1 & E2 & E3 & E4 & E5 --> F["PROCESO DE CIERRE"]:::cierre
    
    F --> F1["Demo Call (15 min)"]:::cierre
    F1 --> F2["Llamada 1 - Presentación"]:::cierre
    F2 --> F3{"¿Único decisor?"}:::decision
    F3 -->|SÍ| F4["CIERRE VENTA"]:::cierre
    F3 -->|NO| F5["Llamada 2 - Todos los decisores"]:::cierre
    F5 --> F4
    
    F4 --> G["NUEVO CLIENTE CONSEGUIDO"]:::exito