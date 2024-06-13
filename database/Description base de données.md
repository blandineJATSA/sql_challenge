J'ai recupéré  sur kaggle la base de données de TheLook.

TheLook est un site e-commerce fictif de vêtements développé par l'équipe Looker. Le jeu de données contient des informations sur les clients, les produits, 
les commandes, la logistique, les événements web et les campagnes de marketing digital. 
Il s'agit d'un jeu de données publique que j'utiliserai à des fins d'analyse de données et d'appentissage du SQL.


Cette base de données contient 7 tables qui suit :

### **- distribution_centers.csv**

Cette base de données decrire les centres de distribution des produits.

id : Identifiant unique pour chaque centre de distribution

name : Nom du centre de distribution

latitude : Coordonnée de latitude du centre de distribution

longitude : Coordonnée de longitude du centre de distribution 




### **- events.csv**

Elle capture les evenenements et les interactions que le site a avec les clients.

id : Identifiant unique de chaque evenement
Chaque fois qu'un utilisateur effectue une action sur le site ou l'application, un nouvel enregistrement est ajouté à la table events avec le type d'événement correspondant.
Ainsi, si un utilisateur consulte 10 produits différents, il y aura 10 enregistrements dans la table events avec le event_type égal à view_product.


user_id : Identifiant de l'utilisateur associé à l'événement web

sequence_number : Cette colonne indique l'ordre des événements dans une séquence donnée, souvent pour un utilisateur ou une session spécifique. Par exemple, si un utilisateur visite plusieurs pages d'un site web dans une session, chaque événement de "view_product" ou de "add_to_cart" pourrait avoir un numéro de séquence croissant pour cette session spécifique. Cela permet d'analyser le parcours de l'utilisateur à travers votre application ou votre site web.

event_type : Cette colonne indique le type d'événement qui s'est produit. Par exemple, dans une application de commerce électronique, les types d'événements pourraient inclure "view_product" (consultation de produit), "add_to_cart" (ajout au panier), "purchase" (achat), etc. Comprendre les différents types d'événements peut être crucial pour analyser le comportement des utilisateurs et améliorer l'expérience utilisateur.  

session_id : Identifiant de la session pendant laquelle l'événement s'est produit

created_at : Horodatage indiquant quand l'événement a eu lieu

ip_address : Adresse IP d'où l'événement a originaire ( provient)

city : Ville où l'événement s'est produit

state : État où l'événement s'est produit

postal_code : Code postal du lieu de l'événement

browser : Navigateur web utilisé pendant l'événement






### **- inventory_items.csv**

contient les informations sur les artciles en stock

id  : Identifiant unique pour chaque article en stock

product_id : Identifiant du produit associé

created_at : Horodatage indiquant quand l'article en stock a été créé

sold_at : Horodatage indiquant quand l'article a été vendu

cost : Coût de l'article en stock

product_category : Catégorie du produit associé

product_name : Nom du produit associé

product_brand : Marque du produit associé.

product_retail_price : Prix de détail du produit associé.

product_department : Département auquel le produit appartient.





### **-  order_items.csv**

Elle contient les informations sur chaque article de commande

id : Identifiant unique pour chaque élément de commande

order_id : Identifiant de la commande associée.

user_id : Identifiant de l'utilisateur ayant passé la commande.

product_id : Identifiant du produit associé.

inventory_item_id : Identifiant de l'article en stock associé.

status : État de l'élément de commande.

created_at : Horodatage indiquant quand l'élément de commande a été créé.

shipped_at : Horodatage indiquant quand l'élément de commande a été expédié.

delivered_at : Timestamp indicating when the order item was delivered.

returned_at : Horodatage indiquant quand l'élément de commande a été retourné.





### **- orders.csv**

Elle contient les informations sur chaque commande

order_id : Identifiant unique pour chaque commande.

user_id : Identifiant de l'utilisateur ayant passé la commande.

status : Statut de la commande.

gender : Informations sur le genre de l'utilisateur.

created_at : Horodatage indiquant quand la commande a été créée.

returned_at : Horodatage indiquant quand la commande a été retournée.

shipped_at : Horodatage indiquant quand la commande a été expédiée.

delivered_at : Horodatage indiquant quand la commande a été livrée.

num_of_item : Nombre d'articles dans la commande.





### **- products.csv**
  
contient les informations sur chaque produit

id : Identifiant unique pour chaque produit.

cost : Coût du produit.

category : Catégorie à laquelle le produit appartient.

name : Nom du produit.

brand : Marque du produit.

retail_price : Prix de détail du produit.

department : Département auquel le produit appartient.

sku : Unité de gestion des stocks (SKU) du produit.

distribution_center_id : Identifiant du centre de distribution associé au produit.




### **- users.csv**

contient les onformations sur les utilisateurs

id : Identifiant unique pour chaque utilisateur.

first_name : Prénom de l'utilisateur.

last_name : Nom de famille de l'utilisateur.

email : Adresse e-mail de l'utilisateur.

age : Âge de l'utilisateur.

gender : Genre de l'utilisateur.

state : Genre de l'utilisateur.

street_address : Adresse postale de l'utilisateur.

postal_code : Code postal de l'utilisateur.

city : Ville où se trouve l'utilisateur.

