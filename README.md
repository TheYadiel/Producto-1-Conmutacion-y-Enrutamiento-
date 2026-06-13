# Producto 1 - Red Empresarial (Equipo 4)

Materia: Conmutación y Enrutamiento (TI-203), ITLA
Plataforma: PNETLab

## Descripción

Red empresarial segmentada por departamentos mediante VLANs, con alta disponibilidad de gateway (HSRP), redundancia de enlace (EtherChannel y STP) y enrutamiento dinámico con OSPFv2 (área única, con posibilidad de extender a multiárea).

## Direccionamiento asignado

IPv4: 172.22.0.0/15
IPv6: 2001:25:22::/48

## Plan IPv4 (VLSM)

**R1-Core**
- Estudiantes (1500 hosts / 2046 usables): 172.22.0.0/21, gateway 172.22.0.1, broadcast 172.22.7.255
- Docentes (164 hosts / 254 usables): 172.22.8.0/24, gateway 172.22.8.1, broadcast 172.22.8.255
- Gestión (29 hosts / 30 usables): 172.22.9.0/27, gateway 172.22.9.1, broadcast 172.22.9.31
- Voz (16 hosts / 30 usables): 172.22.9.32/27, gateway 172.22.9.33, broadcast 172.22.9.63
- Blackhull (10 hosts / 14 usables): 172.22.9.64/28, gateway 172.22.9.65, broadcast 172.22.9.79

**R2**
- Académicos (80 hosts / 126 usables): 172.22.10.0/25, gateway 172.22.10.1, broadcast 172.22.10.127
- Finanzas (64 hosts / 126 usables): 172.22.10.128/25, gateway 172.22.10.129, broadcast 172.22.10.255
- Datacenter (44 hosts / 62 usables): 172.22.11.0/26, gateway 172.22.11.1, broadcast 172.22.11.63
- Blackhull (10 hosts / 14 usables): 172.22.11.64/28, gateway 172.22.11.65, broadcast 172.22.11.79
- P2P R1-R2 (2 hosts / 2 usables): 172.22.11.80/30, gateway 172.22.11.81, broadcast 172.22.11.83

## Plan IPv6

Prefijos /64 asignados desde 2001:25:22::/48, ordenados de mayor a menor tamaño de red:

- Estudiantes: 2001:25:22:1::/64, gateway 2001:25:22:1::1
- Docentes: 2001:25:22:2::/64, gateway 2001:25:22:2::1
- Gestión: 2001:25:22:3::/64, gateway 2001:25:22:3::1
- Voz: 2001:25:22:4::/64, gateway 2001:25:22:4::1
- Blackhull R1: 2001:25:22:5::/64, gateway 2001:25:22:5::1
- Académicos: 2001:25:22:6::/64, gateway 2001:25:22:6::1
- Finanzas: 2001:25:22:7::/64, gateway 2001:25:22:7::1
- Datacenter: 2001:25:22:8::/64, gateway 2001:25:22:8::1
- Blackhull R2: 2001:25:22:9::/64, gateway 2001:25:22:9::1
- Enlace P2P R1-R2: 2001:25:22:a::/64, gateway 2001:25:22:a::1

## Tecnologías implementadas

- VLANs y VTP para segmentación y propagación entre switches
- EtherChannel y STP para redundancia en capa 2
- HSRP para alta disponibilidad de gateway
- OSPFv2 para enrutamiento dinámico entre routers

## Estructura del repositorio

configs/      configuraciones de cada dispositivo
topologia/    diagrama y mapa de puertos
pruebas/      scripts y resultados de pruebas
README.md     este documento

## Estado del proyecto

Sprint 1: diseño de direccionamiento, topología y VLANs - completado
Sprint 2: VLANs, VTP, STP, EtherChannel, HSRP - en progreso
Sprint 3: OSPFv2, pruebas y documentación final - pendiente




