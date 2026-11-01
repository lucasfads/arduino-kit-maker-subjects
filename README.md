# Arduino Subjects

Uma trilha de desafios práticos de Arduino, escrita em português.

Cada projeto propõe um resultado observável, mas não entrega a solução. A ideia é montar o circuito, desenvolver o sketch, testar por conta própria e então usar a régua de avaliação para verificar a entrega.

## Estrutura

```text
01-nome-do-projeto/
├── subject.md  # desafio, escopo e critérios de aceite
└── review.md   # roteiro de validação e autoavaliação
```

Os projetos são numerados em ordem crescente de dificuldade e usam nomes em `kebab-case`.

## Projetos

| Nº | Projeto | Conceitos principais |
| --- | --- | --- |
| 01 | [Pisca-pisca](01-pisca-pisca/subject.md) | Saída digital, LED e temporização |
| 02 | [SOS luminoso](02-sos-luminoso/subject.md) | Código Morse, laços e temporização |
| 03 | [Brilho oscilante](03-brilho-oscilante/subject.md) | PWM, laços e transição gradual |
| 08 | [Acionando um motor](08-acionando-um-motor/subject.md) | Entrada digital, `INPUT_PULLUP` e servomotor |
| 09 | [Controlando o motor](09-controlando-o-motor/subject.md) | Entrada analógica, mapeamento e servomotor |

## Como usar

1. Leia o `subject.md` sem consultar soluções externas.
2. Monte o circuito e implemente o sketch.
3. Valide seu resultado com `review.md`.
4. Só depois consulte referências externas, se precisar comparar abordagens.

Veja [docs/setup.md](docs/setup.md) para preparar o ambiente e [docs/referencias.md](docs/referencias.md) para entender a proposta editorial dos subjects.

## Status

A trilha está em construção. Os projetos serão adicionados e revisados um a um.

## Princípios

- Aprender fazendo, com espaço para tentativa e erro.
- Avaliar comportamentos observáveis, não apenas “o código parece certo”.
- Manter os subjects autocontidos e evitar soluções prontas no repositório.
- Escrever conteúdos próprios, claros e reutilizáveis.
