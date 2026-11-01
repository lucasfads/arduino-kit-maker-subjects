# 09 — Controlando o motor

> Use um potenciômetro para definir, em tempo real, a posição de um servomotor 9g.

## Objetivos de aprendizagem

- Ler um sinal analógico com `analogRead()`.
- Compreender a faixa de leitura analógica do Arduino (`0` a `1023`).
- Converter essa faixa para ângulos de servo (`0°` a `180°`).
- Controlar continuamente um servomotor com a biblioteca `Servo`.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `09-controlando-o-motor/` |
| Arquivo esperado | `controlando-o-motor.ino` |
| Placa | Arduino Uno ou compatível |
| Hardware obrigatório | Protoboard, 1 servomotor 9g, 1 potenciômetro de 10 kΩ e 8 jumpers |
| Biblioteca permitida | `Servo.h` |
| APIs esperadas | `analogRead()`, `map()`, `Servo.attach()`, `Servo.write()` |

## Parte obrigatória

Monte o circuito e escreva um sketch que controle diretamente a posição do servomotor pela rotação do potenciômetro.

O potenciômetro deve ser ligado como divisor de tensão: os pinos externos vão para `5V` e `GND`, e o pino central vai para uma entrada analógica do Arduino. Você pode usar `A0` para essa leitura e o pino digital `9` para o sinal do servo, ou documentar outros pinos no início do sketch.

O programa deve ler o valor analógico do potenciômetro, convertê-lo da faixa de `0` a `1023` para a faixa de `0°` a `180°` e usar o resultado para posicionar o servo. A resposta deve ocorrer continuamente enquanto o potenciômetro é girado.

## Comportamentos esperados

| Situação | Resultado esperado |
| --- | --- |
| Potenciômetro na posição mínima | Servo próximo de `0°` |
| Potenciômetro na posição intermediária | Servo próximo de `90°` |
| Potenciômetro na posição máxima | Servo próximo de `180°` |
| Potenciômetro girado lentamente | Servo acompanha a mudança de posição sem precisar reiniciar a placa |

Não é obrigatório que os extremos físicos do potenciômetro coincidam perfeitamente com `0°` e `180°`, mas os três estados devem respeitar a relação esperada entre a rotação e o ângulo.

## Critérios de aceite

- O sketch compila usando `Servo.h`.
- O potenciômetro é lido por uma entrada analógica.
- A leitura é convertida da faixa `0–1023` para `0–180` antes de controlar o servo.
- O servo responde continuamente à rotação do potenciômetro.
- O código identifica de forma clara os pinos usados e o valor lido.
- As ligações de `5V` e `GND` estão corretas para o potenciômetro e o servo.

## Bônus (opcional)

Reduza pequenos tremores do servo sem perder uma resposta natural ao giro do potenciômetro. Documente, em um comentário curto, qual estratégia foi usada e por que ela ajuda.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- A alimentação do servo pelo `5V` do Arduino é adequada apenas para testes de bancada leves. Se houver tremores, reinicializações ou pouca força, investigue uma fonte externa regulada com terra comum antes de alterar o código.
