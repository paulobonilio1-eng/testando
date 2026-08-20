<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>MODÃO FIT | Academia Raiz</title>

    <style>

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #080808;
            color: white;
        }

        /* =========================
           CABEÇALHO
        ========================= */

        header {
            position: fixed;
            top: 0;
            left: 0;

            width: 100%;
            height: 85px;

            background: rgba(5, 5, 5, 0.96);

            border-bottom: 1px solid #9c6d24;

            display: flex;
            align-items: center;
            justify-content: space-between;

            padding: 5px 7%;

            z-index: 1000;
        }

        .logo-menu {
            height: 70px;
            width: auto;
            object-fit: contain;
        }

        nav {
            display: flex;
            gap: 30px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        nav a:hover {
            color: #d6a84f;
        }

        /* =========================
           HERO
        ========================= */

        .hero {

            min-height: 100vh;

            padding: 140px 8% 80px;

            display: flex;

            align-items: center;
            justify-content: space-between;

            gap: 60px;

            background:
                linear-gradient(
                    rgba(0,0,0,0.78),
                    rgba(0,0,0,0.92)
                ),
                radial-gradient(
                    circle at center,
                    #4b3010,
                    #080808 65%
                );
        }

        .hero-text {
            max-width: 620px;
        }

        .hero-text small {
            color: #d6a84f;
            font-weight: bold;
            letter-spacing: 4px;
        }

        .hero h1 {
            font-size: clamp(60px, 9vw, 110px);
            line-height: 0.85;
            margin: 25px 0;
            font-weight: 900;
            letter-spacing: -5px;
        }

        .hero h1 span {
            color: #d6a84f;
        }

        .hero p {
            color: #ccc;
            font-size: 19px;
            line-height: 1.7;
            margin-bottom: 30px;
        }

        .botao {

            display: inline-block;

            padding: 16px 30px;

            background: #d6a84f;

            color: #111;

            text-decoration: none;

            font-weight: 900;

            border-radius: 4px;

            transition: 0.3s;
        }

        .botao:hover {
            transform: translateY(-4px);
            background: #f1ca73;
        }

        /* =========================
           LOGO PRINCIPAL
        ========================= */

        .logo-principal {

            width: 470px;

            max-width: 100%;

            filter:
                drop-shadow(
                    0 0 35px
                    rgba(214,168,79,0.25)
                );

            animation: aparecer 1.2s ease;
        }

        @keyframes aparecer {

            from {
                opacity: 0;
                transform: scale(0.8);
            }

            to {
                opacity: 1;
                transform: scale(1);
            }

        }

        /* =========================
           SEÇÕES
        ========================= */

        section {
            padding: 100px 8%;
        }

        .titulo {
            text-align: center;
            margin-bottom: 60px;
        }

        .titulo h2 {
            font-size: 45px;
        }

        .titulo span {
            color: #d6a84f;
        }

        .titulo p {
            color: #999;
            margin-top: 12px;
        }

        /* =========================
           MÚSICA
        ========================= */

        .musica {
            background: #111;
        }

        .musica-container {

            max-width: 1100px;

            margin: auto;

            display: grid;

            grid-template-columns:
                1fr 1fr;

            gap: 50px;

            align-items: center;
        }

        /* TV */

        .tv {

            background: #050505;

            border: 12px solid #242424;

            border-radius: 10px;

            padding: 10px;

            box-shadow:
                0 20px 50px
                rgba(0,0,0,0.7);
        }

        .tela {

            aspect-ratio: 16 / 9;

            display: flex;

            flex-direction: column;

            justify-content: center;

            align-items: center;

            text-align: center;

            background:
                radial-gradient(
                    circle,
                    #6d4819,
                    #130c03
                );
        }

        .play {
            font-size: 65px;
            margin-bottom: 10px;
        }

        .tela h3 {
            font-size: 25px;
        }

        .tela p {
            color: #d6a84f;
            margin-top: 8px;
        }

        /* =========================
           TEXTO DA MÚSICA
        ========================= */

        .musica-text h3 {

            font-size: 36px;

            margin-bottom: 20px;
        }

        .musica-text p {

            color: #aaa;

            line-height: 1.8;

            margin-bottom: 25px;
        }

        .player {

            background: #191919;

            padding: 20px;

            border-left:
                4px solid #d6a84f;

            border-radius: 4px;
        }

        .player strong {
            color: #d6a84f;
        }

        /* =========================
           TREINOS
        ========================= */

        .cards {

            max-width: 1100px;

            margin: auto;

            display: grid;

            grid-template-columns:
                repeat(3, 1fr);

            gap: 25px;
        }

        .card {

            background: #151515;

            padding: 35px 25px;

            border: 1px solid #292929;

            border-radius: 8px;

            transition: 0.3s;
        }

        .card:hover {

            transform: translateY(-8px);

            border-color: #d6a84f;

            box-shadow:
                0 15px 35px
                rgba(214,168,79,0.12);
        }

        .icone {

            font-size: 45px;

            margin-bottom: 20px;
        }

        .card h3 {

            color: #d6a84f;

            margin-bottom: 12px;
        }

        .card p {

            color: #999;

            line-height: 1.6;
        }

        /* =========================
           FRASE
        ========================= */

        .frase {

            text-align: center;

            background:
                linear-gradient(
                    rgba(0,0,0,0.7),
                    rgba(0,0,0,0.85)
                ),
                #321f09;
        }

        .frase h2 {

            font-size:
                clamp(35px, 6vw, 75px);

            color: #d6a84f;

            text-transform: uppercase;
        }

        .frase p {

            margin-top: 20px;

            font-size: 20px;

            color: #ddd;
        }

        /* =========================
           RODAPÉ
        ========================= */

        footer {

            background: #050505;

            padding: 60px 8%;

            text-align: center;

            border-top:
                1px solid #292929;
        }

        .logo-footer {

            width: 180px;

            margin-bottom: 20px;
        }

        footer p {

            color: #777;

            margin-top: 12px;
        }

        .social {

            margin-top: 25px;
        }

        .social a {

            color: white;

            text-decoration: none;

            margin: 0 12px;

            transition: 0.3s;
        }

        .social a:hover {
            color: #d6a84f;
        }

        /* =========================
           CELULAR
        ========================= */

        @media (max-width: 800px) {

            header {
                padding: 5px 20px;
            }

            .logo-menu {
                height: 60px;
            }

            nav {
                display: none;
            }

            .hero {

                flex-direction: column;

                text-align: center;

                padding-top: 130px;
            }

            .logo-principal {
                width: 330px;
            }

            .musica-container {
                grid-template-columns: 1fr;
            }

            .cards {
                grid-template-columns: 1fr;
            }

        }

    </style>

</head>


<body>


    <!-- =========================
         MENU
    ========================= -->

    <header>

        <img
            src="ChatGPT Image 17 de ago. de 2026, 22_27_50.png"
            alt="Logo Modão Fit"
            class="logo-menu"
        >

        <nav>

            <a href="#inicio">
                Início
            </a>

            <a href="#musica">
                Nossa Música
            </a>

            <a href="#treinos">
                Treinos
            </a>

            <a href="#contato">
                Contato
            </a>

        </nav>

    </header>


    <!-- =========================
         INÍCIO
    ========================= -->

    <section
        class="hero"
        id="inicio"
    >

        <div class="hero-text">

            <small>
                ACADEMIA RAIZ
            </small>

            <h1>

                TREINE<br>

                <span>NO RITMO</span>

            </h1>

            <p>

                Bem-vindo à Modão Fit.

                Uma ideia que nasceu por causa
                de uma conversa entre amigos,
                hoje sócios e donos.

                Paulo e Vanessa são os responsáveis
                pelo sucesso da academia, que tem
                como objetivo unir o treino com a música.

            </p>

            <a
                href="#treinos"
                class="botao"
            >

                CONHEÇA A ACADEMIA

            </a>

        </div>


        <!-- LOGO OFICIAL -->

        <img
            src="ChatGPT Image 17 de ago. de 2026, 22_27_50.png"
            alt="MODÃO FIT"
            class="logo-principal"
        >

    </section>


    <!-- =========================
         MÚSICA
    ========================= -->

    <section
        class="musica"
        id="musica"
    >

        <div class="titulo">

            <h2>

                AQUI O
                <span>MODÃO</span>
                TOCA

            </h2>

            <p>
                Academia sem sertanejo?
                Aqui não!
            </p>

        </div>


        <div class="musica-container">


            <!-- TV -->

            <div class="tv">

                <div class="tela">

                    <iframe
                        width="100%"
                        height="100%"
                        src="https://www.youtube.com/embed/Y59pC4FcBxM?si=2ieiJPny2z_H9PrH"
                        title="YouTube video player"
                        frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                        referrerpolicy="strict-origin-when-cross-origin"
                        allowfullscreen>
                    </iframe>

                </div>

            </div>


            <!-- TEXTO -->

            <div class="musica-text">

                <h3>
                    Treino + Moda de Viola
                </h3>

                <p>

                    Enquanto você treina,
                    nossa TV transmite música,
                    clipes e os grandes clássicos
                    do sertanejo.

                </p>


                <div class="player">

                    🎵 Tocando agora

                    <br><br>

                    <strong>
                        Evidência - Chitãozinho & Xororó
                    </strong>

                    <br><br>

                    ███████████░░░░░

                    <br><br>

                    02:31 / 04:12

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         TREINOS
    ========================= -->

    <section id="treinos">

        <div class="titulo">

            <h2>

                SEU
                <span>TREINO</span>

            </h2>

            <p>

                Pegue seu equipamento
                e bora pro modão.

            </p>

        </div>


        <div class="cards">


            <!-- MUSCULAÇÃO -->

            <div class="card">

                <div class="icone">
                    🏋️
                </div>

                <h3>
                    MUSCULAÇÃO
                </h3>

                <p>

                    Equipamentos completos
                    para seus treinos de força.

                </p>

            </div>


            <!-- FUNCIONAL -->

            <div class="card">

                <div class="icone">
                    🔥
                </div>

                <h3>
                    FUNCIONAL
                </h3>

                <p>

                    Treinos dinâmicos para
                    melhorar condicionamento
                    e resistência.

                </p>

            </div>


            <!-- CARDIO -->

            <div class="card">

                <div class="icone">
                    🚴
                </div>

                <h3>
                    CARDIO
                </h3>

                <p>

                    Esteiras, bicicletas e
                    equipamentos para cardio.

                </p>

            </div>


        </div>

    </section>


    <!-- =========================
         FRASE
    ========================= -->

    <section class="frase">

        <h2>
            TREINE FORTE.
        </h2>

        <h2>
            ESCUTE MODÃO.
        </h2>

        <p>
            🤠 Música boa. Corpo forte. Vida melhor.
        </p>

    </section>


    <!-- =========================
         RODAPÉ
    ========================= -->

    <footer id="contato">

        <img
            src="ChatGPT Image 17 de ago. de 2026, 22_35_38.png"
            alt="Modão Fit"
            class="logo-footer"
        >

        <p>

            Academia raiz, música boa
            e treino de verdade.

        </p>


        <div class="social">

            <a href="#">
                Instagram
            </a>

            <a href="#">
                WhatsApp
            </a>

            <a href="#">
                Facebook
            </a>

        </div>


        <p>
            © 2026 MODÃO FIT
        </p>

    </footer>


</body>

</html>
