# 07 — Troque a cor das luzes

> Use um potenciômetro para escolher o estado de um LED RGB a partir de faixas de leitura analógica.

## Objetivos de aprendizagem

- Ler um potenciômetro com `analogRead()`.
- Trabalhar com a faixa de valores de `0` a `1023`.
- Criar condições exclusivas para diferentes faixas numéricas.
- Combinar entradas analógicas com saídas digitais.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `07-troque-a-cor-das-luzes/` |
| Arquivo esperado | `troque-a-cor-das-luzes.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 1 LED RGB de 5 mm, 3 resistores de 220 Ω, 1 potenciômetro de 10 kΩ e 9 jumpers macho-macho |
| APIs esperadas | `analogRead()`, `digitalWrite()`, condicionais e funções próprias |

## Parte obrigatória

Use o mesmo LED RGB de ânodo comum do projeto 6: terminal comum em `5V`; canais vermelho, verde e azul com resistores próprios e ligados, respectivamente, aos pinos `7`, `6` e `5`.

Ligue o potenciômetro como divisor de tensão: os terminais externos vão para `5V` e `GND`; o terminal central vai para `A0`.

Leia continuamente o potenciômetro e aplique os estados:

| Faixa da leitura | Estado do LED |
| --- | --- |
| `0–256` | Apagado |
| `257–512` | Vermelho |
| `513–768` | Verde |
| `769–1023` | Azul |

A mudança de estado deve ocorrer enquanto o potenciômetro é girado, sem reiniciar a placa.

## Critérios de aceite

- O potenciômetro é lido pelo pino `A0`.
- O LED RGB possui três resistores de 220 Ω, um por canal.
- As quatro faixas cobrem toda a leitura de `0` a `1023` sem sobreposição.
- Cada faixa seleciona o estado de cor correto.
- O LED responde continuamente ao giro do potenciômetro.

## Bônus (opcional)

Troque as faixas discretas por uma mistura gradual das cores usando PWM, mantendo os três resistores.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- Confirme a ordem física dos terminais do seu LED RGB antes de energizar o circuito.
