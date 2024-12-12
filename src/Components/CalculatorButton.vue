    <template>
        <button @click="action">{{ label }}</button>
    </template>
    
    <script>
    export default {
        name: 'CalculatorButton',
        props: {
        label: String,
        action: Function,
        },
    };
    </script>
    
    <style scoped>
    button {
        padding: 10px 20px;
        margin: 5px;
        font-size: 1rem;
        background-color: #007BFF;
        color: #fff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
    
    button:hover {
        background-color: #0056b3;
    }
    </style>
    