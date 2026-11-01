# 05 — Interruptor de luz

> Use uma chave táctil para alternar o estado de um LED, como um interruptor de parede.

## Objetivos de aprendizagem

- Ler uma entrada digital com `INPUT_PULLUP`.
- Armazenar e alternar um estado booleano.
- Distinguir o evento de pressionar do estado contínuo de manter um botão pressionado.
- Aplicar uma forma simples de debounce.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `05-interruptor-de-luz/` |
| Arquivo esperado | `interruptor-de-luz.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 1 LED vermelho de 5 mm, 1 resistor de 220 Ω, 1 chave táctil push button e 5 jumpers macho-macho |
| APIs esperadas | `pinMode()`, `digitalRead()`, `digitalWrite()` e `delay()` |

## Parte obrigatória

Monte um botão no pino digital `7` usando `INPUT_PULLUP`: um lado da chave deve ficar no pino de leitura e o outro no `GND`.

Ligue o LED vermelho ao pino digital `13`, em série com o resistor de 220 Ω e com retorno ao `GND`.

O programa deve funcionar como um interruptor:

1. começa com o LED apagado;
2. cada novo pressionamento alterna o estado do LED;
3. segurar o botão não pode alternar repetidamente;
4. para uma nova troca, o botão deve ser solto e pressionado de novo.

## Comportamentos esperados

| Ação | Resultado esperado |
| --- | --- |
| Placa é ligada | LED inicia apagado |
| Botão é pressionado uma vez | LED acende |
| Botão é solto e pressionado novamente | LED apaga |
| Botão é mantido pressionado | O estado muda somente uma vez |

## Critérios de aceite

- O botão usa `INPUT_PULLUP`, sem resistor externo.
- O LED possui resistor de 220 Ω em série.
- Cada pressionamento completo alterna o LED exatamente uma vez.
- O estado do LED é mantido entre um pressionamento e outro.
- O sketch evita acionamentos repetidos por manter o botão pressionado.

## Bônus (opcional)

Implemente o debounce sem usar `delay()`, registrando o tempo da última mudança.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- Com `INPUT_PULLUP`, botão pressionado corresponde a `LOW`.
