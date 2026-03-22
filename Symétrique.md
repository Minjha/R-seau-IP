On a un réseau en **172.16.1.0/24**  
On coupe en 4 sous-réseau symétrique : 

* _Pôle informatique_
* _Pôle Administratif_
* _Pôle Technicien_
* _Pôle Développement_

Chaque sous-réseau doit accueillir *50* équipements.  
On cherhche dans le tableau, la puissance^ > à 50.  
>La puissance 2^6 = 64 est > à 50. 

64 adresses IP disponibles au total dont 2 pour le réseau et le broadcast.  
Donc 62 adresses IP utilisables pour chaque pôle.  
>Le CIDR = 32 -n^  
Soit : 32 - 6 = 26.  

Le CIDR est /26  

1. Pôle informatique  
Adresse de réseau : 172.16.1.0/26  
Début de plage IP disponible : 172.16.1.1/26  
Fin de plage IP disponible : 172.16.1.62/26  
Adresse de broadcast : 172.16.1.63/26

2. Pôle administratif  
Adresse de réseau : 172.16.1.64/26  
Début de plage IP disponible : 172.16.1.65/26  
Fin de plage IP disponible : 172.16.1.126/26  
Adresse de broadcast : 172.16.1.127/26

3. Pôle technicien  
Adresse de réseau : 172.16.1.128/26  
Début de plage IP disponible : 172.16.1.129/26  
Fin de plage IP disponible : 172.16.1.190/26  
Adresse de broadcast : 172.16.1.191/26

4. Pôle développement  
Adresse de réseau : 172.16.1.192/26  
Début de plage IP disponible : 172.16.1.193/26  
Fin de plage IP disponible : 172.16.1.254/26  
Adresse de broadcast : 172.16.1.255/26

| Pôles | Adresse réseau |	Adresse de broadcast | Adresse de début de plage | Adresse de fin de plage
| :---: | :---:          | :---:                 | :---:                     | :---: |
|Informatique	|  172.16.1.0/26	| 172.16.1.63	| 172.16.1.1	 | 172.16.1.62 |
|Administratif | 172.16.1.64/26	| 172.16.1.127	| 172.16.1.65	 | 172.16.1.126 |
|Technicien | 172.16.1.128/26    |	172.16.1.191|	172.16.1.129	 | 172.16.1.190 |
|Développement |	172.16.1.192/26|	172.16.1.255 |	172.16.1.193	| 172.16.1.254 |

