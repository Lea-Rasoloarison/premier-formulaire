# premier-formulaire
premier-formulaire


<?php


?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <html lang="en-US">
    <link rel="stylesheet" href="style.css">
    <title>Premier Formulaire</title>
    </head>

<body>

<p>Formulaire 1</p>

<form  action=""  method="post">

    <label for="mailSubject">Choisissez un sujet:</label>

    <select name="mailSubject" id="mailSubject">
        <option value="">--Please choose an option--</option>
        <option value="Commentaire">Commentaire</option>
        <option value="Demande">Demande</option>
        <option value="Réclamation">Réclamation</option>
        <option value="Question">Question</option>
        <option value="Avis">Avis</option>
        <option value="Autres">Autres</option>
    </select>

    <br><br>

    <div>
        <label  for="nom">Nom :</label>
        <input  type="text"  id="nom"  name="nom">
    </div>
    <div>
        <label  for="courriel">Courriel :</label>
        <input  type="email"  id="courriel"  name="courriel">
    </div>
    <div>
        <label  for="message">Message :</label>
        <textarea  id="message"  name="message"></textarea>
    </div>
    <div>
        <label  for="phoneNumber">Numéro de téléphone :</label>
        <input id="phoneNumber" name="phoneNumber" type="number">
    </div>
    <div  class="button">
        <button  type="submit">Envoyer votre message</button>
    </div>
</form>


<p>
    "Merci <?php echo  $_POST['nom']; ?> de nous avoir contacté à propos de <?php echo  $_POST['mailSubject']; ?>.

    Un de nos conseiller vous contactera soit à l’adresse <?php echo  $_POST['courriel']; ?> ou par téléphone au <?php echo  $_POST['phoneNumber']; ?> dans les plus brefs délais pour traiter votre demande :

    <?php echo  $_POST['message']; ?>"

</p>

</body>
</html>
