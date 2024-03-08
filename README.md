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
    git clone https://github.com/seu-usuario/color-flipper.git
    ```

2. Navegue até o diretório do projeto:

    ```
    cd color-flipper
    ```

3. Abra o arquivo `index.html` em seu navegador.

4. Clique no botão "Trocar Cor" para ver a cor de fundo da página mudar aleatoriamente.

## Exemplo de Código

```javascript
const hex = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, "A", "B", "C", "D", "E", "F"];

const btn = document.getElementById("btn");
const color = document.querySelector(".color");

btn.addEventListener('click', function () {
  let hexColor = "#";
  for(let index = 0; index < 6; index++){
    hexColor += hex[getRandomNumber()];
  }
  color.textContent = hexColor;
  document.body.style.background = hexColor;
});

function getRandomNumber(){
  return Math.floor(Math.random() * hex.length);
}
