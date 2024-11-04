<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cloudelivery - Service de Livraison</title>
    <!-- Importer Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <!-- Importer Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* Styles globaux */
        body {
            font-family: 'Poppins', sans-serif;
            color: #333;
            background-color: #f9f9f9;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #ff69b4;
            color: white;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-weight: 600;
        }

        nav a {
            color: white;
            font-weight: 500;
        }

        .hero {
            background-color: #ffe3f1;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            margin-top: 20px;
        }

        .btn-custom {
            background-color: #ff69b4;
            color: white;
            font-weight: 500;
            border-radius: 5px;
        }

        .service-item {
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            background-color: white;
        }

        footer {
            background-color: #333;
            color: white;
            padding: 10px;
            text-align: center;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <h1>Cloudelivery</h1>
        <nav class="navbar navbar-expand-lg navbar-dark">
            <div class="container">
                <a class="navbar-brand" href="#">Accueil</a>
                <a class="navbar-brand" href="#services">Services</a>
                <a class="navbar-brand" href="#about">À propos</a>
                <a class="navbar-brand" href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="container">
        <div class="hero text-center">
            <h2 class="display-4 font-weight-bold">Votre solution de livraison rapide et fiable</h2>
            <p class="lead">Nous livrons vos colis dans les meilleurs délais en respectant vos exigences.</p>
            <a href="#services" class="btn btn-custom btn-lg mt-3">Découvrir nos services</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="container mt-5">
        <h2 class="text-center text-uppercase font-weight-bold mb-4">Nos Services</h2>
        <div class="row">
            <div class="col-md-4 service-item">
                <h3 class="h5 font-weight-bold">Livraison express</h3>
                <p>Livraison rapide en moins de 24 heures pour les clients professionnels et particuliers.</p>
            </div>
            <div class="col-md-4 service-item">
                <h3 class="h5 font-weight-bold">Livraison de colis volumineux</h3>
                <p>Nous prenons en charge les colis de toutes tailles, avec des solutions adaptées.</p>
            </div>
            <div class="col-md-4 service-item">
                <h3 class="h5 font-weight-bold">Suivi de livraison</h3>
                <p>Suivez votre colis en temps réel grâce à notre système de tracking.</p>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="container mt-5">
        <h2 class="text-center text-uppercase font-weight-bold mb-4">À propos de nous</h2>
        <p class="text-center">Cloudelivery est une société de livraison dédiée à fournir un service rapide, fiable et de haute qualité. Nous opérons avec une flotte de véhicules écologiques pour réduire notre impact environnemental.</p>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="container mt-5">
        <h2 class="text-center text-uppercase font-weight-bold mb-4">Contactez-nous</h2>
        <form id="contactForm" class="mx-auto" style="max-width: 600px;">
            <div class="form-group">
                <label for="name">Nom :</label>
                <input type="text" class="form-control" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email :</label>
                <input type="email" class="form-control" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="message">Message :</label>
                <textarea class="form-control" id="message" name="message" required></textarea>
            </div>
            <button type="submit" class="btn btn-custom btn-block">Envoyer</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Cloudelivery. Tous droits réservés.</p>
    </footer>

    <!-- JavaScript Bootstrap et Formulaire -->
    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.bundle.min.js"></script>
    <script>
        // Exemple de script pour gérer la soumission du formulaire de contact
        document.getElementById("contactForm").addEventListener("submit", function(event) {
            event.preventDefault();
            alert("Merci pour votre message ! Nous vous contacterons bientôt.");
        });
    </script>
</body>
</html>

