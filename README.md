# Multitênis

Jogo de tênis para dois jogadores no mesmo teclado, escrito em C com a biblioteca
[Allegro 5](https://liballeg.org/). A diferença para o tênis comum: várias bolas ficam em jogo ao
mesmo tempo.

## Regras

- A partida começa sem bolas. A cada 5 segundos, um dos quatro canhões nos cantos da quadra lança
  uma bola nova, com velocidade e tamanho aleatórios, até o limite de 20.
- As paredes laterais são sólidas: a bola ricocheteia e volta para a quadra.
- Cada jogador fica na própria metade. Quando uma bola passa pelo fundo da quadra de um jogador, o
  adversário marca 1 ponto.
- Vence quem chegar a 10 pontos primeiro.

## Controles

| | Jogador 1 (azul, em cima) | Jogador 2 (vermelho, embaixo) |
|---|---|---|
| Mover | `W` `A` `S` `D` | Setas |
| Rebater | `Espaço` | `Enter` do teclado numérico |

A raquete só rebate enquanto a tecla de rebater estiver pressionada.

## Placar e histórico

- `historico.txt` recebe, ao fim de cada partida, a data, a hora e os pontos dos dois jogadores.
- `npartida.txt` guarda o placar geral de vitórias (`vitórias_do_J1 vitórias_do_J2`), mostrado na
  tela final. O arquivo precisa existir para o jogo abrir.

## Como compilar

O `Makefile` é para Windows com MinGW 4.7.0 e Allegro 5.0.10 (monolith) instalado em
`C:\allegro-5.0.10-mingw-4.7.0`. Para outro caminho ou outra versão, ajuste as variáveis no topo do
arquivo.

```bash
mingw32-make
multitenis.exe
```

O jogo carrega a fonte `arial.ttf` da pasta onde roda. Ela não está no repositório: copie-a de
`C:\Windows\Fonts` para cá antes de jogar.

## Documentação

[Instruções do Jogo.pdf](Instruções%20do%20Jogo.pdf) traz as regras, uma imagem da tela e a
descrição do código, trecho a trecho.

Projeto de Leonardo D'avila Teixeira Soares, do curso de Engenharia de Controle e Automação da UFMG.
