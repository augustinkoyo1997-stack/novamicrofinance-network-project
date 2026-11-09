# Plan d'adressage IPv6 - NovaMicrofinance

Préfixe de documentation utilisé : 2001:db8::/32

## Un /48 par site

| Site | Préfixe |
|---|---|
| Siège | 2001:db8:1::/48 |
| Agence A | 2001:db8:2::/48 |
| Agence B | 2001:db8:3::/48 |

## Siège : un /64 par VLAN

| VLAN | Nom | Préfixe |
|---|---|---|
| 10 | USERS | 2001:db8:1:10::/64 |
| 20 | SERVEURS | 2001:db8:1:20::/64 |
| 30 | ADMIN | 2001:db8:1:30::/64 |
| 40 | WIFI-INVITES | 2001:db8:1:40::/64 |
| 99 | MANAGEMENT | 2001:db8:1:99::/64 |

## Principes
- /64 pour tous les réseaux locaux.
- Numéro de VLAN repris dans l'adresse pour la lisibilité.
- Dual stack avec le plan IPv4.
