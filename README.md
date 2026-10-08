# Cahier des Charges - Gestion des Pannes Réseau

## 1. Objectif du projet

Permettre aux techniciens de recevoir une alerte immédiate lorsqu'un serveur tombe en
panne.

## 2. Exigences fonctionnelles

- **Exigence 1 :** Le système doit détecter la panne d'un serveur via une sonde SNMP.
- **Exigence 2 :** Le système doit envoyer un email au technicien responsable.
- **Exigence 3 :** Le site doit être accessible même le lundi matin.
- **exigence 4 :** Le système doit respecter un délais lors de la panne d'un serveur
- **Exigence 10 :** Si pannes, changer de serveur.
- **Exigence 11 :** Si pannes sur le deuxième serveur, passer au troisième

                                                                                                                                                                                                 
                                                                                                                                                                                                 
PPPPPPPPPPPPPPPPP   LLLLLLLLLLL                            AAA           YYYYYYY       YYYYYYY                                                                                                   
P::::::::::::::::P  L:::::::::L                           A:::A          Y:::::Y       Y:::::Y                                                                                                   
P::::::PPPPPP:::::P L:::::::::L                          A:::::A         Y:::::Y       Y:::::Y                                                                                                   
PP:::::P     P:::::PLL:::::::LL                         A:::::::A        Y::::::Y     Y::::::Y                                                                                                   
  P::::P     P:::::P  L:::::L                          A:::::::::A       YYY:::::Y   Y:::::YYY                                                                                                   
  P::::P     P:::::P  L:::::L                         A:::::A:::::A         Y:::::Y Y:::::Y                                                                                                      
  P::::PPPPPP:::::P   L:::::L                        A:::::A A:::::A         Y:::::Y:::::Y                                                                                                       
  P:::::::::::::PP    L:::::L                       A:::::A   A:::::A         Y:::::::::Y                                                                                                        
  P::::PPPPPPPPP      L:::::L                      A:::::A     A:::::A         Y:::::::Y                                                                                                         
  P::::P              L:::::L                     A:::::AAAAAAAAA:::::A         Y:::::Y                                                                                                          
  P::::P              L:::::L                    A:::::::::::::::::::::A        Y:::::Y                                                                                                          
  P::::P              L:::::L         LLLLLL    A:::::AAAAAAAAAAAAA:::::A       Y:::::Y                                                                                                          
PP::::::PP          LL:::::::LLLLLLLLL:::::L   A:::::A             A:::::A      Y:::::Y                                                                                                          
P::::::::P          L::::::::::::::::::::::L  A:::::A               A:::::A  YYYY:::::YYYY                                                                                                       
P::::::::P          L::::::::::::::::::::::L A:::::A                 A:::::A Y:::::::::::Y                                                                                                       
PPPPPPPPPP          LLLLLLLLLLLLLLLLLLLLLLLLAAAAAAA                   AAAAAAAYYYYYYYYYYYYY                                                                                                       
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
UUUUUUUU     UUUUUUUULLLLLLLLLLL       TTTTTTTTTTTTTTTTTTTTTTTRRRRRRRRRRRRRRRRR                  AAA               KKKKKKKKK    KKKKKKKIIIIIIIIIILLLLLLLLLLL             LLLLLLLLLLL             
U::::::U     U::::::UL:::::::::L       T:::::::::::::::::::::TR::::::::::::::::R                A:::A              K:::::::K    K:::::KI::::::::IL:::::::::L             L:::::::::L             
U::::::U     U::::::UL:::::::::L       T:::::::::::::::::::::TR::::::RRRRRR:::::R              A:::::A             K:::::::K    K:::::KI::::::::IL:::::::::L             L:::::::::L             
UU:::::U     U:::::UULL:::::::LL       T:::::TT:::::::TT:::::TRR:::::R     R:::::R            A:::::::A            K:::::::K   K::::::KII::::::IILL:::::::LL             LL:::::::LL             
 U:::::U     U:::::U   L:::::L         TTTTTT  T:::::T  TTTTTT  R::::R     R:::::R           A:::::::::A           KK::::::K  K:::::KKK  I::::I    L:::::L                 L:::::L               
 U:::::D     D:::::U   L:::::L                 T:::::T          R::::R     R:::::R          A:::::A:::::A            K:::::K K:::::K     I::::I    L:::::L                 L:::::L               
 U:::::D     D:::::U   L:::::L                 T:::::T          R::::RRRRRR:::::R          A:::::A A:::::A           K::::::K:::::K      I::::I    L:::::L                 L:::::L               
 U:::::D     D:::::U   L:::::L                 T:::::T          R:::::::::::::RR          A:::::A   A:::::A          K:::::::::::K       I::::I    L:::::L                 L:::::L               
 U:::::D     D:::::U   L:::::L                 T:::::T          R::::RRRRRR:::::R        A:::::A     A:::::A         K:::::::::::K       I::::I    L:::::L                 L:::::L               
 U:::::D     D:::::U   L:::::L                 T:::::T          R::::R     R:::::R      A:::::AAAAAAAAA:::::A        K::::::K:::::K      I::::I    L:::::L                 L:::::L               
 U:::::D     D:::::U   L:::::L                 T:::::T          R::::R     R:::::R     A:::::::::::::::::::::A       K:::::K K:::::K     I::::I    L:::::L                 L:::::L               
 U::::::U   U::::::U   L:::::L         LLLLLL  T:::::T          R::::R     R:::::R    A:::::AAAAAAAAAAAAA:::::A    KK::::::K  K:::::KKK  I::::I    L:::::L         LLLLLL  L:::::L         LLLLLL
 U:::::::UUU:::::::U LL:::::::LLLLLLLLL:::::LTT:::::::TT      RR:::::R     R:::::R   A:::::A             A:::::A   K:::::::K   K::::::KII::::::IILL:::::::LLLLLLLLL:::::LLL:::::::LLLLLLLLL:::::L
  UU:::::::::::::UU  L::::::::::::::::::::::LT:::::::::T      R::::::R     R:::::R  A:::::A               A:::::A  K:::::::K    K:::::KI::::::::IL::::::::::::::::::::::LL::::::::::::::::::::::L
    UU:::::::::UU    L::::::::::::::::::::::LT:::::::::T      R::::::R     R:::::R A:::::A                 A:::::A K:::::::K    K:::::KI::::::::IL::::::::::::::::::::::LL::::::::::::::::::::::L
      UUUUUUUUU      LLLLLLLLLLLLLLLLLLLLLLLLTTTTTTTTTTT      RRRRRRRR     RRRRRRRAAAAAAA                   AAAAAAAKKKKKKKKK    KKKKKKKIIIIIIIIIILLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLL
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
                                                                                                                                                                                                 
