Producto 1 - Red Empresarial (Equipo 4)

Materia: Conmutación y Enrutamiento (TI-203), ITLA
Plataforma: PNETLab

Descripción

Red empresarial segmentada por departamentos mediante VLANs, con alta disponibilidad de gateway (HSRP), redundancia de enlace (EtherChannel y STP) y enrutamiento dinámico con OSPFv2 (área única, con posibilidad de extender a multiárea).

Direccionamiento asignado

IPv4: 172.22.0.0/15
IPv6: 2001:25:22::/48

Plan IPv4 (VLSM)

R1-Core


Estudiantes (1500 hosts): 172.22.0.0/21
Docentes (164 hosts): 172.22.8.0/24
Gestión (29 hosts): 172.22.10.0/27
Voz (16 hosts): 172.22.10.32/28
Blackhull (10 hosts): 172.22.10.48/28


R2


Académicos (80 hosts): 172.22.9.0/25
Finanzas (64 hosts): 172.22.9.128/26
Datacenter (44 hosts): 172.22.9.192/26
Blackhull (10 hosts): 172.22.10.64/28
Enlace P2P R1-R2 (2 hosts): 172.22.10.80/30


Plan IPv6

Prefijos /64 asignados desde 2001:25:22::/48, ordenados de mayor a menor tamaño de red:


Estudiantes: 2001:25:22:1::/64
Docentes: 2001:25:22:2::/64
Académicos: 2001:25:22:3::/64
Finanzas: 2001:25:22:4::/64
Datacenter: 2001:25:22:5::/64
Gestión: 2001:25:22:6::/64
Voz: 2001:25:22:7::/64
Blackhull R1: 2001:25:22:8::/64
Blackhull R2: 2001:25:22:9::/64
Enlace P2P R1-R2: 2001:25:22:a::/64


Tecnologías implementadas


VLANs y VTP para segmentación y propagación entre switches
EtherChannel y STP para redundancia en capa 2
HSRP para alta disponibilidad de gateway
OSPFv2 para enrutamiento dinámico entre routers




