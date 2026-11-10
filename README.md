# aim_duelo

Duelo 1v1 estilo CS que roda no navegador. Um arquivo só (`index.html`), arena ensolarada de caixas azuis no espírito do aim_map, rodadas como no CS e velocidade de movimento do Valorant.

## Como jogar com seu parceiro

1. Abra o jogo pelo GitHub Pages (ou abra o `index.html` direto no Chrome).
2. Os dois digitam o **mesmo código de sala** e clicam em **Entrar na sala 1v1**.
3. Quem entrar primeiro cria a sala e vira o juiz das rodadas. Quando o segundo conecta, a partida começa sozinha.

A conexão é direta entre os dois navegadores (WebRTC via PeerJS). O servidor público do PeerJS só faz o pareamento; o jogo em si não passa por servidor. Algumas redes corporativas bloqueiam conexão direta. Se não conectar em 15 segundos, testem fora da VPN ou em outra rede.

Sem parceiro? Use **Treinar contra bot** (fácil, médio ou difícil).

## Mapas

Todos são simétricos (girados 180°), com chão branco e uma parede na frente de cada base, então ninguém nasce vendo o outro. Lado e ponto de nascimento são sorteados a cada rodada.

| Mapa | Cor | O que tem |
|---|---|---|
| Caixas | azul | Arena aberta cheia de caixas |
| Pátio | amarelo | Praça elevada no centro, com rampa saindo de cada base |
| Torres | verde | Uma torre ao lado de cada base, com rampa vindo do meio |
| Ponte | roxo | Ponte elevada no meio; dá para passar por baixo |
| Fortes | laranja | Cada base fica num forte elevado, com duas rampas descendo |
| Rotação | — | Sorteia um mapa diferente a cada rodada |

Vale o mapa escolhido por quem criou a sala.

## Regras

- Primeiro a 10 rodadas vence (dá para mudar para 5, 8, 13 ou 16).
- 3 s de freeze no começo de cada rodada. Rodada acaba na primeira morte.
- Se o tempo acabar, vence quem tiver mais vida.
- 100 de vida, sem colete. Cabeça leva 4x. Na AK e na Deagle, corpo e pernas levam o mesmo dano.
- Lado e ponto de nascimento são sorteados a cada rodada.

| Arma | Corpo | Cabeça | Velocidade |
|---|---|---|---|
| AK-47 (1) | 27 | 144 | 5,4 m/s |
| Desert Eagle (2) | 40 | 212 | 5,73 m/s |
| Faca (3) | 40 / 65 | — | 6,75 m/s |
| AWP (4) | 115 | 460 | 5,13 m/s |

O movimento tem inércia como no Valorant: trocar de A para D perde velocidade, e soltar as teclas para o boneco quase na hora (não precisa de contra-strafe). Andar com Shift fica em 55% da velocidade e não faz barulho de passo. Agachado fica em 40%. Atirar correndo ou no ar é impreciso; parado ou agachado é preciso, como no CS. A AK tem padrão de spray.

## Controles

| Tecla | Ação |
|---|---|
| WASD | Mover |
| Shift | Andar devagar (sem passos) |
| C | Agachar (no ar, encolhe as pernas para subir nas caixas) |
| Espaço | Pular |
| Mouse 1 | Atirar |
| Mouse 2 | Luneta da AWP / golpe forte da faca |
| 1 2 3 4 | AK, Deagle, Faca, AWP |
| Q / rodinha | Última arma / trocar arma |
| R | Recarregar |
| Tab | Placar |
| Esc | Menu e configurações |

## Configurações

- **Cor do boneco:** escolha antes de entrar na sala. É a cor que o oponente vê.

- **Mira:** estilo estático ou dinâmico, cor, tamanho, espessura, espaço, contorno, ponto central, formato T, opacidade.
- **Mouse:** sensibilidade na escala do CS (mostra o equivalente no Valorant e os cm/360 pelo seu DPI) e sensibilidade da luneta.
- **Vídeo:** FOV (horizontal 4:3, igual ao CS), escala de resolução para PC fraco, contador de FPS.

Tudo fica salvo no navegador.

## Publicar no GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch `main`, pasta `/ (root)`.
