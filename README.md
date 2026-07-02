<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema de Reações</title>
    <style>
        /* CSS para garantir que a página não fique branca/invisível */
        body {
            background-color: #f0f2f5;
            color: #1c1e21;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
            height: 100vh;
            margin: 0;
        }

        .botao-reacao {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 20px;
            font-size: 18px;
            border: 1px solid #ccd0d5;
            border-radius: 20px;
            background-color: #ffffff;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .botao-reacao:hover {
            transform: scale(1.05);
            background-color: #e4e6eb;
        }

        .contador {
            font-weight: bold;
            color: #65676b;
        }
    </style>
</head>
<body>

    <button class="botao-reacao">
        <span>👍</span>
        <span class="contador">0</span>
    </button>

    <button class="botao-reacao">
        <span>🚀</span>
        <span class="contador">0</span>
    </button>

    <button class="botao-reacao">
        <span>❤️</span>
        <span class="contador">0</span>
    </button>

    <button class="botao-reacao">
        <span>🎉</span>
        <span class="contador">0</span>
    </button>


    <script>
        // Seleciona todos os botões pela classe comum
        const botoesReacao = document.querySelectorAll('.botao-reacao');

        // Adiciona o evento de clique em cada um deles
        botoesReacao.forEach(botao => {
            botao.addEventListener('click', () => {
                // Encontra o contador específico DESTE botão que foi clicado
                const contadorElemento = botao.querySelector('.contador');
                
                // Pega o número atual, soma +1 e atualiza na tela
                let quantidadeAtual = parseInt(contadorElemento.textContent);
                contadorElemento.textContent = quantidadeAtual + 1;
            });
        });
    </script>

</body>
</html>
