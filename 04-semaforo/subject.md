# 04 — Semáforo

> Simule o ciclo coordenado de um semáforo para carros e pedestres usando cinco LEDs.

## Objetivos de aprendizagem

- Controlar múltiplas saídas digitais.
- Modelar uma sequência de estados com tempos diferentes.
- Coordenar sinais de carros e pedestres sem estados conflitantes.
- Organizar pinos e etapas do programa com nomes claros.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `04-semaforo/` |
| Arquivo esperado | `semaforo.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 2 LEDs vermelhos, 2 LEDs verdes, 1 LED amarelo, 5 resistores de 220 Ω e 11 jumpers macho-macho |
| APIs esperadas | `pinMode()`, `digitalWrite()`, `delay()` e laços de repetição |

## Parte obrigatória

Monte dois conjuntos de sinalização:

- **Carros:** LED verde, LED amarelo e LED vermelho.
- **Pedestres:** LED verde e LED vermelho.

Cada LED deve ter seu próprio resistor de 220 Ω em série e todos devem compartilhar o `GND` do Arduino.

Use este mapeamento de pinos:

| Sinal | Cor | Pino |
| --- | --- | ---: |
| Pedestres — pare | Vermelho | `8` |
| Pedestres — atravesse | Verde | `9` |
| Carros — pare | Vermelho | `10` |
| Carros — atenção | Amarelo | `11` |
| Carros — siga | Verde | `12` |

Implemente continuamente a seguinte sequência:

1. **Carros seguem:** verde dos carros e vermelho dos pedestres acesos por aproximadamente 5 segundos.
2. **Carros em atenção:** amarelo dos carros aceso por aproximadamente 3 segundos; pedestres permanecem no vermelho.
3. **Pedestres atravessam:** vermelho dos carros e verde dos pedestres acesos por aproximadamente 5 segundos.
4. **Fim da travessia:** verde dos pedestres apaga; vermelho dos pedestres pisca 5 vezes, com aproximadamente 250 ms aceso e 250 ms apagado.
5. Reinicie o ciclo, liberando os carros novamente.

## Regras de segurança lógica

- O verde dos carros e o verde dos pedestres nunca podem estar acesos ao mesmo tempo.
- Durante o amarelo dos carros, o vermelho dos pedestres deve permanecer aceso.
- Durante a travessia, o vermelho dos carros deve permanecer aceso.

## Comportamentos esperados

| Etapa | Carros | Pedestres |
| --- | --- | --- |
| 1 | Verde | Vermelho |
| 2 | Amarelo | Vermelho |
| 3 | Vermelho | Verde |
| 4 | Vermelho | Vermelho piscando |
| 5 | Reinício do ciclo | Reinício do ciclo |

## Critérios de aceite

- O sketch compila e é enviado para a placa sem erros.
- Os cinco LEDs possuem resistores individuais de 220 Ω.
- Cada sinal está conectado ao pino correspondente.
- A sequência respeita as quatro etapas e se repete automaticamente.
- Os tempos de 5 s, 3 s e os piscas de 250 ms são visualmente reconhecíveis.
- Os dois sinais verdes nunca ficam acesos juntos.
- Os pinos e as etapas da sequência têm nomes claros no código.

## Bônus (opcional)

Extraia cada etapa do ciclo para uma função com nome descritivo. O comportamento final deve continuar o mesmo, mas a sequência principal deve ficar fácil de ler.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- Pequenas variações de temporização são aceitáveis, desde que não alterem a lógica do semáforo.
