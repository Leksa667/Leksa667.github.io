<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Netari.fr - Site en Maintenance</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        :root {
            --primary-color: #007ACC;
            --secondary-color: #FDBC71;
            --dark-bg: #0A0A0F;
            --darker-bg: #050508;
            --card-bg: #141420;
            --text-color: #FFFFFF;
            --text-secondary: #A0A0B0;
            --gradient-primary: linear-gradient(135deg, #007ACC 0%, #FDBC71 100%);
            --border-radius: 12px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: var(--dark-bg);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            background: radial-gradient(ellipse at center, rgba(0, 122, 204, 0.15) 0%, transparent 50%),
                        radial-gradient(ellipse at bottom, rgba(253, 188, 113, 0.1) 0%, transparent 50%),
                        var(--dark-bg);
        }

        .maintenance-container {
            max-width: 600px;
            text-align: center;
            padding: 40px;
            background: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 0.6s ease;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .site-logo {
            max-width: 90px;
            width: 100%;
            height: auto;
            display: block;
            margin: 0 auto 30px;
            object-fit: contain;
        }

        .maintenance-icon {
            width: 120px;
            height: 120px;
            margin: 0 auto 30px;
            background: var(--gradient-primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
                box-shadow: 0 0 0 0 rgba(0, 122, 204, 0.7);
            }
            50% {
                transform: scale(1.05);
                box-shadow: 0 0 0 20px rgba(0, 122, 204, 0);
            }
        }

        .maintenance-icon svg {
            width: 60px;
            height: 60px;
            fill: white;
        }

        h1 {
            font-size: 2.5rem;
            font-weight: 600;
            margin-bottom: 20px;
            color: var(--text-color);
        }

        p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 30px;
            line-height: 1.7;
        }

        .status-message {
            background: rgba(0, 122, 204, 0.1);
            border-left: 4px solid var(--primary-color);
            padding: 15px 20px;
            margin: 30px 0;
            border-radius: 8px;
            text-align: left;
        }

        .status-message p {
            margin: 0;
            font-size: 0.95rem;
        }

        .loading-dots {
            display: flex;
            justify-content: center;
            gap: 8px;
            margin-top: 30px;
        }

        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--gradient-primary);
            animation: loading 1.4s ease-in-out infinite;
        }

        .dot:nth-child(2) {
            animation-delay: 0.2s;
        }

        .dot:nth-child(3) {
            animation-delay: 0.4s;
        }

        @keyframes loading {
            0%, 80%, 100% {
                transform: scale(0.8);
                opacity: 0.5;
            }
            40% {
                transform: scale(1.2);
                opacity: 1;
            }
        }

        .refresh-button {
            display: inline-block;
            padding: 12px 25px;
            background: var(--gradient-primary);
            color: white;
            text-decoration: none;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 30px;
        }

        .refresh-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 122, 204, 0.4);
        }

        .contact-info {
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .contact-info p {
            font-size: 0.9rem;
            margin-bottom: 10px;
        }

        .contact-link {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
        }

        .contact-link:hover {
            color: var(--secondary-color);
        }

        @media (max-width: 768px) {
            .maintenance-container {
                margin: 20px;
                padding: 30px 20px;
            }

            h1 {
                font-size: 2rem;
            }

            p {
                font-size: 1rem;
            }

            .maintenance-icon {
                width: 100px;
                height: 100px;
            }

            .maintenance-icon svg {
                width: 50px;
                height: 50px;
            }

            .site-logo {
                max-width: 70px;
            }

            .refresh-button {
                padding: 10px 20px;
                font-size: 0.9rem;
            }
        }

        @media (max-width: 480px) {
            .maintenance-container {
                margin: 10px;
                padding: 20px 15px;
            }

            h1 {
                font-size: 1.8rem;
            }

            p {
                font-size: 0.9rem;
            }

            .site-logo {
                max-width: 60px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <div class="maintenance-container">
        <img src="https://media.discordapp.net/attachments/1251174732271849476/1433496691205738676/logo.png"
             alt="Netari.fr Logo" class="site-logo">
        
        <div class="maintenance-icon">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                <path d="M22.7 19l-9.1-9.1c.9-2.3.4-5-1.5-6.9-2-2-5-2.4-7.4-1.3L9 6 6 9 1.6 4.7C.4 7.1.9 10.1 2.9 12.1c1.9 1.9 4.6 2.4 6.9 1.5l9.1 9.1c.4.4 1 .4 1.4 0l2.3-2.3c.5-.4.5-1.1.1-1.4z"/>
            </svg>
        </div>

        <h1>Site en Maintenance</h1>
        <p>Nous effectuons actuellement des mises à jour pour améliorer votre expérience. Je travaille activement pour remettre le site en ligne dans les meilleurs délais.</p>

        <div class="status-message">
            <p><strong>🔧 Travaux en cours :</strong> Optimisation des performances et mise à jour des fonctionnalités.</p>
        </div>

        <div class="loading-dots">
            <div class="dot"></div>
            <div class="dot"></div>
            <div class="dot"></div>
        </div>

        <button class="refresh-button" onclick="location.reload()">Actualiser la page</button>

        <div class="contact-info">
            <p>Pour toute urgence, vous pouvez me contacter :</p>
            <p><a href="mailto:contactnetari@proton.me" class="contact-link">contactnetari@proton.me</a></p>
        </div>
    </div>
</body>
</html>
