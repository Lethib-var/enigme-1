<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jeu de Piste</title>
    <style>
        body {
            background-color: transparent; /* Fond transparent */
            color: black; /* Texte noir pour tout le corps */
            font-family: Arial, sans-serif; /* Police par défaut */
            display: flex;
            justify-content: center; /* Centrer le contenu horizontalement */
            align-items: center; /* Centrer le contenu verticalement */
            height: 100vh; /* Prendre toute la hauteur de l'écran */
            margin: 0; /* Supprimer les marges */
        }

        .conteneur {
            width: 300px; /* Largeur faible de la boîte contenant le jeu */
            padding: 20px; /* Un peu d'espace autour du contenu */
            background-color: rgba(255, 255, 255, 0.8); /* Fond léger et transparent */
            border-radius: 10px; /* Coins arrondis */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Ombre légère */
            text-align: center; /* Centrer le texte */
        }

        input[type="text"] {
            width: 100%; /* Prendre toute la largeur de l'input */
            padding: 10px; /* Un peu de marge interne pour l'input */
            margin-bottom: 10px; /* Marge sous l'input */
            border: 1px solid #ccc; /* Bordure de l'input */
            border-radius: 5px; /* Coins arrondis */
            font-size: 16px; /* Taille de la police */
        }

        button {
            padding: 10px 20px;
            background-color: #4CAF50; /* Couleur du bouton */
            color: white; /* Texte du bouton en blanc */
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #45a049; /* Changer la couleur du bouton au survol */
        }

        #message {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="conteneur">
        <h2>Jeu de Piste</h2>
        <input type="text" id="motMystere" placeholder="Entrez le mot mystère" />
        <button onclick="verifierMot()">Vérifier</button>
        <p id="message"></p>
    </div>

    <script>
        const motCorrect = "arcgis"; // Remplace par ton mot mystère

        function verifierMot() {
            let motEntre = document.getElementById("motMystere").value.trim().toLowerCase();
            let message = document.getElementById("message");

            if (motEntre === motCorrect) {
                message.innerHTML = "🎉 Bravo ! Vous avez trouvé le bon mot mystère !";
                message.style.color = "green"; /* Texte en vert pour succès */
            } else {
                message.innerHTML = "❌ Oups, ce n'est pas le bon mot. Essayez encore !";
                message.style.color = "red"; /* Texte en rouge pour erreur */
            }
        }
    </script>
</body>
</html>
