# Plan d'adressage v0 - NovaMicrofinance

## Plages privées RFC 1918

| Plage | CIDR |
|---|---|
| 10.0.0.0 - 10.255.255.255 | 10.0.0.0/8 |
| 172.16.0.0 - 172.31.255.255 | 172.16.0.0/12 |
| 192.168.0.0 - 192.168.255.255 | 192.168.0.0/16 |

Plage retenue : 10.0.0.0/8 (beaucoup de place pour l'évolution et les futures agences).

## Siège (provisoire)

| VLAN | Nom | Réseau |
|---|---|---|
| 10 | USERS | 10.1.10.0/24 |
| 20 | SERVEURS | 10.1.20.0/24 |
| 30 | ADMIN | 10.1.30.0/24 |
| 40 | WIFI-INVITES | 10.1.40.0/24 |
| 99 | MANAGEMENT | 10.1.99.0/24 |
