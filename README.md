# Atividade_20
<!DOCTYPE html>
<html>
<head>
    <title>Série de Fibonacci</title>
</head>
<body>
    <h1>Trinta primeiros valores da série de Fibonacci</h1>
    <p id="resultado"></p>

    <script>
        // Função para calcular os trinta primeiros valores da série de Fibonacci
        function calcularFibonacci() {
            let fibonacci = [1, 1];
            for (let i = 2; i < 30; i++) {
                fibonacci[i] = fibonacci[i - 1] + fibonacci[i - 2];
            }
            return fibonacci;
        }

        // Exibindo os valores no parágrafo com o id "resultado"
        document.getElementById("resultado").innerText = "Os trinta primeiros valores da série de Fibonacci são: " + calcularFibonacci().join(", ");
    </script>
</body>
</html>
