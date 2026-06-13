# Producto 1 - Red Empresarial (Equipo 4)
**Materia:** Conmutación y Enrutamiento (TI-203) - ITLA
**Plataforma:** PNETLab

## Descripción general

Este proyecto implementa una red empresarial de mediana escala, segmentada por departamentos mediante VLANs, con alta disponibilidad de gateway (HSRP), redundancia de enlace (EtherChannel y STP) y enrutamiento dinámico con OSPFv2 (área única y soporte para multiárea).

## Bloque de direcciones asignado (Equipo 4)

- **IPv4:** 172.22.0.0/15
- **IPv6:** 2001:25:22::/48

## Plan de direccionamiento IPv4 (VLSM)

### R1-Core

| VLAN | Hosts requeridos | Máscara | Red asignada |
|---|---|---|---|
| Estudiantes | 1500 | /21 | 172.22.0.0/21 |
| Docentes | 164 | /24 | 172.22.8.0/24 |
| Gestión | 29 | /27 | 172.22.10.0/27 |
| Voz | 16 | /28 | 172.22.10.32/28 |
| Blackhull | 10 | /28 | 172.22.10.48/28 |

### R2

| VLAN | Hosts requeridos | Máscara | Red asignada |
|---|---|---|---|
| Académicos | 80 | /25 | 172.22.9.0/25 |
| Finanzas | 64 | /26 | 172.22.9.128/26 |
| Datacenter | 44 | /26 | 172.22.9.192/26 |
| Blackhull | 10 | /28 | 172.22.10.64/28 |
| P2P (enlace R1-R2) | 2 | /30 | 172.22.10.80/30 |

## Plan de direccionamiento IPv6

Asignación de prefijos /64 a partir de 2001:25:22::/48, ordenados según el tamaño de la red IPv4 correspondiente (la red más grande recibe el primer prefijo).

| VLAN | Prefijo IPv6 |
|---|---|
| Estudiantes | 2001:25:22:1::/64 |
| Docentes | 2001:25:22:2::/64 |
| Académicos | 2001:25:22:3::/64 |
| Finanzas | 2001:25:22:4::/64 |
| Datacenter | 2001:25:22:5::/64 |
| Gestión | 2001:25:22:6::/64 |
| Voz | 2001:25:22:7::/64 |
| Blackhull (R1) | 2001:25:22:8::/64 |
| Blackhull (R2) | 2001:25:22:9::/64 |
| P2P (R1-R2) | 2001:25:22:a::/64 |

## VLANs por router

**R1-Core:** Docentes, Estudiantes, Gestión, Voz, Blackhull
**R2:** Finanzas, Académicos, Datacenter, Blackhull, enlace P2P hacia R1




- **Sprint 1:** Diseño de direccionamiento, topología lógica/física, VLANs y VTP. ✅
- **Sprint 2:** Implementación de VLANs, VTP, STP, EtherChannel y HSRP. ⏳
- **Sprint 3:** OSPFv2, pruebas funcionales y documentación final. ⏳
