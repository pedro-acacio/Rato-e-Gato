# Rato e Gato

Jogo de perseguição em [p5.js](https://p5js.org/) + [p5.play](https://p5play.molleindustria.org/): pressionar a seta esquerda troca a animação do rato e faz o gato avançar em direção a ele; quando a distância entre os dois fica pequena o bastante, ambos voltam às posições iniciais com uma animação de "pego".

## Estado do repositório

`sketch.js` carrega imagens em `preload()` (`images/garden.png`, `images/mouse1.png` a `mouse4.png`, `images/cat1.png` a `cat4.png`), mas a pasta `images/` não está neste repositório. Sem esses arquivos, `index.html` não carrega o cenário nem os sprites.

## Tecnologias

- [p5.js](https://p5js.org/) e [p5.play.js](https://p5play.molleindustria.org/) para sprites e animações
- p5.dom e p5.sound incluídos, mas não usados diretamente na lógica em `sketch.js`
- JavaScript puro, sem build

## Estrutura

- `sketch.js` — carrega imagens, cria os sprites do gato e do rato, e a lógica de movimento (seta esquerda) e colisão
- `index.html` — carrega p5.js, p5.dom, p5.play, p5.sound e o sketch
- `style.css` — estilo básico do canvas

## Como rodar

Faltam os assets em `images/` referenciados por `sketch.js`; sem recriá-los, a página abre mas o `preload()` falha. Com as imagens no lugar, basta abrir `index.html` direto no navegador ou servir a pasta com qualquer servidor estático (ex: `npx serve .`).
