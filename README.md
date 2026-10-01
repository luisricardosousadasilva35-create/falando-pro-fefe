<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Para alguém especial ✨</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;600;700&family=Zeyada&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            min-height: 100vh;
            overflow: hidden;
            font-family: 'Quicksand', sans-serif;
            background: linear-gradient(180deg, #081426 0%, #102844 55%, #183d5d 100%);
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }

        /* estrelas */
        .stars {
            position: absolute;
            inset: 0;
            overflow: hidden;
        }

        .star {
            position: absolute;
            width: 3px;
            height: 3px;
            background: white;
            border-radius: 50%;
            box-shadow: 0 0 8px rgba(255,255,255,0.8);
            animation: brilho 2s infinite alternate;
        }

        .star:nth-child(1)  { top: 10%; left: 15%; animation-delay: .2s; }
        .star:nth-child(2)  { top: 20%; left: 80%; animation-delay: .8s; }
        .star:nth-child(3)  { top: 35%; left: 8%; animation-delay: 1.2s; }
        .star:nth-child(4)  { top: 15%; left: 55%; animation-delay: .5s; }
        .star:nth-child(5)  { top: 70%; left: 90%; animation-delay: 1s; }
        .star:nth-child(6)  { top: 80%; left: 18%; animation-delay: .3s; }
        .star:nth-child(7)  { top: 60%; left: 75%; animation-delay: 1.4s; }
        .star:nth-child(8)  { top: 45%; left: 92%; animation-delay: .7s; }
        .star:nth-child(9)  { top: 85%; left: 55%; animation-delay: 1.1s; }
        .star:nth-child(10) { top: 8%; left: 35%; animation-delay: .9s; }
        .star:nth-child(11) { top: 55%; left: 40%; animation-delay: .4s; }
        .star:nth-child(12) { top: 30%; left: 65%; animation-delay: 1.3s; }

        @keyframes brilho {
            from {
                opacity: 0.25;
                transform: scale(0.7);
            }
            to {
                opacity: 1;
                transform: scale(1.5);
            }
        }

        /* lua */
        .moon {
            position: absolute;
            top: 8%;
            right: 10%;
            width: 85px;
            height: 85px;
            background: #f9e9b4;
            border-radius: 50%;
            box-shadow: 0 0 35px rgba(249, 233, 180, 0.25);
        }

        .moon::after {
            content: "";
            position: absolute;
            top: -5px;
            left: 20px;
            width: 85px;
            height: 85px;
            background: #081426;
            border-radius: 50%;
        }

        /* conteúdo */
        .container {
            width: min(90%, 700px);
            text-align: center;
            position: relative;
            z-index: 2;
            padding: 35px;
            background: rgba(7, 19, 36, 0.42);
            border: 1px solid rgba(255,255,255,0.12);
            border-radius: 25px;
            backdrop-filter: blur(8px);
            box-shadow: 0 20px 70px rgba(0,0,0,0.25);
        }

        .pequena-luz {
            font-size: 18px;
            color: #f9d77e;
            margin-bottom: 12px;
            letter-spacing: 3px;
        }

        h1 {
            font-family: 'Zeyada', cursive;
            font-size: clamp(48px, 8vw, 76px);
            font-weight: 400;
            color: #ffe7a1;
            margin-bottom: 20px;
        }

        .texto {
            font-size: 19px;
            line-height: 1.8;
            color: #f5f1e6;
            margin-bottom: 28px;
        }

        .destaque {
            color: #ffe4a0;
            font-weight: 600;
        }

        .pergunta {
            font-family: 'Zeyada', cursive;
            font-size: clamp(36px, 6vw, 55px);
            color: #fff0bd;
            margin-bottom: 25px;
        }

        .botoes {
            position: relative;
            height: 110px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 18px;
        }

        button {
            border: none;
            padding: 14px 28px;
            border-radius: 999px;
            font-family: 'Quicksand', sans-serif;
            font-size: 17px;
            font-weight: 700;
            cursor: pointer;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        #sim {
            background: #f5ce73;
            color: #24334a;
            box-shadow: 0 8px 25px rgba(245, 206, 115, 0.3);
        }

        #sim:hover {
            transform: scale(1.08);
            box-shadow: 0 12px 30px rgba(245, 206, 115, 0.45);
        }

        #nao {
            background: #ffffff;
            color: #3c4a5d;
            position: absolute;
            left: 50%;
            transform: translateX(55px);
        }

        .frase-final {
            display: none;
            margin-top: 20px;
            font-family: 'Zeyada', cursive;
            font-size: 38px;
            color: #ffe7a1;
            animation: aparecer 1s ease forwards;
        }

        @keyframes aparecer {
            from {
                opacity: 0;
                transform: translateY(12px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 600px) {
            .container {
                padding: 28px 20px;
            }

            .texto {
                font-size: 17px;
            }

            .moon {
                width: 60px;
                height: 60px;
                right: 6%;
            }

            .moon::after {
                width: 60px;
                height: 60px;
                left: 14px;
            }
        }
    </style>
</head>

<body>

    <div class="stars">
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
    </div>

    <div class="moon"></div>

    <div class="container">

        <div class="pequena-luz">✦ PARA VOCÊ ✦</div>

        <h1>Entre todas as estrelas...</h1>

        <p class="texto">
            Eu não me arrependo de te conhecer,<br>
            porque <span class="destaque">tu me cativas</span>
            e eu <span class="destaque">te cativo</span>.<br><br>

            E, em um mundo tão grande,<br>
            tão cheio de caminhos e estrelas,<br>
            às vezes parece que existe apenas<br>
            <span class="destaque">nós dois.</span>
        </p>

        <div class="pergunta">
            Tu aceitas ser meu calabresso? ❤️
        </div>

        <div class="botoes">
            <button id="sim">Sim ✨</button>
            <button id="nao">Não</button>
        </div>

        <div class="frase-final" id="final">
            Então vem... vamos cuidar da nossa pequena estrela. 🌹
        </div>

    </div>

    <script>
        const botaoNao = document.getElementById("nao");
        const botaoSim = document.getElementById("sim");
        const fraseFinal = document.getElementById("final");

        function fugir() {
            const largura = window.innerWidth;
            const altura = window.innerHeight;

            const margem = 20;

            const novoX = Math.random() * (largura - botaoNao.offsetWidth - margem * 2) + margem;
            const novoY = Math.random() * (altura - botaoNao.offsetHeight - margem * 2) + margem;

            botaoNao.style.position = "fixed";
            botaoNao.style.left = novoX + "px";
            botaoNao.style.top = novoY + "px";
            botaoNao.style.transform = "none";
        }

        botaoNao.addEventListener("mouseover", fugir);
        botaoNao.addEventListener("touchstart", fugir);
        botaoNao.addEventListener("click", fugir);

        botaoSim.addEventListener("click", () => {
            fraseFinal.style.display = "block";
            botaoSim.style.display = "none";
            botaoNao.style.display = "none";
        });
    </script>

</body>
</html>
