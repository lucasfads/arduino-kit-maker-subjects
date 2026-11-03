# Arduino Subjects

Uma trilha de desafios práticos de Arduino, escrita em português e organizada para aprendizado baseado em projetos (*Project-Based Learning*, PBL).

A proposta é aprender construindo: cada projeto define um circuito e um comportamento observável, mas não entrega a solução. Monte, desenvolva o sketch, teste por conta própria e use a régua de avaliação para validar sua entrega.

Os desafios privilegiam componentes comuns, fáceis de encontrar e de baixo custo. Um kit físico é recomendável, mas não obrigatório.

## Estrutura

```text
01-nome-do-projeto/
├── subject.md
├── review.md
├── diagram.json
└── assets/
    └── circuito.png
```

Os projetos são numerados em ordem crescente de dificuldade e usam nomes em `kebab-case`.

## Projetos

| Nº | Projeto | Conceitos principais |
| --- | --- | --- |
| 01 | [Pisca-pisca](01-pisca-pisca/subject.md) | Saída digital e temporização |
| 02 | [SOS luminoso](02-sos-luminoso/subject.md) | Código Morse e laços |
| 03 | [Brilho oscilante](03-brilho-oscilante/subject.md) | PWM |
| 04 | [Semáforo](04-semaforo/subject.md) | Múltiplas saídas |
| 05 | [Interruptor de luz](05-interruptor-de-luz/subject.md) | Entrada digital e estado |
| 06 | [Luzes coloridas](06-luzes-coloridas/subject.md) | LED RGB |
| 07 | [Troque a cor das luzes](07-troque-a-cor-das-luzes/subject.md) | Entrada analógica |
| 08 | [Acionando um motor](08-acionando-um-motor/subject.md) | Botão e servomotor |
| 09 | [Controlando o motor](09-controlando-o-motor/subject.md) | Potenciômetro e servomotor |
| 10 | [Sensor de luz ambiente](10-sensor-de-luz-ambiente/subject.md) | LDR |
| 11 | [Dó ré mi](11-do-re-mi/subject.md) | Buzzer e frequências |
| 12 | [Alarme com sensor a laser](12-alarme-com-sensor-a-laser/subject.md) | LDR, laser e alarme |
| 13 | [Alarme de movimento](13-alarme-de-movimento/subject.md) | Sensor tilt |
| 14 | [Contador digital](14-contador-digital/subject.md) | Display de sete segmentos |
| 15 | [Dado eletrônico](15-dado-eletronico/subject.md) | Aleatoriedade e display |

## Como usar

1. Leia o `subject.md` sem consultar soluções externas.
2. Monte o circuito e implemente o sketch.
3. Valide seu resultado com `review.md`.

Veja [docs/setup.md](docs/setup.md) para preparar o ambiente.

## Programação

Os sketches dos desafios usam a linguagem do ecossistema Arduino, baseada em C++. Ter noções básicas de lógica e programação ajuda, mas não é necessário dominar C++ para começar.

Há dois caminhos possíveis:

- **Código:** use a Arduino IDE, VS Code ou Wokwi para escrever e executar o sketch.
- **Blocos:** no Tinkercad Circuits, você pode montar a lógica por blocos de arrastar e soltar e consultar o código equivalente, avançando gradualmente para a programação em texto.

## Sem um kit físico?

Você pode começar pelos simuladores online e gratuitos:

- [Tinkercad Circuits](https://www.tinkercad.com/circuits)
- [Wokwi](https://wokwi.com/arduino)

## Diagramas dos circuitos

Cada projeto inclui uma imagem de referência em `assets/circuito.png` e um arquivo `diagram.json` editável. Eles representam uma possível montagem: outras disposições na protoboard também são válidas quando preservam as conexões, polaridades e o comportamento esperado.

Os diagramas foram criados com o [Arduino Diagram Alchemist](https://lucasfads.github.io/arduino-diagram-alchemist/). O código da ferramenta está disponível em [lucasfads/arduino-diagram-alchemist](https://github.com/lucasfads/arduino-diagram-alchemist).

## Referências

Consulte [docs/referencias.md](docs/referencias.md) para o contexto dos materiais públicos usados como referência técnica.
