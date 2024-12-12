    <template>
        <div class="calculator">
        <h3 class="calculator-info">Calculadora Científica</h3>
        <div class="calculator-body">
            <input type="number" v-model="scientificInput" placeholder="Digite um número" />
            <div class="buttons">
            <button @click="squareScientific">x²</button>
            <button @click="sqrtScientific">√x</button>
            </div>
            <div v-if="scientificResult !== null">
            <p>Resultado: {{ scientificResult }}</p>
            </div>
        </div>
        </div>
    </template>
    
    <script>
    export default {
        name: 'CalculatorScientific',
        data() {
        return {
            scientificInput: 0,
            scientificResult: null,
        };
        },
        methods: {
        squareScientific() {
            try {
            this.scientificResult = Math.pow(Number(this.scientificInput), 2);
            } catch {
            this.scientificResult = 'Erro';
            }
        },
        sqrtScientific() {
            try {
            this.scientificResult = Math.sqrt(Number(this.scientificInput));
            } catch {
            this.scientificResult = 'Erro';
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
    
    .buttons {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 10px;
    }
    </style>
    