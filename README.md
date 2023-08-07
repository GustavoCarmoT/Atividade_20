# Atividade_20
<!DOCTYPE html>
<html>
<head>
    <title>Serie de Fibonacci</title>
    <style>
        .red { color: red; }
        .blue { color: blue; }
        .green { color: green; }
    </style>
</head>
<body>
    <h1>Serie de Fibonacci</h1>
    <p id="fibonacciSequence"></p>

    <script>
        
        function fibonacci(n) {
            const sequence = [1, 1];
            for (let i = 2; i < n; i++) {
                sequence.push(sequence[i - 1] + sequence[i - 2]);
            }
            return sequence;
        }

       
        function isPrime(number) {
            if (number <= 1) return false;
            if (number <= 3) return true;
            if (number % 2 === 0 || number % 3 === 0) return false;

            let i = 5;
            while (i * i <= number) {
                if (number % i === 0 || number % (i + 2) === 0) return false;
                i += 6;
            }

            return true;
        }

        
        function displayFibonacciWithColors(n) {
            const fibonacciSequence = fibonacci(n);
            const fibonacciElement = document.getElementById('fibonacciSequence');

            for (let i = 0; i < fibonacciSequence.length; i++) {
                const number = fibonacciSequence[i];
                const spanElement = document.createElement('span');
                spanElement.textContent = number;

                if (number % 2 === 0) {
                    spanElement.classList.add('blue');
                } else {
                    spanElement.classList.add('red');
                }

                if (isPrime(number)) {
                    spanElement.classList.add('green');
                }

                fibonacciElement.appendChild(spanElement);
                fibonacciElement.appendChild(document.createTextNode(', '));
            }
        }

      
        displayFibonacciWithColors(30);
    </script>
</body>
</html>
