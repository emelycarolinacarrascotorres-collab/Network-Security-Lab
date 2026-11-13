# Evidencias — checklist

| Requisito | Evidencia | Comando / captura | Estado |
|---|---|---|---|
| 01 RADIUS | Config router | `show running-config \| section radius` / `section aaa` | ✅ |
| 01 RADIUS | NPS, AD, políticas | Capturas de consola NPS y ADUC | ✅ |
| 01 RADIUS | Login con usuario AD | `ssh <usuarioAD>@20.25.6.1` → `images/radius/login-radius.png` | ✅ |
| 01 RADIUS | Login local/fallback | NPS detenido, `ssh admin@...` → `login-local.png` | ✅ |
| 02 VPN | GUI FortiGate (config) | `images/vpn/fortigate-vpn-config.png` | ✅ |
| 02 VPN | Túnel UP (GUI) | `fortigate-tunnel-up.png`; router: `show crypto isakmp sa` / `show crypto ipsec sa` | ⏳ |
| 04 SNMP | Config | `show running-config \| include snmp` | ✅ |
| 04 SNMP | Lectura | `snmpwalk` | ✅ |
| 04 SNMP | `snmpget` | `snmpget -v2c -c <com> 20.25.6.1 1.3.6.1.2.1.1.5.0` |  |
| 04 SNMP | Escritura rechazada | `snmpset` → `noAccess` | ✅ |
| 05 DHCP | Config, pool, binding, cliente | `section dhcp`, `show ip dhcp pool`, `show ip dhcp binding`, `ipconfig` | ✅ |
| 06 CIS | Ejecución e informe | `python cis_hardening.py` (solo lectura) | ✅ |
| 07 SSH | Config y login | `show ip ssh`, login a router y switch | ✅ |
| 08 Direccionamiento | Interfaces y pings | `show ip interface brief`, `ping` | ✅ |
| Extra Zabbix | Host y datos | GUI Zabbix | ✅ |
| Video | Enlace | https://youtu.be/c5fdI4BFvHI | ✅ |

