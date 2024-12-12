# Calculadora Aritmética e Científica

Este projeto é uma aplicação Vue.js que implementa uma **calculadora aritmética** e **científica**, com a funcionalidade de alternar entre os dois tipos de calculadora. O projeto tem como objetivo demonstrar a capacidade de manipular dados, realizar cálculos dinâmicos e tornar a interface interativa e responsiva.

## Funcionalidades

1. **Calculadora Aritmética**:
   - Permite ao usuário inserir dois números e escolher uma operação matemática (Soma, Subtração, Multiplicação ou Divisão).
   - O cálculo é realizado automaticamente assim que os valores ou a operação são alterados, sem a necessidade de clicar em um botão.

2. **Calculadora Científica**:
   - Permite ao usuário inserir um número e calcular o seu **quadrado** (x²) ou **raiz quadrada** (√x) com apenas um clique.
   - Exibe o resultado imediatamente abaixo dos botões.

## Estrutura do Projeto

### Componentização

O projeto foi dividido em componentes Vue.js para facilitar a manutenção e reutilização do código. A estrutura principal do projeto inclui:

1. **Componente Principal (`App.vue`)**:
   - Este componente é responsável por exibir a introdução, permitir a seleção entre as calculadoras (normal e científica) e gerenciar o estado global da aplicação.

2. **Calculadora Normal**:
   - Componente para realizar operações aritméticas básicas (soma, subtração, multiplicação, divisão).
   - Usa a diretiva `v-model` para vincular os valores dos inputs e do select ao estado da aplicação.
   - A operação é automaticamente calculada usando `watchers` que detectam mudanças nos valores inseridos.

3. **Calculadora Científica**:
   - Componente para realizar operações científicas como calcular o quadrado e a raiz quadrada de um número.
   - Botões para cada operação, com cálculos realizados em métodos separados.

### Tecnologias Utilizadas

- **Vue.js**: Framework JavaScript utilizado para criar a interface dinâmica e interativa.
- **HTML/CSS**: Utilizado para estruturar e estilizar a página, criando um layout responsivo e agradável.
- **Vue CLI**: Ferramenta de inicialização para gerenciar o projeto Vue.js.

