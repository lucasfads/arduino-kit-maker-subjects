# 01 — Pisca-pisca

> Faça um LED piscar em intervalos regulares para praticar montagem básica, saída digital e temporização no Arduino.

## Objetivos de aprendizagem

- Identificar o ânodo e o cátodo de um LED.
- Montar um circuito simples com resistor limitador de corrente.
- Configurar um pino digital como saída.
- Alternar o estado de uma saída com um intervalo de tempo definido.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `01-pisca-pisca/` |
| Arquivo esperado | `pisca-pisca.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 1 LED vermelho difuso de 5 mm, 1 resistor de 220 Ω e 2 jumpers macho-macho |
| APIs esperadas | `pinMode()`, `digitalWrite()` e `delay()` |

## Parte obrigatória

Monte um circuito em que o LED vermelho seja controlado pelo pino digital `11` do Arduino.

Ao iniciar, o programa deve repetir indefinidamente este ciclo:

1. acender o LED por aproximadamente 1 segundo;
2. apagar o LED por aproximadamente 1 segundo.

O LED deve ser conectado em série com o resistor de 220 Ω. A perna longa do LED é o ânodo e deve estar no lado conectado ao pino digital; a perna curta é o cátodo e deve estar no lado conectado ao resistor e, em seguida, ao `GND`.

## Conexões obrigatórias

| Origem | Destino | Finalidade |
| --- | --- | --- |
| Pino digital `11` | Ânodo do LED | Controlar o acendimento |
| Cátodo do LED | Resistor de 220 Ω | Limitar a corrente |
| Outra perna do resistor | `GND` do Arduino | Fechar o circuito |

### Montagem de referência

As posições físicas na protoboard podem variar desde que as conexões obrigatórias sejam preservadas. Para reproduzir a disposição da folha do projeto:

| Componente | Posição |
| --- | --- |
| Jumper de terra | `GND` do Arduino → `A19` |
| Resistor de 220 Ω | `D19` → `D15` |
| LED — cátodo (perna curta) | `E15` |
| LED — ânodo (perna longa) | `E14` |
| Jumper de sinal | `A14` → pino digital `11` |

Nos blocos centrais da protoboard, os furos `A` a `E` de uma mesma linha numerada são conectados entre si. Portanto, `A19` e `D19` formam o mesmo ponto elétrico, assim como `A14` e `E14`.

## Comportamentos esperados

| Situação | Resultado esperado |
| --- | --- |
| Arduino ligado | LED inicia o ciclo de piscar |
| Durante o primeiro intervalo | LED permanece aceso por aproximadamente 1 segundo |
| Durante o segundo intervalo | LED permanece apagado por aproximadamente 1 segundo |
| Após o segundo intervalo | O ciclo recomeça sem intervenção |

## Critérios de aceite

- O sketch compila e é enviado para a placa sem erros.
- O LED acende e apaga continuamente.
- Cada estado dura aproximadamente 1 segundo.
- O LED está em série com um resistor de 220 Ω.
- O pino `11` é configurado como saída.
- A polaridade do LED e a ligação ao `GND` estão corretas.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- A tolerância visual de alguns centésimos de segundo na temporização é aceitável.
