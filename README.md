# Challenge-D-coupage-de-r-seaux-IP
172.16.1.0/24  donc 2^8 =256 - 2(Adresse Réseau et brodcast) 254 adresse disponible 

A.Symétrique  

les besoins du pôle ayant le plus grand besoin (50 équipements) donc 
On divise en 4 le nombre de sous-réseaux égaux  donc 64 pour chaque Pole 
nous choisissons un sous-réseau /26 pour tous les pôles. Un sous-réseau /26 offre 64 adresses IP au total (2^6) dont 62 utilisables (2 adresses réservées pour le réseau et la diffusion).



## Découpage Symétrique

| Pôle              | Sous-réseau         | Adresse Réseau | Adresse Broadcast | Début de plage | Fin de plage |
|-------------------|---------------------|----------------|-------------------|----------------|--------------|
| Informatique      | 172.16.1.0/26       | 172.16.1.0     | 172.16.1.63       | 172.16.1.1     | 172.16.1.62  |
| Administratif     | 172.16.1.64/26      | 172.16.1.64    | 172.16.1.127      | 172.16.1.65    | 172.16.1.126 |
| Technicien        | 172.16.1.128/26     | 172.16.1.128   | 172.16.1.191      | 172.16.1.129   | 172.16.1.190 |
| Développement     | 172.16.1.192/26     | 172.16.1.192   | 172.16.1.255      | 172.16.1.193   | 172.16.1.254 |


B.Asymétrique
## Découpage Asymétrique

| Pôle              | Sous-réseau         | Adresse Réseau | Adresse Broadcast | Début de plage | Fin de plage |
|-------------------|---------------------|----------------|-------------------|----------------|--------------|
| Informatique      | 172.16.1.0/26       | 172.16.1.0     | 172.16.1.63       | 172.16.1.1     | 172.16.1.62  |
| Administratif     | 172.16.1.64/27      | 172.16.1.64    | 172.16.1.95       | 172.16.1.65    | 172.16.1.94  |
| Technicien        | 172.16.1.96/28      | 172.16.1.96    | 172.16.1.111      | 172.16.1.97    | 172.16.1.110 |
| Développement     | 172.16.1.112/28     | 172.16.1.112   | 172.16.1.127      | 172.16.1.113   | 172.16.1.126 |

 


Explication :

Informatique  c'est 50 équipements  2^6= 64 adresses   CIDR : /26

Administratif : 20 équipements    2^5= 32 adresses     CIDR : /27

Technicien : 15 équipements    2^4= 16 adresses        CIDR :/28

Développement : 12 équipements     2^4=16 adresses     CIDR  : /28
  
