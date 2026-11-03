# Preparação do ambiente

## Componentes sugeridos

A lista abaixo representa um conjunto recomendado para percorrer a trilha inteira. As quantidades são o **estoque total sugerido**, não a quantidade exigida por desafio: cada `subject.md` informa apenas os componentes que devem ser usados naquele projeto.

| Componente | Quantidade sugerida |
| --- | ---: |
| Arduino Uno R3 ou placa compatível | 1 |
| Protoboard de 400 pontos | 1 |
| LED difuso vermelho de 5 mm | 10 |
| LED difuso verde de 5 mm | 10 |
| LED difuso amarelo de 5 mm | 10 |
| Resistor de 220 Ω | 20 |
| Resistor de 10 kΩ | 20 |
| Display de sete segmentos | 1 |
| Cabo USB compatível com a placa | 1 |
| Potenciômetro linear de 10 kΩ | 1 |
| LED RGB difuso de 5 mm | 1 |
| Sensor de luminosidade (LDR) | 1 |
| Micro servo 9g | 1 |
| Jumper macho-macho | 40 |
| Chave táctil push button | 10 |
| Sensor de vibração tilt | 1 |
| Buzzer ativo de 5V | 1 |
| Diodo laser de 5V | 1 |

Você não precisa usar todos os itens em todos os exercícios. Ter unidades extras de LEDs, resistores, jumpers e botões é útil para montar circuitos diferentes e substituir peças eventualmente danificadas.

## Segurança e montagem

Antes de energizar o circuito:

- confira se `5V` e `GND` não estão em curto;
- confira a polaridade de LEDs e outros componentes polarizados;
- desconecte o Arduino do USB antes de alterar uma montagem;
- use uma fonte externa regulada com terra comum se um componente exigir mais corrente do que o Arduino pode fornecer com segurança.

## Software e simuladores

Você pode escolher um ambiente físico ou virtual:

- **Arduino IDE**, para começar rapidamente com sketches em C++;
- **PlatformIO**, se já usa VS Code e quer um fluxo mais próximo do desenvolvimento de software;
- **[Tinkercad Circuits](https://www.tinkercad.com/circuits)**, para montar e simular circuitos no navegador, inclusive com lógica em blocos;
- **[Wokwi](https://wokwi.com/arduino)**, para escrever sketches e simular Arduino no navegador.

Nos simuladores, você não precisa ter placa, cabo USB ou componentes físicos. Eles são uma boa forma de experimentar antes de montar o circuito real. Para usar Arduino IDE ou PlatformIO, selecione a placa correta — normalmente **Arduino Uno** — e a porta serial correspondente antes de enviar um sketch.

## Fluxo sugerido

1. Leia o subject por inteiro.
2. Separe e identifique os componentes.
3. Monte o circuito com o Arduino desconectado ou reproduza-o no simulador.
4. Escreva e envie o sketch — ou comece com blocos no Tinkercad e examine o código equivalente.
5. Teste os cenários do subject.
6. Use o arquivo `review.md` somente após a primeira tentativa.
