### 🗺️ Arquitetura do Ambiente
O diagrama abaixo representa o fluxo de rede e a segmentação lógica das instâncias dentro do Proxmox:

```mermaid
graph TD
    %% Estilo
    classDef hardware fill:#f96,stroke:#333,stroke-width:2px;
    classDef network fill:#69f,stroke:#333,stroke-width:2px;
    classDef service fill:#dfd,stroke:#333,stroke-width:1px;

    Internet((Internet)) --- FW[pfSense / Firewall]

    subgraph Host_Fisico [Dell PowerEdge 2950]
        direction TB
        PVE[Proxmox VE]
        RAID1[(RAID 1 - 1TB)] --- PVE
    end

    FW --> VLAN10[VLAN 10: Gerenciamento]
    FW --> VLAN20[VLAN 20: DMZ / Web]
    FW --> VLAN30[VLAN 30: Lab Zone]

    PVE -.-> VLAN10
    PVE -.-> VLAN20
    PVE -.-> VLAN30

    VLAN10 --> ZBX[Zabbix Server]
    VLAN20 --> NPM[Nginx Proxy Manager]
    VLAN30 --> DKR[Docker Host / Containers]

    class Host_Fisico hardware;
    class FW,VLAN10,VLAN20,VLAN30 network;
    class ZBX,NPM,DKR service;
