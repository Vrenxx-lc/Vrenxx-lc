<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Perfil interativo</title>
    <!-- Fontes do Google -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
    <!-- Ícones (FontAwesome) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: rgba(30, 41, 59, 0.7);
            --primary: #38bdf8;
            --text-main: #f1f5f9;
            --text-sec: #94a3b8;
            --accent: #818cf8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            display: flex;
            justify-content: center;
            min-height: 100vh;
            padding: 20px;
            background-image: 
                radial-gradient(at 0% 0%, rgba(56, 189, 248, 0.15) 0px, transparent 50%),
                radial-gradient(at 100% 100%, rgba(129, 140, 248, 0.15) 0px, transparent 50%);
        }

        .container {
            width: 100%;
            max-width: 700px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* --- Header / Perfil --- */
        .profile-card {
            background: var(--card-bg);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 24px;
            padding: 40px;
            text-align: center;
            box-shadow: 0 10px 30px -10px rgba(0,0,0,0.5);
            animation: slideDown 0.8s ease-out;
        }

        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 3px solid var(--primary);
            object-fit: cover;
            margin-bottom: 15px;
            box-shadow: 0 0 20px rgba(56, 189, 248, 0.4);
            transition: transform 0.3s ease;
        }

        .avatar:hover {
            transform: scale(1.05) rotate(3deg);
        }

        h1 {
            font-size: 2rem;
            font-weight: 800;
            margin-bottom: 5px;
        }

        .typing-text {
            color: var(--primary);
            font-weight: 600;
            font-size: 1.1rem;
            min-height: 1.5rem;
            display: inline-block;
            border-right: 2px solid var(--primary);
            padding-right: 5px;
            animation: blink 0.7s infinite;
        }

        .bio {
            color: var(--text-sec);
            margin-top: 15px;
            line-height: 1.6;
            font-size: 0.95rem;
        }

        /* --- Botões Sociais --- */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 25px;
            flex-wrap: wrap;
        }

        .btn {
            text-decoration: none;
            padding: 12px 24px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            border: none;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: #fff;
        }

        .btn-outline {
            background: transparent;
            border: 1px solid var(--text-sec);
            color: var(--text-main);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px -5px rgba(0,0,0,0.3);
        }
        
        .btn:active {
            transform: scale(0.95);
        }

        /* --- Grid de Estatísticas --- */
        .stats-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            animation: fadeIn 1s ease-in 0.3s backwards;
        }

        .stat-card {
            background: var(--card-bg);
            border: 1px solid rgba(255,255,255,0.05);
            border-radius: 16px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            transition: transform 0.3s;
        }

        .stat-card:hover {
            transform: translateY(-5px);
            border-color: var(--
