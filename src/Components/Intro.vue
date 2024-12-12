<template>
        <div class="intro">
        <div class="aisten">
            <img src="https://clipground.com/images/albert-einstein-cartoon-clipart-4.jpg" alt="Aisten" class="character" />
            <p class="message">A matemática é a base para resolver problemas e criar soluções inovadoras!</p>
        </div>
        <div class="options">
            <button @click="setCalculator('normal')">Calculadora Normal</button>
            <button @click="setCalculator('scientific')">Calculadora Científica</button>
        </div>
        </div>
    </template>
    
    <script>
    export default {
        name: 'Intro',
        methods: {
        setCalculator(type) {
            this.$emit('setCalculator', type);
        },
        },
    };
    </script>
    
    <style scoped>
    .intro {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
    
    .aisten {
        margin-bottom: 20px;
    }
    
    .character {
        width: 150px;
        height: auto;
    }
    
    .message {
        font-size: 1.2rem;
        color: #555;
        margin-top: 10px;
    }
    
    .options {
        margin-bottom: 20px;
    }
    
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
