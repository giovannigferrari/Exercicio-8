<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8Calculadora de Ligações Iônicas e Covalentes</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        input, button {
            padding: 10px;
            margin: 5px;
        }
        .result {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Calculadora de Proporções em Ligações Químicas</h1>
    <h2>Ligações Iônicas</h2>
    <label for="eletronsMetal">Elétrons que o metal perde (positivo):</label>
    <input type="number" id="eletronsMetal" placeholder="Ex: 2" />
    <br>
    <label for="eletronsAmetal">Elétrons que o ametal ganha (negativo):</label>
    <input type="number" id="eletronsAmetal" placeholder="Ex: 1" />
    <br>
    <button onclick="calcularLigacaoIonica()">Calcular Fórmula Iônica</button>
    <div class="result">
        <p><strong>Fórmula Mínima da Ligação Iônica:</strong> <span id="formulaIonica"></span></p>
    </div>
    <script>
        function calcularLigacaoIonica() {
            const eletronsMetal = parseInt(document.getElementById('eletronsMetal').value);
            const eletronsAmetal = parseInt(document.getElementById('eletronsAmetal').value);
            if (isNaN(eletronsMetal) || isNaN(eletronsAmetal) || eletronsMetal <= 0 || eletronsAmetal <= 0) {
                alert("Por favor, insira números válidos para os elétrons.");
                return;
            }
            let proporcaoMetal = eletronsAmetal;
            let proporcaoAmetal = eletronsMetal;
            document.getElementById('formulaIonica').textContent = `M${proporcaoMetal}A${proporcaoAmetal}`;
        }
    </script>
</body>
</html>
