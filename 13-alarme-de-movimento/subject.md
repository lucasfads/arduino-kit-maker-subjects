# 13 — Alarme de movimento

> Use um sensor de vibração para detectar movimento e disparar um buzzer.

## Objetivos de aprendizagem

- Ler um sensor digital de vibração.
- Configurar e interpretar uma entrada digital.
- Acionar um buzzer em resposta a um evento físico.
- Ajustar a sensibilidade do módulo de tilt.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta | `13-alarme-de-movimento/` |
| Arquivo | `alarme-de-movimento.ino` |
| Hardware | 1 buzzer, 1 sensor de vibração tilt com chave de ajuste e 7 jumpers |
| Pinos | Sensor em `7`; buzzer em `6` |
| APIs esperadas | `digitalRead()`, `tone()`, `noTone()` e `delay()` |

## Parte obrigatória

Ligue o sensor de vibração ao pino `7` e ajuste sua sensibilidade. Quando a leitura indicar movimento, toque um alarme de aproximadamente 440 Hz por cerca de 1 segundo. Sem movimento, o buzzer deve ficar desligado.

## Critérios de aceite

- O buzzer permanece desligado enquanto o sensor está estável.
- Uma vibração ou movimento dispara o alarme.
- O tom dura aproximadamente 1 segundo.
- A sensibilidade é ajustável pela chave do módulo.

## Bônus (opcional)

Faça o tom variar conforme a quantidade ou duração das detecções.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- A lógica de saída do módulo pode variar; confirme seu LED indicador antes de definir a condição ativa.
