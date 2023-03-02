# Maze
> Classe Labyrinthe Représentation sous forme de graphe non-orienté dont chaque sommet est une cellule  *(un tuple  *(l,c)* )*  et dont la structure est représentée par un dictionnaire - clés : sommets - valeurs : ensemble des sommets voisins accessibles 
## Constructeur *(self, height, width, empty=False)* 
> Constructeur d'un labyrinthe de height cellules de haut et de width cellules de large Les voisinages sont initialisés à des ensembles vides Remarque : dans le labyrinthe créé, chaque cellule est complètement emmurée 
## info *(self)* 
> **NE PAS MODIFIER CETTE MÉTHODE** Affichage des attributs d'un objet 'Maze'  *(fonction utile pour deboguer)*    
**Retour:**  
> chaîne  *(string)* : description textuelle des attributs de l'objet 
## __str__ *(self)* 
> **NE PAS MODIFIER CETTE MÉTHODE** Représentation textuelle d'un objet Maze  *(en utilisant des caractères ascii)*    
**Retour:**  
> chaîne  *(str)*  : chaîne de caractères représentant le labyrinthe 
## add_wall *(self, c1, c2)* 
> Ajoute un mur entre deux cellules adjacentes   
**Paramètres:**  
> c1  *(tuple)* , c2  *(tuple)* : cellules adjacentes 
## remove_wall *(self, c1, c2)* 
> Supprime un mur entre deux cellules adjacentes   
**Paramètres:**  
> c1, c2 : cellules adjacentes 
## get_walls *(self)* 
> Retourne la liste des murs du labyrinthe   
**Retour:**  
> walls  *(list)*  : liste de couples de cellules 
## fill *(self)* 
> Remplissage du labyrinthe en ajoutant des murs entre toutes les cellules 
## empty *(self)* 
> Vide le labyrinthe en supprimant tous les murs 
## get_contiguous_cells *(self, c)* 
> Retourne la liste des cellules contiguës à une cellule donnée  *(sans s’occuper des éventuels murs)*    
**Paramètre:**  
> c  *(tuple)*  : cellule   
**Retour:**  
> cellules  *(list)*  : liste de cellules contiguës 
## get_reachable_cells *(self, c)* 
> Retourne la liste des cellules accessibles depuis une cellule donnée   
**Paramètre:**  
> c : cellule   
**Retour:**  
> liste de cellules 
## <u>gen_btree</u>  *(cls, h, w)* 
> Génère un labyrinthe aléatoire selon l'algorithme de génération par arbre binaire   
**Paramètres:**  
> h, w : dimensions du labyrinthe 
## <u>gen_sidewinder</u>  *(cls, h, w)* 
> Génère un labyrinthe aléatoire selon l'algorithme de génération de Sidewinder   
**Paramètres:**  
> h, w : dimensions du labyrinthe 
## <u>gen_fusion</u>  *(cls, h, w)* 
> Génère un labyrinthe aléatoire selon l'algorithme de génération de fusion   
**Paramètres:**  
> h, w : dimensions du labyrinthe 
## <u>gen_exploration</u>  *(cls, h, w)* 
> Génère un labyrinthe aléatoire selon l'algorithme de génération par exploration   
**Paramètres:**  
> h, w : dimensions du labyrinthe 
## <u>gen_wilson</u>  *(cls, h, w)* 
> Génère un labyrinthe aléatoire selon l'algorithme de génération de Wilson   
**Paramètres:**  
> h, w : dimensions du labyrinthe 
## overlay *(self, content=None)* 
> Rendu en mode texte, sur la sortie standard,  d'un labyrinthe avec du contenu dans les cellules   
**Paramètres:**  
> content  *(dict)*  : dictionnaire tq content[cell] contient le caractère à afficher au milieu de la cellule   
**Retour:**  
> string 
## solve_dfs *(self, start, stop)* 
> Résout un labyrinthe en utilisant l'algorithme de recherche en profondeur   
**Paramètres:**  
> start, stop : cellules de départ et d'arrivée   
**Retour:**  
> list : liste des cellules du chemin trouvé 
## solve_bfs *(self, start, stop)* 
> Résout un labyrinthe en utilisant l'algorithme de recherche en largeur   
**Paramètres:**  
> start, stop : cellules de départ et d'arrivée   
**Retour:**  
> list : liste des cellules du chemin trouvé 
## distance_geo *(self, c1, c2)* 
> Calcul la distance géodésique entre la cellule c1 et la cellule c2, c'est à dire le nombre minimal de déplacements nécessaires pour aller de c1 à c2   
**Paramètres:**  
> c1, c2 : cellules   
**Retour:**  
> int : distance géodésique entre c1 et c2 
## distance_man *(self, c1, c2)* 
> Calcul la distance de Manhattan entre la cellule c1 et la cellule c2, c'est à dire le nombre minimal de déplacements nécessaires pour aller de c1 à c2 si le labyrinthe était vide de tout mur   
**Paramètres:**  
> c1, c2 : cellules   
**Retour:**  
> int : distance de Manhattan entre c1 et c2 
## get_mat *(self)* 
> Retourne la matrice représentant le labyrinthe, 0 pour un mur, 1 pour une cellule libre 
