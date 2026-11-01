# 08 — Acionando um motor

> Controle um servomotor com um botão para praticar leitura digital, lógica de estado e posicionamento angular no Arduino.

## Objetivos de aprendizagem

- Conectar e controlar um servomotor 9g com a biblioteca `Servo`.
- Ler uma chave táctil com `INPUT_PULLUP`.
- Relacionar o acionamento do botão a um movimento observável do servo.
- Trabalhar com ângulos, laços de repetição e pequenas pausas para criar um movimento gradual.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta de entrega | `08-acionando-um-motor/` |
| Arquivo esperado | `acionando-um-motor.ino` |
| Placa | Arduino Uno ou compatível |
| Hardware obrigatório | Protoboard, 1 servomotor 9g, 1 chave táctil push button e 7 jumpers |
| Biblioteca permitida | `Servo.h` |
| APIs esperadas | `pinMode()`, `digitalRead()`, `Servo.attach()`, `Servo.write()`, `delay()` |

## Parte obrigatória

Monte o circuito e escreva um sketch que mantenha o servo em repouso na posição inicial.

Ao pressionar o botão, o servomotor deve:

1. mover-se gradualmente de `0°` até `180°`;
2. retornar gradualmente de `180°` para `0°`;
3. permanecer em `0°` ao fim do ciclo.

Use a chave com `INPUT_PULLUP`: o pino de leitura deve ficar em nível alto sem pressão e em nível baixo enquanto o botão estiver pressionado. Não é necessário usar resistor externo para a chave.

Você pode usar o botão no pino `7` e o sinal do servo no pino `9`, ou documentar outros pinos no início do sketch.

O movimento deve ser perceptivelmente gradual. Use incrementos de ângulo e uma pausa curta entre eles; não posicione o servo diretamente em `180°` e depois em `0°`.

## Comportamentos esperados

| Situação | Resultado esperado |
| --- | --- |
| Arduino ligado e botão solto | Servo parado em `0°` |
| Botão pressionado | Servo gira suavemente até `180°` e retorna suavemente a `0°` |
| Ciclo concluído | Servo permanece em repouso em `0°` |
| Nova ativação após o ciclo | O movimento completo é executado novamente |

## Critérios de aceite

- O sketch compila usando `Servo.h`.
- A chave é lida com `INPUT_PULLUP` e funciona sem resistor externo.
- O servo percorre os dois sentidos entre `0°` e `180°`.
- O movimento é gradual e visível.
- Ao final do ciclo, o servo não fica parado em uma posição intermediária.
- As ligações e os pinos usados podem ser identificados no código por comentários ou constantes com nomes claros.

## Bônus (opcional)

Implemente uma pequena máquina de estados para que uma nova pressão do botão durante o movimento não reinicie nem interrompa o ciclo atual. O próximo ciclo deve ser aceito somente depois que o servo voltar a `0°`.

## Premissas adotadas

- Este é um exercício único, de nível introdutório.
- A alimentação do servo pelo `5V` do Arduino é adequada apenas para testes de bancada leves. Se houver tremores, reinicializações ou pouca força, investigue uma fonte externa regulada com terra comum antes de alterar o código.
