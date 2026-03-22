| 2^0   | 2^1   |2^2   | 2^3  | 2^4  | 2^5  | 2^6  | 2^7  | 2^8  |
| :---: | :---: | :---:| :---:| :---:| :---:| :---:| :---:| :---:|
| 1| 2| 4| 8| 16| 32| 64| 128| 256|


| Nombre d'équipements | Puissance^2 | Formule CIDR | Calculs CIDR
| :---: | :---: | :---: | :---: |
| 50 équipements (Info) | 2^6 = 64 |  32 -n^ | 32 - 6 = /26 |
| 20 équipements (Admin) | 2^5 = 32 |  32 -n^ | 32 - 5 = /27 |
| 15 équipements (Tech) | 2^5 = 32 |  32 -n^ | 32 - 5 = /27 |
| 12 équipements (Dev) | 2^4 = 16 |  32 -n^ | 32 - 4 = /28 |

| Pour le réseau 172.16.1.0/24, on a donc les 4 sous-réseaux suivants : |
| :---: |

* Sous-réseau 1 : Saut de 64 IP
* Sous-réseau 2 : Saut de 32 IP
* Sous-réseau 3 : Saut de 32 IP
* Sous-réseau 4 : Saut de 16 IP

| Sous-réseau 1 | Pôle informatique |
| :---: | :---: |
|Adresse de réseau | 172.16.1.0/26  |
|Début de plage IP disponible | 172.16.1.1 |  
|Fin de plage IP disponible | 172.16.1.62 | 
|Adresse de broadcast | 172.16.1.63 | 


| Sous-réseau 2 | Pôle Administratif  |
| :---: | :---: |
|Adresse de réseau | 172.16.1.64/27  |
|Début de plage IP disponible | 172.16.1.65 | 
|Fin de plage IP disponible | 172.16.1.94 | 
|Adresse de broadcast | 172.16.1.95 |

| Sous-réseau 3 | Pôle Technicien  |
| :---: | :---: |
|Adresse de réseau | 172.16.1.96/27  |
|Début de plage IP disponible | 172.16.1.97 | 
|Fin de plage IP disponible | 172.16.1.126  |
|Adresse de broadcast | 172.16.1.127  |

| Sous-réseau 4 | Pôle Développement |  
| :---: | :---: |
|Adresse de réseau | 172.16.1.128/28  |
|Début de plage IP disponible | 172.16.1.129 |  
|Fin de plage IP disponible | 172.16.1.142  |
|Adresse de broadcast | 172.16.1.143  |


| Pôles         |Adresse réseau |	Adresse de broadcast |	Adresse de début de plage	| Adresse de fin de plage |
| :---: | :---: | :---: | :---: | :---: |
| Informatique	  | 172.16.1.0/26|	172.16.1.63|	172.16.1.1|	172.16.1.62|
| Administratif  |	172.16.1.64/27|	172.16.1.95|	172.16.1.65|	172.16.1.94|
| Technicien|	172.16.1.96/27|	172.16.1.127|	172.16.1.97|	172.16.1.126|
| Développement |	172.16.1.128/28|	172.16.1.143|	172.16.1.129|	172.16.1.142|






