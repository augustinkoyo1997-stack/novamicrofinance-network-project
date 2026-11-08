# Méthode de dépannage OSI - NovaMicrofinance

Principe : on diagnostique de la couche 1 vers la couche 7 et on s'arrête à la première défaillance.

| Couche | Vérification | Outil / commande |
|---|---|---|
| 1 - Physique | Câble, voyant, lien | Observation, show interfaces |
| 2 - Liaison | VLAN, adresse MAC | show vlan, show mac address-table |
| 3 - Réseau | IP, masque, passerelle | ipconfig, ping |
| 4 - Transport | Port ouvert, filtrage | telnet, netstat |
| 7 - Application | Service actif | Navigateur, nslookup |

## Cas d'étude
Agence A : l'application bancaire est inaccessible. Ping passerelle OK, ping serveur siège en échec : problème de couche 3 sur le lien WAN.
