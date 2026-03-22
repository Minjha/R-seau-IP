1.Effectuer le découpage réseau pour une entreprise en donnant la formule utilisée pour chaque réseau découpé ainsi que le CIDR qui lui correspond pour permettre d'adresser ses équipements.
2.Calculer pour chaque réseau, l'adresse réseau et l'adresse de diffusion (Broadcast)
3.Présenter ce découpage dans un fichier texte en markdown, à la suite, ou sous forme de tableau

Les différentes plages d'adresses sont valides
Il y a assez de place dans chaque plage pour accueillir le nombre d'équipements prévus
La méthode de calcul est expliquée clairement
Les adresses de réseau et de diffusion sont correctes
Il y a le résultats pour un découpage symétrique et pour un découpage asymétrique.

| Le Pôle | Nombre des bureaux | 
| :---:  | :---: |
| Informatique | 6 bureaux  |
| Administratif | 4 bureaux |
| Technicien | 4 bureaux |
| Développement | 6 bureaux |

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

1. Sous-réseau 1 : Saut de 64 IP
2. Sous-réseau 2 : Saut de 32 IP
3. Sous-réseau 3 : Saut de 32 IP
4. Sous-réseau 4 : Saut de 16 IP

1. Sous-réseau 1 : Pôle informatique 
Adresse de réseau : 172.16.1.0/24
Début de plage IP disponible : 172.16.1.1
Fin de plage IP disponible : 172.16.1.62
Adresse de broadcast : 172.16.1.63

2. Sous-réseau 2 : Pôle Administratif
Adresse de réseau : 172.16.1.64/24
Début de plage IP disponible : 172.16.1.65
Fin de plage IP disponible : 172.16.1.92
Adresse de broadcast : 172.16.1.93

3. Sous-réseau 3 : Pôle Technicien 
Adresse de réseau : 172.16.1.96/24
Début de plage IP disponible : 172.16.1.97
Fin de plage IP disponible : 172.16.1.126
Adresse de broadcast : 172.16.1.127

4. Sous-réseau 4 : Pôle Développement 
Adresse de réseau : 172.16.1.128/24
Début de plage IP disponible : 172.16.1.129
Fin de plage IP disponible : 172.16.1.142
Adresse de broadcast : 172.16.1.143










| :---: | | :---: | :---: |
