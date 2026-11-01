# 10 — Sensor de luz ambiente

> Leia a intensidade de luz com um LDR e use esse valor para controlar um LED.

## Objetivos de aprendizagem

- Montar um divisor de tensão com LDR e resistor.
- Ler uma entrada analógica com `analogRead()`.
- Comparar uma leitura com um limiar.
- Automatizar uma saída digital a partir de um sensor.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta | `10-sensor-de-luz-ambiente/` |
| Arquivo | `sensor-de-luz-ambiente.ino` |
| Hardware | 1 LED vermelho de 5 mm, 1 LDR, 1 resistor de 220 Ω, 1 resistor de 10 kΩ e 7 jumpers |
| Pinos | LDR em `A0`; LED em `13` |
| APIs esperadas | `analogRead()`, `digitalWrite()` e condicionais |

## Parte obrigatória

Monte o LDR em conjunto com o resistor de 10 kΩ como divisor de tensão, com o ponto de leitura conectado a `A0`. Ligue o LED ao pino `13`, em série com um resistor de 220 Ω.

Leia o sensor continuamente. Quando a leitura for igual ou superior a `750`, acenda o LED; abaixo desse limite, apague-o.

## Critérios de aceite

- O LED responde a mudanças de luz no LDR.
- A leitura é feita por `A0`.
- O código usa um limiar de `750`.
- LED e LDR estão ligados com os resistores corretos.

## Bônus (opcional)

Exiba a leitura no Monitor Serial para facilitar a calibração do limiar.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- A leitura pode variar com a iluminação do ambiente; o limiar pode exigir ajuste em outra montagem.
