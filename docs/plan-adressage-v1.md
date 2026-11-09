# Plan d'adressage v1 - Siège NovaMicrofinance

| VLAN | Nom | Besoin | Réseau | Passerelle | Broadcast |
|---|---|---|---|---|---|
| 10 | USERS | 80 | 10.1.10.0/24 | 10.1.10.1 | 10.1.10.255 |
| 20 | SERVEURS | 20 | 10.1.20.0/24 | 10.1.20.1 | 10.1.20.255 |
| 30 | ADMIN | 10 | 10.1.30.0/24 | 10.1.30.1 | 10.1.30.255 |
| 40 | WIFI-INVITES | 30 | 10.1.40.0/24 | 10.1.40.1 | 10.1.40.255 |
| 99 | MANAGEMENT | 12 | 10.1.99.0/28 | 10.1.99.1 | 10.1.99.15 |

## Justification des choix
- /24 par VLAN : lisibilité (le VLAN est dans le 3e octet), marge de croissance, les adresses privées en 10.0.0.0/8 sont abondantes.
- /28 pour MANAGEMENT : peu d'équipements, réseau d'administration volontairement restreint.
- /30 sur les liens WAN : 2 adresses suffisent (un routeur à chaque extrémité).
- Passerelle = première adresse utilisable (.1) de chaque réseau.
