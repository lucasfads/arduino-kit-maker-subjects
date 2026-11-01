# 11 — Dó ré mi

> Toque uma escala musical com um buzzer para praticar frequências, arrays e repetição.

## Objetivos de aprendizagem

- Produzir notas com `tone()`.
- Relacionar frequência e altura musical.
- Armazenar uma sequência em um array.
- Percorrer um array com laço de repetição.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta | `11-do-re-mi/` |
| Arquivo | `do-re-mi.ino` |
| Hardware | 1 buzzer, 1 resistor de 220 Ω e 2 jumpers |
| Pino | Buzzer em `6` |
| APIs esperadas | `tone()`, `delay()`, arrays e laços |

## Parte obrigatória

Ligue o buzzer ao pino `6` conforme a montagem e programe-o para tocar repetidamente a escala:

`Dó, Ré, Mi, Fá, Sol, Lá, Si, Dó`.

Cada nota deve durar aproximadamente 500 ms. Use as frequências correspondentes às notas e uma estrutura de dados para representar a melodia.

## Critérios de aceite

- O buzzer toca oito notas em ordem ascendente.
- Cada nota dura aproximadamente 500 ms.
- A sequência reinicia automaticamente.
- O código evita repetir manualmente a chamada de cada nota.

## Bônus (opcional)

Inclua uma pequena pausa entre as notas ou toque a escala descendente depois da ascendente.
