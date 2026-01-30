# 🖥️ Homelab Physical – Proxmox Infrastructure

![PROVIDER](https://img.shields.io/badge/PROVIDER-HOME_LAB-orange?style=flat-square)
![OS](https://img.shields.io/badge/OS-PROXMOX_VE-E57024?style=flat-square&logo=proxmox&logoColor=white)
![TYPE](https://img.shields.io/badge/TYPE-BARE_METAL-blue?style=flat-square)
![STATUS](https://img.shields.io/badge/STATUS-ONLINE-brightgreen?style=flat-square)

> **Resumo:** Homelab físico de alta performance provisionado em hardware Dell Enterprise, com foco em virtualização avançada, segmentação de redes e simulação de ambientes produtivos on-premises utilizando Proxmox VE.

---

### ⚙️ Especificações de Hardware
| Componente | Detalhes Técnicos |
| :--- | :--- |
| **Servidor** | Dell PowerEdge 2950 |
| **Processador** | Intel® Xeon® Processors |
| **Memória** | 8 GB RAM DDR2 ECC |
| **Storage** | 1 TB RAID 1 (SATA/SAS) |
| **Controladora** | PERC 6/i Integrated |

---

### 🧩 Stack de Tecnologias
* **Virtualização:** Proxmox VE (KVM/LXC)
* **Sistemas Base:** Ubuntu Server
* **Containers:** Docker Compose
* **Monitoramento:** Zabbix
* **Redes:** pfSense
* **Automação:** Shell Script & rsync

---

### 🗺️ Arquitetura & Segmentação
O ambiente é dividido em camadas para simular uma infraestrutura real:
* **DMZ:** Serviços expostos (Web/Proxy).
* **Management:** Acesso restrito ao hipervisor e ferramentas de monitoramento.
* **Lab Zone:** Área de testes e deploy de novas VMs/Containers.

---

### 🔐 Segurança & Backup
* **Firewalling:** Regras granulares por VLAN.
* **Acesso:** Autenticação via Chaves SSH (Hardening).
* **Resiliência:** Espelhamento de disco via RAID 1 por hardware.
* **Backup:** Rotinas automatizadas enviando dados críticos para storage externo.

---

### 🚀 Roadmap de Evolução
- [ ] Implementação de provisionamento via **Ansible**.
- [ ] Configuração de **High Availability** (Cluster Proxmox).
- [ ] Integração de CI/CD para infraestrutura como código (IaC).
- [ ] Migração de backups para Cloud Object Storage.

---
*Documentação mantida como parte do processo de aprendizado contínuo em SysAdmin e DevOps.*
