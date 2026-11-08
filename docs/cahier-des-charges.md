# Cahier des charges - NovaMicrofinance

## Client
NovaMicrofinance, institution de microfinance, environ 200 employés.

## Sites

| Site | Effectif | Rôle |
|---|---|---|
| Siège | 80 | Direction, comptabilité, IT, datacenter (serveurs) |
| Agence A | 60 | Guichets, agents de crédit |
| Agence B | 60 | Guichets, agents de crédit |

## Services à fournir

- Accès à l'application métier bancaire (hébergée au siège)
- Annuaire utilisateurs centralisé (Active Directory), DNS, DHCP
- Serveur de fichiers et messagerie
- Wi-Fi employés et Wi-Fi invités (séparés)
- Accès Internet sécurisé

## Contraintes

- **Disponibilité** : les agences ne doivent jamais perdre l'accès à l'application (redondance des liens et équipements critiques)
- **Sécurité** : données clients confidentielles, segmentation stricte entre utilisateurs, serveurs, invités et administration
- **Évolutivité** : prévoir l'ouverture de 2 agences supplémentaires
- **Budget** : matériel Cisco, firewall Fortinet, extension cloud

## VLAN prévus

| VLAN | Nom | Usage |
|---|---|---|
| 10 | USERS | Postes employés |
| 20 | SERVEURS | AD, DNS, DHCP, application métier |
| 30 | ADMIN | Équipe IT |
| 40 | WIFI-INVITES | Clients et visiteurs |
| 99 | MANAGEMENT | Administration des équipements |
