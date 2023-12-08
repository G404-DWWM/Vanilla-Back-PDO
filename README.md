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
  <summary>Live coding</summary>
  
  ```php
  <?php
      require_once('connexion.php');

      // requete de mon user
      $request =  $db->query('SELECT * FROM user');
      $user = $request->fetch();

      var_dump($user);

      echo($user['prenom']);

      ?>

```


</details>

- **Connexion à une base de données MySQL avec PDO**
- **La préparation d'une requête**
- **La récupération de la réponse d’une requête**

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
