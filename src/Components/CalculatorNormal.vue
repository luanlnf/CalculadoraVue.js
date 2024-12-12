    <template>
        <div class="calculator">
        <h3 class="calculator-info">Calculadora Aritmética</h3>
        <div class="calculator-body">
            <input type="number" v-model="numero1" placeholder="Primeiro número" />
            <input type="number" v-model="numero2" placeholder="Segundo número" />
            <select v-model="operacao">
            <option value="+">Soma</option>
            <option value="-">Subtração</option>
            <option value="*">Multiplicação</option>
            <option value="/">Divisão</option>
            </select>
            <div v-if="resultado !== null">
            <p>Resultado: {{ resultado }}</p>
            </div>
        </div>
        </div>
    </template>
    
    <script>
    export default {
        name: 'CalculatorNormal',
        data() {
        return {
            numero1: 0,
            numero2: 0,
            operacao: '+',
            resultado: null,
        };
        },
        watch: {
        numero1: 'calcular',
        numero2: 'calcular',
        operacao: 'calcular',
        },
        methods: {
        calcular() {
            const num1 = parseFloat(this.numero1);
            const num2 = parseFloat(this.numero2);
            if (isNaN(num1) || isNaN(num2)) {
            this.resultado = null;
            return;
            }
            switch (this.operacao) {
            case '+':
                this.resultado = num1 + num2;
                break;
            case '-':
                this.resultado = num1 - num2;
                break;
            case '*':
                this.resultado = num1 * num2;
                break;
            case '/':
                this.resultado = num2 !== 0 ? num1 / num2 : 'Erro: Divisão por zero';
                break;
            }
        },
        },
    };
    </script>
    
    <style scoped>
    .calculator {
        margin-top: 20px;
    }
    
    .calculator-info {
        font-size: 1rem;
        color: #333;
        margin-bottom: 10px;
    }
    
    .calculator-body {
        display: inline-block;
        text-align: center;
        border: 2px solid #ccc;
        border-radius: 10px;
        padding: 20px;
        background-color: #8c8d8a;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
    
    input[type="number"] {
        width: 90%;
        max-width: 300px;
        padding: 8px;
        font-size: 1.2rem;
        border: 1px solid #ccc;
        border-radius: 5px;
        margin-bottom: 15px;
    }
    
    select {
        padding: 8px;
        font-size: 1rem;
        border: 1px solid #ccc;
        border-radius: 5px;
        margin-bottom: 15px;
    }
    </style>
    