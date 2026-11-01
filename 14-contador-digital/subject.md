# 14 — Contador digital

> Exiba uma contagem de 0 a 9 em um display de sete segmentos.

## Objetivos de aprendizagem

- Identificar os segmentos A a G de um display.
- Controlar sete saídas digitais.
- Criar representações de dígitos.
- Organizar um comportamento repetitivo em funções.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta | `14-contador-digital/` |
| Arquivo | `contador-digital.ino` |
| Hardware | 1 display de sete segmentos, 1 resistor de 220 Ω e 9 jumpers |
| APIs esperadas | `pinMode()`, `digitalWrite()`, `delay()` e funções próprias |

## Parte obrigatória

Monte o display conforme o diagrama e programe a contagem contínua de `0` a `9`. Cada dígito deve permanecer visível por aproximadamente 1 segundo antes de passar ao próximo.

Use o seguinte mapeamento: segmentos E, D, C, B, A, F e G nos pinos 7, 8, 9, 13, 12, 11 e 10, respectivamente. Para o display usado nesta montagem, `LOW` acende um segmento.

## Critérios de aceite

- Todos os dígitos de 0 a 9 são reconhecíveis.
- Cada dígito permanece cerca de 1 segundo.
- A sequência recomeça após o 9.
- Os sete segmentos usam o mapeamento definido.
- O resistor está no terminal comum do display.

## Bônus (opcional)

Conte de 9 para 0 após chegar ao 9.
