<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Momozinho</title>
    <style>
        body {
            background-color: #ff4d4d;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            font-family: 'Arial', sans-serif;
        }
        
        .painel {
            margin: auto;
            background-color: white;
            width: 90%;
            max-width: 500px;
            height: auto;
            min-height: 500px;
            border-radius: 20px;
            text-align: center;
            padding: 50px 20px 20px;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            position: relative;
            box-shadow: 0 0 20px rgba(0,0,0,0.2);
        }
        
        h1 {
            color: #ff4d4d;
            margin-bottom: 30px;
        }
        
        img {
            width: 200px;
            height: auto;
            border-radius: 10px;
            margin: 10px 0;
            border: 3px solid #ffcccc;
        }
        
        h2 {
            color: #333;
            margin: 20px 0 30px;
        }
        
        #sim {
            height: 40px;
            width: 60px;
            background-color: #ff4d4d;
            border: 2px solid white;
            border-radius: 10px;
            color: white;
            margin-right: 20px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.2s;
        }
        
        #sim:hover {
            background-color: #ff3333;
            transform: scale(1.05);
        }
        
        #nao {
            height: 40px;
            width: 60px;
            background-color: #ff4d4d;
            border: 2px solid white;
            border-radius: 10px;
            color: white;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.2s;
            position: static;
        }
        
        #nao:hover {
            background-color: #ff3333;
        }
        
        .botoes {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            position: relative;
        }
        
        .hidden {
            display: none;
        }
        
        .message {
            margin-top: 20px;
            color: #ff4d4d;
            font-weight: bold;
            animation: pulse 0.5s infinite alternate;
        }
        
        @keyframes pulse {
            from { transform: scale(1); }
            to { transform: scale(1.05); }
        }
    </style>
</head>
<body>
    <div class="painel">
        <h1>Momozinho</h1>
        <img src="https://i.pinimg.com/originals/90/c5/5f/90c55f5ae837a02d9d4080cc32a04782.gif" alt="Coração animado">
        <h2>Você aceita ficar de dengo comigo?</h2>
        
        <div class="botoes">
            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" id="linkVideo"><button id="sim">Sim!</button></a>
            <button id="nao">Não!</button>
        </div>
        
        <div id="obrigado" class="hidden message">
            Oba! Você fez a escolha certa! ❤️
        </div>
    </div>
    
    <script>
        // Função para fazer o botão fugir
        function fuja() {
            var botaoNao = document.getElementById("nao");
            var painel = document.querySelector(".painel");
            
            // Calcula área disponível para movimento
            var larguraDisponivel = window.innerWidth - botaoNao.offsetWidth;
            var alturaDisponivel = window.innerHeight - botaoNao.offsetHeight;
            
            // Gera posições aleatórias
            var aleatorioX = Math.floor(Math.random() * larguraDisponivel);
            var aleatorioY = Math.floor(Math.random() * alturaDisponivel);
            
            // Posiciona o botão
            botaoNao.style.position = "fixed";
            botaoNao.style.left = aleatorioX + "px";
            botaoNao.style.top = aleatorioY + "px";
            
            // Efeito visual
            botaoNao.style.transform = "scale(0.9)";
            setTimeout(() => {
                botaoNao.style.transform = "scale(1)";
            }, 100);
        }
        
        // Event listeners
        document.getElementById("nao").addEventListener("mouseover", fuja);
        document.getElementById("nao").addEventListener("touchstart", function() {
            // Para dispositivos móveis
            fuja();
            // Evita que o toque dispare outros eventos
            event.preventDefault();
        });
        
        document.getElementById("sim").addEventListener("click", function(e) {
            e.preventDefault();
            document.getElementById("obrigado").classList.remove("hidden");
            
            // Redireciona após 1.5 segundos
            setTimeout(() => {
                window.location.href = document.getElementById("linkVideo").href;
            }, 1500);
        });
    </script>
</body>
</html>
