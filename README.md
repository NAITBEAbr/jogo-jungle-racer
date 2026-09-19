# Jungle Racer

Jogo de corrida para dois jogadores, em navegador. Cada jogador entra com o seu nome,
espera o segundo jogador e os dois correm pela selva ao mesmo tempo, cada um vendo a
posição do outro na pista.

## Como funciona

- O jogo usa o **Firebase Realtime Database** para sincronizar os dois jogadores: o
  estado da partida e a posição de cada um ficam salvos lá, e a tela de cada jogador
  acompanha as mudanças em tempo real
- A classe `Game` controla o estado da partida: espera, jogo em andamento e fim
- A classe `Player` guarda o nome, a distância percorrida e a posição de cada jogador
- A classe `Form` mostra o formulário de entrada e o botão de começar
- A partida só começa quando dois jogadores entram

## Tecnologias

- JavaScript
- p5.js e p5.play (desenho, sprites e animação)
- Firebase Realtime Database (partida em tempo real)

## Como executar

Por causa do carregamento das imagens, o jogo precisa de um servidor local. Com o
Python instalado:

```bash
cd Jungle-Racer-Template-main-main
python -m http.server 8000
```

Depois abra `http://localhost:8000` no navegador. Para jogar de verdade, abra em duas
abas ou em dois computadores diferentes, cada um com um nome.

Para usar seu próprio banco, crie um projeto no
[console do Firebase](https://console.firebase.google.com), ative o Realtime Database e
troque as credenciais no `index.html`.
