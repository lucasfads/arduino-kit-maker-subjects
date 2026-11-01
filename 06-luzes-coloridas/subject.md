# 06 — Luzes coloridas

> Controle as três cores de um LED RGB e apresente uma sequência de vermelho, verde, azul e apagado.

## Objetivos de aprendizagem

- Identificar os canais de um LED RGB.
- Controlar três saídas digitais de forma coordenada.
- Entender a diferença entre LED RGB de ânodo comum e cátodo comum.
- Organizar comportamentos repetidos em funções descritivas.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `06-luzes-coloridas/` |
| Arquivo esperado | `luzes-coloridas.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 1 LED RGB de 5 mm, 3 resistores de 220 Ω e 5 jumpers macho-macho |
| APIs esperadas | `pinMode()`, `digitalWrite()`, `delay()` e funções próprias |

## Parte obrigatória

Monte o LED RGB como **ânodo comum**: o terminal comum vai ao `5V`; cada canal de cor deve ter seu próprio resistor de 220 Ω e ser controlado por um pino digital.

| Canal | Pino |
| --- | ---: |
| Vermelho | `7` |
| Verde | `6` |
| Azul | `5` |

Para LED de ânodo comum, `LOW` acende um canal e `HIGH` o apaga.

Repita indefinidamente a sequência abaixo, mantendo cada estado por aproximadamente 1 segundo:

1. vermelho;
2. verde;
3. azul;
4. apagado.

## Critérios de aceite

- O LED RGB possui um resistor de 220 Ω por canal de cor.
- Cada cor é exibida isoladamente.
- A sequência ocorre na ordem vermelho, verde, azul e apagado.
- Cada estado fica visível por aproximadamente 1 segundo.
- O código deixa clara a intenção de acender cada cor e apagar o LED.

## Bônus (opcional)

Inclua também amarelo, ciano, magenta e branco, com uma sequência que não acenda nenhum canal sem resistor.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- Confirme o pinout do seu LED RGB; a ordem física dos terminais pode variar.
