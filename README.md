# Color Flipper

O Color Flipper é um projeto simples que demonstra como criar uma aplicação web que muda a cor de fundo de uma página com base em cores aleatórias.

## Funcionalidades Principais

- **Botão de Troca de Cor**: Ao clicar no botão "Trocar Cor", a cor de fundo da página será alterada para uma cor aleatória.
- **Cores Aleatórias**: O projeto utiliza o método `Math.random()` para gerar cores aleatórias e exibi-las na interface.

## Tecnologias Utilizadas

- JavaScript
- HTML
- CSS

## Instruções de Instalação e Uso

1. Clone este repositório para o seu computador:

    ```
    git@github.com:JyojiTenguam/ColorFlipper.git
    ```

2. Navegue até o diretório do projeto:

    ```
    cd ColorFlipper
    ```

3. Abra o arquivo `index.html` em seu navegador.

4. Clique no botão "Click me" para ver a cor de fundo da página mudar aleatoriamente.

## Exemplo de Código

```javascript
const colors = ["#ff0000", "#00ff00", "#0000ff", "#ffff00", "#00ffff", "#ff00ff"];

const button = document.getElementById("btn");
const body = document.body;

button.addEventListener("click", changeColor);

function changeColor() {
    // Gera um índice aleatório dentro do comprimento da array de cores
    const randomIndex = Math.floor(Math.random() * colors.length);
    // Obtém a cor correspondente ao índice aleatório
    const color = colors[randomIndex];
    // Altera a cor de fundo do corpo da página
    body.style.backgroundColor = color;
}
