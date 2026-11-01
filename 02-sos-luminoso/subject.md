# 02 — SOS luminoso

> Use um LED para transmitir continuamente o sinal internacional de socorro SOS em código Morse.

## Objetivos de aprendizagem

- Reutilizar uma montagem com LED e resistor.
- Representar um padrão de comunicação por uma sequência de saídas digitais.
- Usar laços de repetição para evitar código redundante.
- Controlar diferentes durações com `delay()`.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `02-sos-luminoso/` |
| Arquivo esperado | `sos-luminoso.ino` |
| Placa | Arduino Uno R3 ou compatível |
| Hardware obrigatório | 1 LED vermelho difuso de 5 mm, 1 resistor de 220 Ω e 2 jumpers macho-macho |
| APIs esperadas | `pinMode()`, `digitalWrite()`, `delay()` e laços de repetição |

## Parte obrigatória

Use a mesma montagem elétrica do projeto anterior:

| Origem | Destino | Finalidade |
| --- | --- | --- |
| Pino digital `11` | Ânodo do LED | Controlar o acendimento |
| Cátodo do LED | Resistor de 220 Ω | Limitar a corrente |
| Outra perna do resistor | `GND` do Arduino | Fechar o circuito |

O programa deve emitir repetidamente o sinal Morse `SOS`:

```text
... --- ...
```

- Cada ponto é um flash curto, de aproximadamente 150 ms.
- Cada traço é um flash longo, de aproximadamente 450 ms.
- Um ponto ou traço deve ser seguido por um curto período com o LED apagado.
- Deve haver uma pausa visível entre o primeiro `S`, o `O` e o último `S`.
- Ao final da mensagem, aguarde alguns segundos antes de reiniciar a transmissão.

## Comportamentos esperados

| Etapa | Resultado esperado |
| --- | --- |
| Primeiro `S` | Três flashes curtos |
| `O` | Três flashes longos |
| Último `S` | Três flashes curtos |
| Fim da mensagem | LED apagado por alguns segundos antes de reiniciar |
| Repetição | O padrão inteiro recomeça automaticamente |

## Critérios de aceite

- O sketch compila e é enviado para a placa sem erros.
- O LED está em série com um resistor de 220 Ω e ligado ao pino `11`.
- A sequência `... --- ...` é visualmente reconhecível.
- Os traços duram aproximadamente três vezes o tempo dos pontos.
- Há pausas entre os grupos da mensagem e antes de sua repetição.
- O código evita repetição desnecessária na criação dos três flashes de cada grupo.

## Bônus (opcional)

Permita escolher, por uma constante no início do sketch, a unidade de tempo do Morse. A duração de pontos, traços e pausas deve se adaptar proporcionalmente.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- Variações pequenas nas durações são aceitáveis desde que a diferença visual entre ponto e traço fique clara.
