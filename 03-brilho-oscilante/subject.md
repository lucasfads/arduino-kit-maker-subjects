# 03 — Brilho oscilante

> Faça um LED aumentar e diminuir de brilho continuamente para praticar PWM e variação gradual de valores.

## Objetivos de aprendizagem

- Diferenciar saída digital comum de PWM.
- Usar `analogWrite()` para controlar o brilho de um LED.
- Criar transições graduais com laços de repetição.
- Usar incrementos e decrementos para percorrer uma faixa de valores.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `03-brilho-oscilante/` |
| Arquivo esperado | `brilho-oscilante.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 1 LED vermelho difuso de 5 mm, 1 resistor de 220 Ω e 2 jumpers macho-macho |
| APIs esperadas | `pinMode()`, `analogWrite()`, `delay()` e laços de repetição |

## Parte obrigatória

Use a mesma montagem elétrica dos projetos 1 e 2:

| Origem | Destino | Finalidade |
| --- | --- | --- |
| Pino digital PWM `11` | Ânodo do LED | Controlar o brilho |
| Cátodo do LED | Resistor de 220 Ω | Limitar a corrente |
| Outra perna do resistor | `GND` do Arduino | Fechar o circuito |

O pino `11` deve controlar o LED por PWM. O programa deve repetir indefinidamente este ciclo:

1. aumentar o brilho gradualmente do mínimo até o máximo;
2. diminuir o brilho gradualmente do máximo até o mínimo;
3. reiniciar o aumento de brilho.

A transição deve ser suave e perceptível. Não basta alternar o LED diretamente entre ligado e desligado.

## Comportamentos esperados

| Situação | Resultado esperado |
| --- | --- |
| Início | LED parte apagado ou com brilho muito baixo |
| Primeira fase | Brilho aumenta de forma gradual até o máximo |
| Segunda fase | Brilho diminui de forma gradual até o mínimo |
| Repetição | O ciclo de aumento e diminuição continua automaticamente |

## Critérios de aceite

- O sketch compila e é enviado para a placa sem erros.
- O LED está ligado ao pino PWM `11`, em série com um resistor de 220 Ω.
- O brilho varia entre níveis baixos e altos.
- A transição em ambos os sentidos é gradual e visível.
- O ciclo se repete continuamente.
- O código percorre valores intermediários, em vez de somente ligar e desligar o LED.

## Bônus (opcional)

Defina uma constante para controlar a velocidade da transição e outra para controlar o tamanho dos incrementos. Elas devem permitir deixar o efeito mais rápido, mais lento, mais suave ou mais abrupto sem reescrever a lógica principal.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- O pino `11` do Arduino Uno R3 suporta PWM.
