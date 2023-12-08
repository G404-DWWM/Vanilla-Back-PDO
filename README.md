# Vanilla-Back-PDO

# 💾 PDO Connexion BDD

<img src="schema.png"
     alt="schema-pdo"/>

# Différences entre PDO, MySQL, PhpMyadmin

**MySQL** et **MariaDB** sont deux systèmes de base de données relationnelle concurrents.

MariaDB a été conçu par des anciens fondateurs de MySQL,[ pour diverses raisons](https://subscription.packtpub.com/book/application_development/9781783981601/1/ch01lvl1sec08/mariadb-history).

Ce sont donc des **serveurs** de base de données, qui ouvrent leurs portes pour que d'autres logiciels puissent envoyer des requêtes et recevoir des données en retour.

PhpMyAdmin, HeidiSQL, MySQL CLI, et bien d'autres logiciels du genre ont tous le point commun d'être des **clients** permettant d'envoyer au serveur des requêtes SQL.

Sans **client**, il n'est pas possible d'interroger un serveur SQL.

PDO part du même principe mais au lieu de pouvoir être utilisé via une interface graphique, c'est sous forme de code PHP que l'on acquiert la possibilité de faire des requêtes.

# 🎦 Live coding

<details>
  <summary>Le fichier connexion.php</summary>
  
  ```php
  <?php
     try
     {
          $db = new PDO('mysql:host=localhost;dbname=pdo_test;charset=utf8', 'root', '');
     }
     catch (Exception $e)
     {
          die('Erreur : ' . $e->getMessage());
     }

     ?>

```
</details>

<details>
  <summary>Récupération d'un User en Base de Donnée</summary>

  ```php
  <?php
     // dans un nouveau fichier que l'on peut nommer index.php
     // ne pas oublier d'importer le fichier connexion.php où l'on créer la connexion PDO
      require_once('connexion.php');

      // requete de mon user :

      // on commence par préparer la requète grace à query()
      $request =  $db->query('SELECT * FROM user');

      // on récupère la réponse à la requète grâce à fetch(), car je n'ai qu'un seul user en BDD
      $user = $request->fetch();

      var_dump($user);

      echo($user['prenom']);

     ?>

```
</details>

<details>
  <summary>Récupération de plusieurs product en Base de Donnée</summary>

  ```php
  <?php
     // requete de mes produits

     // on prépare la requète
     $request = $db->query('SELECT * FROM product');

     // on récupère la réponse à la requète grâce à fetchAll(), car j'ai plusieurs produits en BDD
     $products = $request->fetchAll();

     var_dump($products);

     foreach($products as $product){
          echo($product['name']. '<br><hr><br>');
     }

     ?>

```
</details>


# 📖 Le cours de référence

Voici les 2 chapitres OpenClassroom qui regroupent l'ensemble de la théorie sur la requête PDO, la préparation de requête et l'exécution des requêtes

- [Lire des données MySQL avec PHP](https://openclassrooms.com/en/courses/918836-concevez-votre-site-web-avec-php-et-mysql/914293-lisez-des-donnees)
- [Ecrire des données SQL avec PHP](https://openclassrooms.com/en/courses/918836-concevez-votre-site-web-avec-php-et-mysql/914508-ecrivez-des-donnees)
- la doc PDO →[ PHP: PDO - Manual](https://www.php.net/manual/fr/book.pdo.php)

# ⛳ Exercices 1

##

**Pour faire ces exercices, vous devez utiliser le code SQL qui vous est fourni pour créer la BDD.**

Utilisation de PDO pour récupérer, lire et afficher des données

- [simplon-roanne/Exercice-PDO-1](https://github.com/simplon-roanne/Exercice-PDO-1)

# ⛳ Exercices 2

##

**Pour faire ces exercices, vous devez utiliser le code SQL qui vous est fourni pour créer la BDD.**

Ecriture et lecture de données ( Hospital ) :

- [simplon-roanne/Exercice-PDO-2](https://github.com/simplon-roanne/Exercice-PDO-2)

# 🏆 Objectifs

- Je sais connecter mon site avec ma base de données (BDD)
- Je sais récupérer et lire les données de ma BDD
- Je sais écrire et insérer des données dans ma BDD

```

```
