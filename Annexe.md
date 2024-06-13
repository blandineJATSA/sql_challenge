Ce document contient les définitions et informations détaillées sur l’analyse des données du site E-commerce TheLook.

**Les Différentes Pages d'un Site E-commerce**

- Home Page - La page d'accueil du site.

- Product Page - La page d'un produit spécifique.

- Category Page - La page listant les produits d'une catégorie spécifique.

- Search Results Page - La page affichant les résultats de la recherche.

- Cart Page - La page du panier d'achat.

- Checkout Page - La page de validation de commande.

- Order Confirmation Page - La page de confirmation de commande.

- User Account Page - La page du compte utilisateur.

- Login Page - La page de connexion.

- Sign Up Page - La page d'inscription.


**Les événements associés aux pages**

- Page View - Quand un utilisateur visite une page .

- Product View - Quand un utilisateur visualise un produit .

- Add to Cart - Quand un utilisateur ajoute un produit au panier .

- Remove from Cart - Quand un utilisateur retire un produit du panier .

- Begin Checkout - Quand un utilisateur commence le processus de paiement .

- Complete Purchase - Quand un utilisateur finalise l'achat.

- Login - Quand un utilisateur se connecte .

- Sign Up - Quand un utilisateur crée un compte.

- Search - Quand un utilisateur effectue une recherche .

- Click - Quand un utilisateur clique sur un lien ou un bouton.



👍**La colonne event_type de la table events**


la colonne event_type specifie le type d’événement que nous avons dans notre site E-commerce.

- home  :  Cet événement se produit lorsque l'utilisateur visite la page d'accueil du site.

- department  : L'utilisateur visite une page de catégorie ou de département ("Vêtements", "Électronique", etc)

- product  : L'utilisateur consulte un produit spécifique, par exemple, une chemise.

- cart : L'utilisateur ajoute la chemise à son panier.

- purchase : L'utilisateur procède à l'achat de la chemise.

- cancel : L'utilisateur annule la commande avant ou après le paiement.

- earmitts : Pas connue 

- madison : Pas connue



**Les différentes sources de trafic :** 

- Sources de Trafic : Les canaux par lesquels les utilisateurs arrivent sur TheLook. Ces sources peuvent inclure :

- Recherche organique : Utilisateurs venant des moteurs de recherche.

- Trafic direct : Utilisateurs qui tapent directement l'URL du site.

- Réseaux sociaux : Utilisateurs venant des plateformes sociales.

- Référencement : Utilisateurs venant d'autres sites web.

- Publicité payante : Utilisateurs venant de campagnes publicitaires payantes.


👍 **La colonne traffic_source**

Email,

Adwords

Youtube

Facebook

Organic

Concernant les Publicités payantes, nous  avons les paramètres UTM(Urchin Tracking Module) utilisés dans les URL pour aider à suivre l'efficacité des campagnes marketing et à identifier les sources de trafic vers un site web.
Les paramètres UTM sont ajoutés aux liens de campagnes et permettent d'obtenir des données détaillées sur les visiteurs et leurs interactions avec le contenu.

**Paramètres UTM Principaux**

Les paramètres UTM courants incluent :

- utm_source : Identifie la source de la campagne (par exemple, Google, Facebook, newsletter).

- utm_medium : Indique le moyen ou le type de marketing (par exemple, email, CPC, social).

- utm_campaign : Spécifie le nom de la campagne marketing (par exemple, summer_sale, black_friday).

- utm_term : Utilisé pour les mots-clés payants (souvent utilisé dans les campagnes PPC).

- utm_content : Différencie le contenu ou les versions des publicités au sein de la même campagne (par exemple, différentes versions d'une bannière, un appel à l'action différent).


EXemple d’url avec tout les paramètres UTM.
https://www.thelook.com/product/123?utm_source=google&utm_medium=cpc&utm_campaign=spring_sale&utm_term=red_dress&utm_content=text_ad

👍 **Les sessions**

Les sessions ne proviennent pas des UTM, mais des Cookies. 

Les cookies sont de petits fichiers de texte stockés sur le disque dur d'un utilisateur par un site web. 

Ils sont utilisés notamment pour suivre les sessions des utilisateurs, stocker des informations de préférence, et personnaliser l'expérience utilisateur sur un site web.

**Types de Cookies**

**Cookies de Session :**

**Description :** Ces cookies sont temporaires et sont effacés lorsque l'utilisateur ferme son navigateur.

**Utilisation :** Suivre les actions d'un utilisateur pendant une session de navigation (par exemple, garder les articles dans un panier d'achat).


👍 **BROWSER ( navigateur web)**

C’est un logiciel permettant d'accéder à des pages web sur Internet.

Exemples de navigateurs web :

Firefox

IE

Chrome

Safari

Others (Edge, opera,etc)


**Table orders**

La table des commandes est vraiment importante pour toute entreprise de commerce électronique. C'est là que les événements de revenus sont suivis.

👍 **La colonne status**

 - Status fait souvent référence à l'état actuel d'une commande. 

- Shipped  : La commande a été expédiée et est en transit vers le client.

- Processing :  La commande est en cours de traitement

- Cancelled : La commande a été annulée

- Complete : La commande a été terminée avec succès

- Returned : La commande ou une partie de celle-ci a été retournée par le client


**ANALYSE DE SOURCE DE TRAFFIC  ( tables events et orders)**


L'analyse des sources de trafic consiste à comprendre d'où viennent vos clients et quels sont les canaux qui génèrent le trafic de la plus haute qualité.


**QUESTION 1 :**  D’où proviennent la majorité des sessions de site web ? Comment elles sont reparties par source de trafic, par type de campagne, par source de navigateur, par type de contenu  ?


**QUESTION 2 :** TAUX DE CONVERSIONS DE SESSIONS EN COMMANDES


D’après les résultats de la première question, les campagnes emailing et les annonces googles adwords sont les deux sources de traffic les plus importantes. 

Nous souhaitons creuser profondément ces campagnes et essayer de comprendre les taux de conversion des sessions en commandes. En d'autres termes, il s'agit de déterminer quel pourcentage des sessions se convertissent en vente pour l'entreprise.


**CVR  (Conversion Rate) signifie taux de conversion :**  C'est une métrique utilisée pour mesurer l'efficacité d'une campagne ou d'un site web en termes de conversions

**CVR :** Le pourcentage de visiteurs d'un site web ou d'une campagne marketing qui effectuent une action souhaitée, comme un achat, une inscription, ou une demande de devis.

Formule

**CVR = (Nombre de conversions / Nombre total de visiteurs) * 100**

Importance

- Évaluer l'efficacité : Mesure l'efficacité des campagnes marketing ou des modifications sur le site.

- Optimisation : Aide à identifier les points faibles du parcours client pour améliorer le taux de conversion.

- ROI : Contribue à calculer le retour sur investissement des efforts marketing.
