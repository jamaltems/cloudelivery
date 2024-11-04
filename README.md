# cloudelivery
Cloudelivery - Service de livraison rapide et écologique, spécialisé dans le last mile pour les e-commerçants et les entreprises locales.
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cloudelivery - Livraison Last Mile Rapide et Écologique</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Styles globaux pour le site */
        body {
            font-family: Arial, sans-serif;
            color: #333;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }
        
        header {
            background-color: #ff69b4;
            color: white;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-size: 2.5em;
            margin: 0;
        }

        nav {
            margin-top: 20px;
        }

        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }

        section {
            max-width: 1000px;
            margin: 40px auto;
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        h2 {
            color: #ff69b4;
            margin-bottom: 10px;
            font-size: 1.8em;
            text-align: center;
        }

        .content p {
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .service-list, .review-list {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px 0;
        }

        .service-item, .review-item {
            flex: 1 1 30%;
            padding: 10px;
            text-align: center;
        }

        .btn {
            background-color: #ff69b4;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            display: inline-block;
            margin-top: 15px;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #e557a1;
        }

        /* Styles pour le formulaire de suivi et le calculateur de tarif */
        .form-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .form-container input {
            padding: 10px;
            width: 80%;
            max-width: 400px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ddd;
        }

        .result {
            font-size: 1.2em;
            color: #333;
            margin-top: 10px;
            text-align: center;
        }
    </style>
</head>
<body>

<header>
    <h1>Cloudelivery</h1>
    <nav>
        <a href="#services">Services</a>
        <a href="#pricing">Calculateur de Tarifs</a>
        <a href="#tracking">Suivi de Colis</a>
        <a href="#reviews">Avis Clients</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section id="services">
    <h2>Nos Services</h2>
    <div class="service-list">
        <div class="service-item">
            <h3>Livraison Express</h3>
            <p>Livraison en moins de 24 heures pour garantir la satisfaction de nos clients e-commerçants.</p>
        </div>
        <div class="service-item">
            <h3>Écologique</h3>
            <p>Flotte de véhicules électriques pour un impact carbone réduit.</p>
        </div>
        <div class="service-item">
            <h3>Suivi en Temps Réel</h3>
            <p>Suivez votre colis à tout moment grâce à notre technologie de tracking avancée.</p>
        </div>
    </div>
</section>

<section id="pricing">
    <h2>Calculateur de Tarifs</h2>
    <div class="form-container">
        <input type="text" id="origin" placeholder="Adresse de départ">
        <input type="text" id="destination" placeholder="Adresse de destination">
        <button class="btn" onclick="calculatePrice()">Calculer le Tarif</button>
        <div class="result" id="price-result">Entrez les adresses pour calculer le tarif</div>
    </div>
</section>

<section id="tracking">
    <h2>Suivi de Colis</h2>
    <div class="form-container">
        <input type="text" id="tracking-number" placeholder="Numéro de suivi">
        <button class="btn" onclick="trackPackage()">Suivre le Colis</button>
        <div class="result" id="tracking-result">Entrez votre numéro de suivi pour connaître l'état de votre colis</div>
    </div>
</section>

<section id="reviews">
    <h2>Avis Clients</h2>
    <div class="review-list">
        <div class="review-item">
            <p>"Service ultra rapide ! Mon colis est arrivé le jour même, je recommande vivement Cloudelivery !"</p>
            <p><strong>- Marie L.</strong></p>
        </div>
        <div class="review-item">
            <p>"Livraison écologique et professionnelle, merci à l'équipe pour leur efficacité."</p>
            <p><strong>- Paul B.</strong></p>
        </div>
        <div class="review-item">
            <p>"Le suivi en temps réel est génial, je pouvais voir exactement où était mon colis !"</p>
            <p><strong>- Sophie M.</strong></p>
        </div>
    </div>
</section>

<section id="contact">
    <h2>Contactez-nous</h2>
    <p>Pour toute demande de renseignement ou partenariat avec Cloudelivery, n'hésitez pas à nous contacter :</p>
    <p><strong>Téléphone :</strong> 07.49.46.40.56</p>
    <p><strong>Email :</strong> contact@cloudelivery.com</p>
    <p><strong>Adresse à Lyon :</strong> 83 quai Charles de Gaulle, 69006 Lyon</p>
    <p><strong>Adresse à Marseille :</strong> CASTORS DE SERVIERES, 3 ALLEE DU CENTAURE, 13015 MARSEILLE</p>
</section>

<script>
    // Fonction de calcul de tarif (simulation)
    function calculatePrice() {
        const origin = document.getElementById("origin").value;
        const destination = document.getElementById("destination").value;

        if (origin && destination) {
            document.getElementById("price-result").textContent = `Le tarif estimé entre ${origin} et ${destination} est de 15€.`; // Tarif simulé
        } else {
            document.getElementById("price-result").textContent = "Veuillez entrer les adresses de départ et de destination.";
        }
    }

    // Fonction de suivi de colis (simulation)
    function trackPackage() {
        const trackingNumber = document.getElementById("tracking-number").value;

        if (trackingNumber) {
            document.getElementById("tracking-result").textContent = `Le colis avec le numéro ${trackingNumber} est en transit.`;
        } else {
            document.getElementById("tracking-result").textContent = "Veuillez entrer un numéro de suivi valide.";
        }
    }
</script>

</body>
</html>
