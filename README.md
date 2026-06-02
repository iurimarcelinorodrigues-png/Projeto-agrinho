<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agro Forte, Futuro Sustentável | Equilíbrio e Produção</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Variáveis de Cores e Estilo */
        :root {
            --primary: #1b4332;
            --primary-light: #2d6a4f;
            --accent: #52b788;
            --accent-light: #d8f3dc;
            --dark: #1a1a1a;
            --light: #f8f9fa;
            --gray: #6c757d;
            --transition: all 0.3s ease;
        }

        /* Reset e Configurações Gerais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            color: var(--primary);
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .section-subtitle {
            text-align: center;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto 3rem auto;
            font-size: 1.1rem;
        }

        /* Barra de Navegação Fina e Moderna */
        header {
            background-color: rgba(27, 67, 50, 0.95);
            backdrop-filter: blur(10px);
            color: #fff;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-weight: 700;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #fff;
            text-decoration: none;
        }

        .logo i {
            color: var(--accent);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-link {
            color: #e0e0e0;
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: var(--transition);
        }

        .nav-link:hover {
            color: var(--accent);
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section Premium */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.4)), 
                        url('https://images.unsplash.com/photo-1625246333195-78d9c38ad451?auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            height: 85vh;
            display: flex;
            align-items: center;
            color: #fff;
            text-align: left;
        }

        .hero-content {
            max-width: 800px;
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            color: #f0f0f0;
        }

        .btn-primary {
            display: inline-block;
            background-color: var(--accent);
            color: var(--primary);
            padding: 0.9rem 2rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(82, 183, 136, 0.3);
        }

        .btn-primary:hover {
            background-color: #fff;
            color: var(--primary);
            transform: translateY(-2px);
        }

        /* Seção de Estatísticas (Métricas de Impacto) */
        .stats-section {
            background-color: #fff;
            padding: 4rem 0;
            box-shadow: 0 -10px 30px rgba(0,0,0,0.02);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .stat-item h2 {
            font-size: 3rem;
            color: var(--primary-light);
            margin-bottom: 0.5rem;
        }

        .stat-item p {
            color: var(--gray);
            font-weight: 500;
        }

        /* Seção Sobre com Imagem Lateral */
        .about-section {
            padding: 6rem 0;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .about-text h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .about-text p {
            color: #444;
            margin-bottom: 1.5rem;
            font-size: 1.05rem;
        }

        /* Pilares Sustentáveis (Grid de Cards) */
        .pillars-section {
            background-color: var(--accent-light);
            padding: 6rem 0;
        }

        .pillars-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .pillar-card {
            background: #fff;
            padding: 2.5rem 2rem;
            border-radius: 12px;
            transition: var(--transition);
            border-bottom: 4px solid transparent;
        }

        .pillar-card:hover {
            transform: translateY(-10px);
            border-bottom-color: var(--primary-light);
            box-shadow: 0 15px 30px rgba(0,0,0,0.05);
        }

        .pillar-icon {
            font-size: 2.5rem;
            color: var(--primary-light);
            margin-bottom: 1.5rem;
        }

        .pillar-card h3 {
            margin-bottom: 1rem;
            color: var(--primary);
        }

        /* Seção FAQ Avançada (Acordeão) */
        .faq-section {
            padding: 6rem 0;
            background-color: #fff;
        }

        .faq-container {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            margin-bottom: 1rem;
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            overflow: hidden;
        }

        .faq-question {
            background-color: var(--light);
            padding: 1.2rem;
            width: 100%;
            text-align: left;
            border: none;
            outline: none;
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--primary);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: var(--transition);
        }

        .faq-question:hover {
            background-color: #f0f4f1;
        }

        .faq-answer {
            padding: 0 1.2rem;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out, padding 0.3s ease-out;
            background-color: #fff;
            color: #555;
        }

        /* Seção Contato Dupla (Infos + Formulário) */
        .contact-section {
            padding: 6rem 0;
            background-color: var(--light);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1.5fr;
            gap: 4rem;
        }

        .contact-info {
            background-color: var(--primary);
            color: #fff;
            padding: 3rem;
            border-radius: 12px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
        }

        .info-links {
            margin: 2rem 0;
        }

        .info-link-item {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 1.5rem;
            color: #e0e0e0;
        }

        .info-link-item i {
            color: var(--accent);
            font-size: 1.2rem;
        }

        .social-icons {
            display: flex;
            gap: 1rem;
        }

        .social-icons a {
            color: #fff;
            background: rgba(255,255,255,0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
            text-decoration: none;
        }

        .social-icons a:hover {
            background: var(--accent);
            color: var(--primary);
        }

        .contact-form {
            background: #fff;
            padding: 3rem;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.02);
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            font-size: 0.9rem;
            color: #444;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(82, 183, 136, 0.1);
        }

        .btn-submit {
            background-color: var(--primary-light);
            color: #fff;
            border: none;
            padding: 1rem 2rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 6px;
            cursor: pointer;
            width: 100%;
            transition: var(--transition);
        }

        .btn-submit:hover {
            background-color: var(--primary);
        }

        /* Rodapé Robusto */
        footer {
            background-color: #112a1f;
            color: #a0a0a0;
            padding: 4rem 0 2rem 0;
            font-size: 0.95rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-col h4 {
            color: #fff;
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.8rem;
        }

        .footer-col ul li a {
            color: #a0a0a0;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-col ul li a:hover {
            color: var(--accent);
        }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.05);
            padding-top: 2rem;
            text-align: center;
            font-size: 0.85rem;
        }

        /* Responsividade Extrema */
        @media (max-width: 992px) {
            .hero h1 { font-size
