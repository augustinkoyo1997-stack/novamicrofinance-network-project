# Protocoles et ports - NovaMicrofinance

Ce document liste les ports que le réseau doit autoriser. Il servira de base aux futures règles de pare-feu (principe du moindre privilège : on n'autorise que le nécessaire).

## Ports à autoriser

| Port | Protocole | Service | Pourquoi |
|---|---|---|---|
| 443 | TCP | HTTPS | Accès web sécurisé et application métier bancaire |
| 80 | TCP | HTTP | Redirection vers HTTPS uniquement |
| 53 | UDP/TCP | DNS | Résolution des noms (annuaire d'Internet et interne) |
| 67-68 | UDP | DHCP | Attribution automatique des adresses IP aux postes |
| 22 | TCP | SSH | Administration sécurisée des équipements (VLAN ADMIN uniquement) |
| 3389 | TCP | RDP | Bureau à distance vers les serveurs (VLAN ADMIN uniquement) |
| 25 | TCP | SMTP | Envoi des e-mails (serveur de messagerie) |

## Protocoles de diagnostic

| Protocole | Couche | Usage |
|---|---|---|
| ICMP | 3 | ping et traceroute, à autoriser en interne pour le dépannage |
| ARP | 2 | Résolution IP vers MAC (reste dans le réseau local) |

## Règles de principe

- Le VLAN INVITES n'a accès qu'à Internet (80, 443, 53).
- SSH et RDP sont réservés au VLAN ADMIN.
- Tout le reste est refusé par défaut.

## Preuve de lab

Ports observés en mode Simulation (à compléter avec vos propres observations) :

- Port source : 1028 (éphémère, choisi par le PC)
- Port destination : 80 (HTTP)
