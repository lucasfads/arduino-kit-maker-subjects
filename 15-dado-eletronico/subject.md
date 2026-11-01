# 15 — Dado eletrônico

> Use um sensor de vibração para iniciar uma animação de números aleatórios em um display de sete segmentos.

## Objetivos de aprendizagem

- Combinar o sensor tilt com o display de sete segmentos.
- Gerar valores aleatórios com `random()`.
- Criar uma animação que desacelera progressivamente.
- Reutilizar a lógica de exibição dos dígitos.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta | `15-dado-eletronico/` |
| Arquivo | `dado-eletronico.ino` |
| Hardware | 1 display de sete segmentos, 1 sensor de vibração tilt, 1 resistor de 220 Ω e 13 jumpers |
| Pino do sensor | `5` |
| APIs esperadas | `digitalRead()`, `random()`, `delay()`, `switch` e funções próprias |

## Parte obrigatória

Reutilize a montagem e o mapeamento de segmentos do projeto 14. Ligue o sensor de vibração ao pino `5`.

Ao detectar movimento, o programa deve:

1. exibir rapidamente uma sequência de dígitos aleatórios;
2. aumentar gradualmente a pausa entre cada mudança, simulando a desaceleração de um dado;
3. terminar mostrando um último dígito.

Nesta versão, a sequência pode usar os dígitos de `0` a `9`. Cada nova vibração deve iniciar uma nova rodada.

## Critérios de aceite

- O sensor tilt inicia a animação.
- A animação mostra diversos dígitos aleatórios.
- O intervalo entre as mudanças aumenta durante a rodada.
- O display fica em um dígito ao final.
- Uma nova vibração inicia outra rodada.

## Bônus (opcional)

Transforme a versão em um dado convencional: sorteie e exiba somente valores de `1` a `6`.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- O display segue a mesma configuração de ânodo comum do projeto 14.
