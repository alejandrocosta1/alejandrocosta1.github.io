<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>José Alejandro | Dados, Processos & Tecnologia</title>
    <meta name="description" content="Portfólio profissional de José Alejandro Silva Costa — Dados, Processos e Tecnologia.">
    
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
            background: #0b1120;
            color: #f8fafc;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        .container {
            width: min(1100px, 90%);
            margin: auto;
        }

        /* NAVBAR */
        nav {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(11, 17, 32, 0.92);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid #1e293b;
        }

        .nav-content {
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 22px;
            font-weight: 800;
        }

        .logo span {
            color: #38bdf8;
        }

        .nav-links {
            display: flex;
            gap: 25px;
            list-style: none;
            font-size: 14px;
            color: #cbd5e1;
        }

        .nav-links a:hover {
            color: #38bdf8;
        }

        /* HERO */
        .hero {
            min-height: 88vh;
            display: flex;
            align-items: center;
            background: radial-gradient(circle at 80% 20%, #123456 0, transparent 35%), #0b1120;
        }

        .hero-content {
            max-width: 850px;
        }

        .tag {
            display: inline-block;
            color: #38bdf8;
            border: 1px solid #164e63;
            background: #082f49;
            padding: 7px 14px;
            border-radius: 30px;
            font-size: 13px;
            font-weight: bold;
            margin-bottom: 25px;
        }

        .hero h1 {
            font-size: clamp(45px, 8vw, 78px);
            line-height: 1.02;
            letter-spacing: -3px;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: #38bdf8;
        }

        .hero h2 {
            font-size: 24px;
            color: #cbd5e1;
            font-weight: 500;
            margin-bottom: 20px;
        }

        .hero p {
            max-width: 700px;
            color: #94a3b8;
            font-size: 18px;
            margin-bottom: 32px;
        }

        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .button {
            padding: 13px 20px;
            border-radius: 9px;
            font-weight: bold;
            font-size: 14px;
            transition: .2s;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .button-primary {
            background: #38bdf8;
            color: #082f49;
        }

        .button-primary:hover {
            transform: translateY(-2px);
            background: #7dd3fc;
        }

        .button-secondary {
            border: 1px solid #334155;
            color: #e2e8f0;
            background: rgba(15, 23, 42, 0.6);
        }

        .button-secondary:hover {
            border-color: #38bdf8;
            color: #38bdf8;
            background: rgba(56, 189, 248, 0.05);
        }

        /* SECTIONS */
        section {
            padding: 90px 0;
        }

        .section-title {
            font-size: 38px;
            margin-bottom: 10px;
        }

        .section-subtitle {
            color: #94a3b8;
            margin-bottom: 40px;
        }

        /* ABOUT */
        .about-grid {
            display: grid;
            grid-template-columns: 1.2fr .8fr;
            gap: 25px;
        }

        .card {
            background: #111827;
            border: 1px solid #1e293b;
            border-radius: 18px;
            padding: 30px;
        }

        .card p {
            color: #94a3b8;
        }

        /* SKILLS */
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .skill {
            background: #172033;
            border: 1px solid #263449;
            color: #cbd5e1;
            padding: 9px 13px;
            border-radius: 8px;
            font-size: 13px;
        }

        /* PROJECTS */
        .projects {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .project {
            transition: .2s;
        }

        .project:hover {
            transform: translateY(-5px);
            border-color: #38bdf8;
        }

        .project-label {
            color: #38bdf8;
            font-size: 12px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .project h3 {
            margin: 10px 0;
            font-size: 22px;
        }

        .project p {
            margin-bottom: 20px;
        }

        .tech {
            color: #64748b;
            font-size: 13px;
        }

        /* EXPERIENCE & TIMELINE */
        .timeline {
            border-left: 2px solid #1e293b;
            padding-left: 30px;
        }

        .timeline-item {
            position: relative;
            margin-bottom: 45px;
        }

        .timeline-item::before {
            content: "";
            position: absolute;
            width: 12px;
            height: 12px;
            background: #38bdf8;
            border-radius: 50%;
            left: -37px;
            top: 8px;
        }

        .timeline-item h3 {
            font-size: 21px;
            margin-bottom: 5px;
        }

        .timeline-item .date {
            color: #38bdf8;
            font-size: 13px;
            margin-bottom: 12px;
        }

        .timeline-item p {
            color: #94a3b8;
        }

        /* NOVAS CLASSES: FORMAÇÃO, IDIOMAS E CERTIFICAÇÕES */
        .lang-bar {
            width: 100%;
            height: 6px;
            background: #1e293b;
            border-radius: 4px;
            overflow: hidden;
        }
        
        .lang-progress {
            height: 100%;
            background: linear-gradient(90deg, #38bdf8, #818cf8);
            border-radius: 4px;
        }
        
        .cert-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .cert-item {
            display: flex;
            align-items: center;
            gap: 15px;
            background: #172033;
            border: 1px solid #263449;
            padding: 15px;
            border-radius: 12px;
            transition: .2s;
        }
        
        .cert-item:hover {
            border-color: #38bdf8;
            transform: translateX(5px);
        }
        
        .cert-icon {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: rgba(56, 189, 248, 0.1);
            color: #38bdf8;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            flex-shrink: 0;
            font-size: 14px;
        }
        
        .cert-item h4 {
            font-size: 15px;
            color: #e2e8f0;
        }

        /* CONTACT */
        .contact {
            text-align: center;
            background: #0f172a;
        }

        .contact p {
            color: #94a3b8;
            max-width: 600px;
            margin: 15px auto 30px;
        }

        .contact-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 12px;
        }

        /* FOOTER */
        footer {
            padding: 25px;
            text-align: center;
            border-top: 1px solid #1e293b;
            color: #64748b;
            font-size: 13px;
        }

        /* MOBILE */
        @media (max-width: 700px) {
            .nav-links {
                display: none;
            }
            .hero {
                min-height: 80vh;
            }
            .hero h1 {
                letter-spacing: -2px;
            }
            .hero h2 {
                font-size: 20px;
            }
            .hero p {
                font-size: 16px;
            }
            .about-grid,
            .projects {
                grid-template-columns: 1fr;
            }
            section {
                padding: 65px 0;
            }
            .section-title {
                font-size: 30px;
            }
        }
    </style>
</head>
<body>

    <nav>
        <div class="container nav-content">
            <div class="logo">
                JA<span>.</span>
            </div>
            <ul class="nav-links">
                <li><a href="#sobre">Sobre</a></li>
                <li><a href="#projetos">Projetos</a></li>
                <li><a href="#experiencia">Experiência</a></li>
                <li><a href="#formacao">Formação</a></li>
                <li><a href="#contato">Contato</a></li>
            </ul>
        </div>
    </nav>

    <section class="hero">
        <div class="container hero-content">
            <div class="tag">
                DADOS • PROCESSOS • TECNOLOGIA
            </div>
            <h1>José Alejandro<br><span>Silva Costa</span></h1>
            <h2>Analista de Dados | Processos | Tecnologia</h2>
            <p>
                Profissional com sólida capacidade analítica e técnica, focado em utilizar dados, 
                automação e desenvolvimento para otimizar fluxos operacionais e apoiar decisões estratégicas.
            </p>
            <div class="buttons">
                <a href="#projetos" class="button button-primary">Ver meus projetos</a>
                <a href="curriculo.pdf" target="_blank" class="button button-secondary">↓ Baixar CV (PDF)</a>
                <a href="https://github.com/alejandrocosta1" target="_blank" class="button button-secondary">GitHub ↗</a>
                <a href="https://www.linkedin.com" target="_blank" class="button button-secondary">LinkedIn ↗</a>
            </div>
        </div>
    </section>

    <!-- Adicione as suas seções de SOBRE e PROJETOS exatamente como já estavam aqui no meio -->

    <section id="formacao">
        <div class="container">
            <h2 class="section-title">Formação & Certificações</h2>
            <p class="section-subtitle">Minha base acadêmica e ferramentas do ofício.</p>

            <div class="about-grid">
                
                <!-- Coluna 1: Acadêmico e Idiomas -->
                <div class="card">
                    <h3 style="margin-bottom: 25px; color: #f8fafc;">Trajetória Acadêmica</h3>
                    
                    <div class="timeline">
                        <div class="timeline-item">
                            <h3>Análise e Desenvolvimento de Sistemas</h3>
                            <div class="date">UNINASSAU • Em andamento</div>
                            <p>Formação voltada para desenvolvimento de software, modelagem de banco de dados e resolução de problemas tecnológicos.</p>
                        </div>
                    </div>

                    <h3 style="margin-bottom: 20px; margin-top: 35px; color: #f8fafc;">Idiomas</h3>
                    
                    <div style="margin-bottom: 20px;">
                        <div style="display: flex; justify-content: space-between; font-size: 14px; margin-bottom: 8px;">
                            <span style="color: #e2e8f0;">Português</span><span style="color: #64748b;">Nativo</span>
                        </div>
                        <div class="lang-bar"><div class="lang-progress" style="width: 100%;"></div></div>
                    </div>

                    <div>
                        <div style="display: flex; justify-content: space-between; font-size: 14px; margin-bottom: 8px;">
                            <span style="color: #e2e8f0;">Inglês</span><span style="color: #64748b;">Intermediário</span>
                        </div>
                        <div class="lang-bar"><div class="lang-progress" style="width: 50%;"></div></div>
                        <p style="font-size: 12px; color: #64748b; margin-top: 8px;">CLEC - Centro de Línguas Estrangeiras do Ceará</p>
                    </div>
                </div>

                <!-- Coluna 2: Certificações -->
                <div class="card">
                    <h3 style="margin-bottom: 25px; color: #f8fafc;">Certificações Recentes</h3>
                    
                    <div class="cert-list">
                        <!-- Exemplo 1 -->
                        <div class="cert-item">
                            <div class="cert-icon">✓</div>
                            <div>
                                <h4>Power BI e Dashboards</h4>
                                <span class="tech">Instituição/Ano</span>
                            </div>
                        </div>
                        
                        <!-- Exemplo 2 -->
                        <div class="cert-item">
                            <div class="cert-icon">✓</div>
                            <div>
                                <h4>Análise de Dados com Python</h4>
                                <span class="tech">Instituição/Ano</span>
                            </div>
                        </div>
                        
                        <!-- Exemplo 3 -->
                        <div class="cert-item">
                            <div class="cert-icon">✓</div>
                            <div>
                                <h4>Modelagem de Banco de Dados SQL</h4>
                                <span class="tech">Instituição/Ano</span>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <section id="contato" class="contact">
        <div class="container">
            <h2 class="section-title">Vamos conversar?</h2>
            <p>
                Estou aberto a oportunidades relacionadas a Dados, Processos, BI e Tecnologia. Baixe a versão em PDF do meu currículo ou fale comigo diretamente pelos canais abaixo.
            </p>
            <div class="contact-links">
                <a href="curriculo.pdf" target="_blank" class="button button-primary">↓ Baixar CV (PDF)</a>
                <a href="mailto:seuemail@gmail.com" class="button button-secondary">✉ E-mail</a>
                <a href="https://wa.me/5585999999999" target="_blank" class="button button-secondary">💬 WhatsApp</a>
            </div>
        </div>
    </section>

    <footer>
        © 2026 José Alejandro Silva Costa • Dados, Processos & Tecnologia
    </footer>

</body>
</html>
