<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>José Alejandro Silva Costa | Dados, Processos & Tecnologia</title>

    <meta name="description"
          content="Portfólio profissional de José Alejandro Silva Costa — Dados, Processos, Tecnologia, Power BI, Python, SQL e Automação.">

    <link rel="stylesheet"
          href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #080b10;
            color: #f5f7fa;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            width: min(1120px, 90%);
            margin: auto;
        }

        /* =========================
           NAVBAR
        ========================= */

        header {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(8, 11, 16, 0.90);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid #1c222b;
        }

        nav {
            height: 72px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 20px;
            font-weight: 700;
        }

        .logo span {
            color: #4f8cff;
        }

        .menu {
            display: flex;
            gap: 28px;
            list-style: none;
        }

        .menu a {
            color: #aeb7c4;
            font-size: 14px;
            transition: .3s;
        }

        .menu a:hover {
            color: #ffffff;
        }

        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 72px;
        }

        .hero-content {
            max-width: 850px;
        }

        .tag {
            display: inline-block;
            color: #4f8cff;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 18px;
            letter-spacing: .5px;
        }

        .hero h1 {
            font-size: clamp(42px, 7vw, 76px);
            line-height: 1.05;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #4f8cff;
        }

        .hero h2 {
            font-size: clamp(20px, 3vw, 30px);
            color: #c8d0db;
            font-weight: 500;
            margin-bottom: 22px;
        }

        .hero p {
            max-width: 720px;
            color: #8994a3;
            font-size: 18px;
            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 9px;
            padding: 13px 20px;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 600;
            transition: .3s;
        }

        .btn-primary {
            background: #4f8cff;
            color: white;
        }

        .btn-primary:hover {
            background: #3977e8;
            transform: translateY(-2px);
        }

        .btn-secondary {
            border: 1px solid #29313c;
            color: #d7dde5;
        }

        .btn-secondary:hover {
            border-color: #4f8cff;
            color: #4f8cff;
        }

        /* =========================
           SECTIONS
        ========================= */

        section {
            padding: 100px 0;
            border-top: 1px solid #151a21;
        }

        .section-title {
            margin-bottom: 50px;
        }

        .section-title small {
            color: #4f8cff;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            font-size: 12px;
        }

        .section-title h2 {
            font-size: 38px;
            margin-top: 8px;
        }

        .section-title p {
            color: #7f8a98;
            margin-top: 10px;
            max-width: 650px;
        }

        /* =========================
           SOBRE
        ========================= */

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .about-text p {
            color: #9ca6b4;
            margin-bottom: 18px;
        }

        .about-info {
            display: grid;
            gap: 15px;
        }

        .info-card {
            border: 1px solid #1d252f;
            background: #0c1118;
            padding: 20px;
            border-radius: 10px;
        }

        .info-card i {
            color: #4f8cff;
            margin-right: 10px;
        }

        .info-card span {
            color: #9ca6b4;
        }

        /* =========================
           TRAJETÓRIA
        ========================= */

        .timeline {
            position: relative;
            max-width: 850px;
        }

        .timeline::before {
            content: "";
            position: absolute;
            left: 7px;
            top: 0;
            width: 2px;
            height: 100%;
            background: #26303c;
        }

        .timeline-item {
            position: relative;
            padding-left: 35px;
            margin-bottom: 45px;
        }

        .timeline-item::before {
            content: "";
            position: absolute;
            left: 0;
            top: 6px;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background: #4f8cff;
            border: 3px solid #080b10;
            box-shadow: 0 0 0 2px #4f8cff;
        }

        .timeline-date {
            color: #4f8cff;
            font-size: 13px;
            font-weight: 700;
        }

        .timeline-item h3 {
            margin: 6px 0;
            font-size: 21px;
        }

        .timeline-item h4 {
            color: #8994a3;
            font-weight: 500;
            margin-bottom: 10px;
        }

        .timeline-item p {
            color: #8e99a7;
        }

        /* =========================
           PROJETOS
        ========================= */

        .projects {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 22px;
        }

        .project-card {
            background: #0c1118;
            border: 1px solid #1d252f;
            border-radius: 12px;
            padding: 28px;
            transition: .3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: #365f9f;
        }

        .project-icon {
            width: 45px;
            height: 45px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
            background: #111a28;
            color: #4f8cff;
            margin-bottom: 20px;
        }

        .project-card h3 {
            margin-bottom: 10px;
        }

        .project-card p {
            color: #8e99a7;
            font-size: 14px;
            margin-bottom: 18px;
        }

        .tags {
            display: flex;
            flex-wrap: wrap;
            gap: 7px;
            margin-bottom: 20px;
        }

        .tags span {
            background: #141b25;
            color: #aeb8c6;
            padding: 5px 9px;
            border-radius: 5px;
            font-size: 11px;
        }

        .project-link {
            color: #4f8cff;
            font-size: 14px;
            font-weight: 600;
        }

        /* =========================
           STACK
        ========================= */

        .stack-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px;
        }

        .stack-card {
            background: #0c1118;
            border: 1px solid #1d252f;
            border-radius: 10px;
            padding: 25px;
        }

        .stack-card h3 {
            font-size: 16px;
            margin-bottom: 15px;
            color: #e8edf3;
        }

        .stack-card ul {
            list-style: none;
        }

        .stack-card li {
            color: #8e99a7;
            padding: 6px 0;
            font-size: 14px;
        }

        .stack-card li::before {
            content: "•";
            color: #4f8cff;
            margin-right: 8px;
        }

        /* =========================
           FORMAÇÃO / CERTIFICAÇÕES
        ========================= */

        .education-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 22px;
        }

        .education-card {
            background: #0c1118;
            border: 1px solid #1d252f;
            padding: 28px;
            border-radius: 10px;
        }

        .education-card i {
            color: #4f8cff;
            font-size: 22px;
            margin-bottom: 18px;
        }

        .education-card h3 {
            margin-bottom: 6px;
        }

        .education-card p {
            color: #8e99a7;
            font-size: 14px;
        }

        /* =========================
           CONTATO
        ========================= */

        .contact-box {
            border: 1px solid #1d252f;
            background: #0c1118;
            border-radius: 12px;
            padding: 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
        }

        .contact-box h2 {
            margin-bottom: 10px;
        }

        .contact-box p {
            color: #8994a3;
        }

        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        /* =========================
           FOOTER
        ========================= */

        footer {
            padding: 35px 0;
            border-top: 1px solid #151a21;
            color: #65707e;
            font-size: 13px;
        }

        footer .container {
            display: flex;
            justify-content: space-between;
            gap: 20px;
        }

        /* =========================
           RESPONSIVO
        ========================= */

        @media (max-width: 900px) {

            .menu {
                display: none;
            }

            .about-grid,
            .education-grid {
                grid-template-columns: 1fr;
            }

            .projects {
                grid-template-columns: 1fr;
            }

            .stack-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .contact-box {
                flex-direction: column;
                align-items: flex-start;
            }
        }

        @media (max-width: 550px) {

            section {
                padding: 70px 0;
            }

            .hero h1 {
                font-size: 42px;
            }

            .stack-grid {
                grid-template-columns: 1fr;
            }

            footer .container {
                flex-direction: column;
            }
        }

    </style>
</head>

<body>

<header>

    <div class="container">

        <nav>

            <a href="#inicio" class="logo">
                Alejandro<span>.</span>
            </a>

            <ul class="menu">
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#trajetoria">Trajetória</a></li>
                <li><a href="#projetos">Projetos</a></li>
                <li><a href="#stack">Stack</a></li>
                <li><a href="#formacao">Formação</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>

        </nav>

    </div>

</header>


<main>

    <!-- =========================
         INÍCIO
    ========================== -->

    <section class="hero" id="inicio">

        <div class="container">

            <div class="hero-content">

                <span class="tag">
                    DADOS • PROCESSOS • TECNOLOGIA
                </span>

                <h1>
                    José Alejandro<br>
                    Silva <span>Costa</span>
                </h1>

                <h2>
                    Analista de Dados | Processos | Tecnologia
                </h2>

                <p>
                    Profissional com experiência em análise de processos,
                    organização de informações e apoio à gestão, construindo
                    uma trajetória direcionada para dados, tecnologia,
                    automação e inteligência de negócios.
                </p>

                <div class="buttons">

                    <!-- COLOQUE SEU PDF NA PASTA /cv -->
                    <a href="cv/jose-alejandro-cv.pdf"
                       class="btn btn-primary"
                       download>

                        <i class="fa-solid fa-download"></i>
                        Baixar currículo

                    </a>

                    <a href="#projetos"
                       class="btn btn-secondary">

                        Ver projetos
                        <i class="fa-solid fa-arrow-down"></i>

                    </a>

                    <a href="https://www.linkedin.com"
                       target="_blank"
                       class="btn btn-secondary">

                        <i class="fa-brands fa-linkedin"></i>
                        LinkedIn

                    </a>

                    <a href="https://github.com/alejandrocosta1"
                       target="_blank"
                       class="btn btn-secondary">

                        <i class="fa-brands fa-github"></i>
                        GitHub

                    </a>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         SOBRE
    ========================== -->

    <section id="sobre">

        <div class="container">

            <div class="section-title">

                <small>Sobre mim</small>

                <h2>Dados, processos e tecnologia.</h2>

                <p>
                    Uma trajetória construída entre gestão, processos
                    e tecnologia.
                </p>

            </div>


            <div class="about-grid">

                <div class="about-text">

                    <p>
                        Minha experiência profissional foi construída
                        principalmente na área de apoio à gestão e análise
                        de processos, desenvolvendo uma visão prática sobre
                        organização, controle e tomada de decisão.
                    </p>

                    <p>
                        Atualmente direciono minha carreira para Dados e
                        Tecnologia, utilizando ferramentas como Power BI,
                        Excel, SQL e Python para transformar informações
                        em análises e soluções.
                    </p>

                    <p>
                        Também tenho interesse em automação, melhoria de
                        processos, requisitos e produtos digitais.
                    </p>

                </div>


                <div class="about-info">

                    <div class="info-card">
                        <i class="fa-solid fa-location-dot"></i>
                        <span>Fortaleza, Ceará — Brasil</span>
                    </div>

                    <div class="info-card">
                        <i class="fa-solid fa-envelope"></i>
                        <span>SEUEMAIL@gmail.com</span>
                    </div>

                    <div class="info-card">
                        <i class="fa-solid fa-graduation-cap"></i>
                        <span>Análise e Desenvolvimento de Sistemas</span>
                    </div>

                    <div class="info-card">
                        <i class="fa-solid fa-chart-line"></i>
                        <span>Foco: Dados, BI e Processos</span>
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         TRAJETÓRIA
    ========================== -->

    <section id="trajetoria">

        <div class="container">

            <div class="section-title">

                <small>Experiência</small>

                <h2>Minha trajetória</h2>

                <p>
                    Experiências que contribuíram para minha evolução
                    profissional e direcionamento para tecnologia.
                </p>

            </div>


            <div class="timeline">

                <div class="timeline-item">

                    <span class="timeline-date">
                        ATUALMENTE
                    </span>

                    <h3>
                        Assistente de Apoio à Gestão
                    </h3>

                    <h4>
                        Tribunal de Contas do Estado do Ceará — TCE-CE
                    </h4>

                    <p>
                        Atuação com análise e acompanhamento de processos,
                        organização de informações, apoio à gestão,
                        manipulação de dados, elaboração de indicadores
                        e iniciativas de melhoria e automação.
                    </p>

                </div>


                <div class="timeline-item">

                    <span class="timeline-date">
                        FORMAÇÃO
                    </span>

                    <h3>
                        Análise e Desenvolvimento de Sistemas
                    </h3>

                    <h4>
                        Graduação
                    </h4>

                    <p>
                        Formação voltada para desenvolvimento de sistemas,
                        banco de dados, programação, análise de sistemas
                        e tecnologia.
                    </p>

                </div>


                <div class="timeline-item">

                    <span class="timeline-date">
                        PRÓXIMO PASSO
                    </span>

                    <h3>
                        Dados + Processos + Tecnologia
                    </h3>

                    <h4>
                        Direcionamento profissional
                    </h4>

                    <p>
                        Construção de portfólio e desenvolvimento de
                        projetos envolvendo análise de dados, BI,
                        automação e melhoria de processos.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         PROJETOS
    ========================== -->

    <section id="projetos">

        <div class="container">

            <div class="section-title">

                <small>Portfólio</small>

                <h2>Projetos</h2>

                <p>
                    Projetos práticos envolvendo dados, processos,
                    automação e tecnologia.
                </p>

            </div>


            <div class="projects">


                <article class="project-card">

                    <div class="project-icon">
                        <i class="fa-solid fa-chart-column"></i>
                    </div>

                    <h3>
                        Dashboard de Indicadores
                    </h3>

                    <p>
                        Desenvolvimento de dashboard para acompanhamento
                        e apresentação de indicadores do setor.
                    </p>

                    <div class="tags">

                        <span>Power BI</span>
                        <span>Excel</span>
                        <span>Dados</span>

                    </div>

                    <a href="#"
                       class="project-link">

                        Ver projeto →
                    </a>

                </article>


                <article class="project-card">

                    <div class="project-icon">
                        <i class="fa-brands fa-whatsapp"></i>
                    </div>

                    <h3>
                        Comunicação via WhatsApp
                    </h3>

                    <p>
                        Projeto voltado à melhoria do processo de envio
                        de comunicações utilizando tecnologia e automação.
                    </p>

                    <div class="tags">

                        <span>Automação</span>
                        <span>Processos</span>
                        <span>Tecnologia</span>

                    </div>

                    <a href="#"
                       class="project-link">

                        Ver projeto →
                    </a>

                </article>


                <article class="project-card">

                    <div class="project-icon">
                        <i class="fa-brands fa-python"></i>
                    </div>

                    <h3>
                        Análise de Dados com Python
                    </h3>

                    <p>
                        Projeto de análise exploratória e tratamento
                        de dados utilizando Python.
                    </p>

                    <div class="tags">

                        <span>Python</span>
                        <span>Pandas</span>
                        <span>Data Analysis</span>

                    </div>

                    <a href="#"
                       class="project-link">

                        GitHub →
                    </a>

                </article>


                <article class="project-card">

                    <div class="project-icon">
                        <i class="fa-solid fa-database"></i>
                    </div>

                    <h3>
                        Modelagem de Dados
                    </h3>

                    <p>
                        Projeto de estruturação e modelagem de dados
                        para apoiar análises e indicadores.
                    </p>

                    <div class="tags">

                        <span>SQL</span>
                        <span>Banco de Dados</span>
                        <span>Modelagem</span>

                    </div>

                    <a href="#"
                       class="project-link">

                        Ver projeto →
                    </a>

                </article>


            </div>

        </div>

    </section>


    <!-- =========================
         STACK
    ========================== -->

    <section id="stack">

        <div class="container">

            <div class="section-title">

                <small>Conhecimentos</small>

                <h2>Stack técnica</h2>

                <p>
                    Ferramentas e tecnologias utilizadas nos meus
                    estudos e projetos.
                </p>

            </div>


            <div class="stack-grid">


                <div class="stack-card">

                    <h3>Dados & BI</h3>

                    <ul>
                        <li>Power BI</li>
                        <li>Excel</li>
                        <li>SQL</li>
                        <li>Python</li>
                    </ul>

                </div>


                <div class="stack-card">

                    <h3>Programação</h3>

                    <ul>
                        <li>Python</li>
                        <li>HTML</li>
                        <li>CSS</li>
                        <li>JavaScript</li>
                    </ul>

                </div>


                <div class="stack-card">

                    <h3>Processos & Automação</h3>

                    <ul>
                        <li>Power Automate</li>
                        <li>Análise de Processos</li>
                        <li>Automação</li>
                        <li>Requisitos</li>
                    </ul>

                </div>


                <div class="stack-card">

                    <h3>Gestão</h3>

                    <ul>
                        <li>Scrum</li>
                        <li>Kanban</li>
                        <li>Product</li>
                        <li>Gestão de Processos</li>
                    </ul>

                </div>


            </div>

        </div>

    </section>


    <!-- =========================
         FORMAÇÃO
    ========================== -->

    <section id="formacao">

        <div class="container">

            <div class="section-title">

                <small>Formação</small>

                <h2>Formação & Certificações</h2>

            </div>


            <div class="education-grid">


                <div class="education-card">

                    <i class="fa-solid fa-graduation-cap"></i>

                    <h3>
                        Análise e Desenvolvimento de Sistemas
                    </h3>

                    <p>
                        Graduação em andamento
                    </p>

                    <p>
                        Instituição: [NOME DA INSTITUIÇÃO]
                    </p>

                </div>


                <div class="education-card">

                    <i class="fa-solid fa-certificate"></i>

                    <h3>
                        Fundamentos de Data Science e IA
                    </h3>

                    <p>
                        Data Science Academy
                    </p>

                    <p>
                        Certificação em fundamentos de Ciência
                        de Dados e Inteligência Artificial.
                    </p>

                </div>


                <div class="education-card">

                    <i class="fa-solid fa-certificate"></i>

                    <h3>
                        Python
                    </h3>

                    <p>
                        Curso / Formação complementar
                    </p>

                    <p>
                        [ADICIONE A INSTITUIÇÃO E CARGA HORÁRIA]
                    </p>

                </div>


                <div class="education-card">

                    <i class="fa-solid fa-certificate"></i>

                    <h3>
                        Power BI
                    </h3>

                    <p>
                        Curso / Formação complementar
                    </p>

                    <p>
                        [ADICIONE A INSTITUIÇÃO E CARGA HORÁRIA]
                    </p>

                </div>


            </div>

        </div>

    </section>


    <!-- =========================
         CONTATO
    ========================== -->

    <section id="contato">

        <div class="container">

            <div class="section-title">

                <small>Contato</small>

                <h2>Vamos conversar?</h2>

                <p>
                    Estou aberto a oportunidades, projetos e conexões
                    profissionais nas áreas de Dados, Tecnologia e Processos.
                </p>

            </div>


            <div class="contact-box">

                <div>

                    <h2>
                        José Alejandro Silva Costa
                    </h2>

                    <p>
                        Fortaleza, Ceará — Brasil
                    </p>

                    <p>
                        SEUEMAIL@gmail.com
                    </p>

                </div>


                <div class="contact-links">

                    <a href="mailto:SEUEMAIL@gmail.com"
                       class="btn btn-primary">

                        <i class="fa-solid fa-envelope"></i>
                        Enviar e-mail

                    </a>

                    <a href="https://www.linkedin.com"
                       target="_blank"
                       class="btn btn-secondary">

                        <i class="fa-brands fa-linkedin"></i>
                        LinkedIn

                    </a>

                    <a href="https://github.com/alejandrocosta1"
                       target="_blank"
                       class="btn btn-secondary">

                        <i class="fa-brands fa-github"></i>
                        GitHub

                    </a>

                </div>

            </div>

        </div>

    </section>

</main>


<footer>

    <div class="container">

        <span>
            © 2026 José Alejandro Silva Costa
        </span>

        <span>
            Dados • Processos • Tecnologia
        </span>

    </div>

</footer>


</body>
</html>
