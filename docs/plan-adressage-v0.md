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

## Découpage VLSM des agences

### Agence A (10.2.0.0/16)

| Réseau | Adresse/masque | Hôtes utilisables | Broadcast |
|---|---|---|---|
| LAN Agence A | 10.2.10.0/25 | 10.2.10.1 à 10.2.10.126 | 10.2.10.127 |

### Agence B (10.3.0.0/16)

| Réseau | Adresse/masque | Hôtes utilisables | Broadcast |
|---|---|---|---|
| LAN Agence B | 10.3.10.0/25 | 10.3.10.1 à 10.3.10.126 | 10.3.10.127 |

### Liens WAN (point à point)

| Lien | Réseau | Hôtes utilisables | Broadcast |
|---|---|---|---|
| Siège - Agence A | 10.2.0.0/30 | 10.2.0.1 et 10.2.0.2 | 10.2.0.3 |
| Siège - Agence B | 10.3.0.0/30 | 10.3.0.1 et 10.3.0.2 | 10.3.0.3 |

### Justification
- /25 par agence : 126 hôtes pour 60 employés, soit une marge de croissance confortable (imprimantes, Wi-Fi, nouveaux postes).
- /30 pour les liens WAN : 2 adresses suffisent (un routeur à chaque extrémité), aucun gaspillage.
