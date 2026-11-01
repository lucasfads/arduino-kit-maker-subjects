# Régua de avaliação — 03 — Brilho oscilante

Use este roteiro depois da sua primeira tentativa. Ele serve para validar o comportamento e a montagem, não para comparar sua implementação com uma solução específica.

## Pré-checagem

- [ ] A montagem elétrica é a mesma dos projetos anteriores: pino `11` → LED → resistor → `GND`.
- [ ] O LED está com a polaridade correta.
- [ ] O pino escolhido suporta PWM.
- [ ] O sketch compila e é enviado para a placa sem erros.

## Cenários de validação

| Cenário | Como testar | Resultado esperado | Status |
| --- | --- | --- | :---: |
| Brilho baixo | Ligue a placa e observe o início do ciclo. | LED está apagado ou quase apagado. | ☐ |
| Aumento | Observe a primeira metade do ciclo. | Brilho aumenta gradualmente até o máximo. | ☐ |
| Redução | Observe a segunda metade do ciclo. | Brilho diminui gradualmente até o mínimo. | ☐ |
| Repetição | Aguarde mais de um ciclo. | O efeito continua sem interrupção. | ☐ |

## Avaliação

| Critério | OK | Parcial | Não atende |
| --- | :---: | :---: | :---: |
| Montagem correta e segura | ☐ | ☐ | ☐ |
| Uso de pino compatível com PWM | ☐ | ☐ | ☐ |
| Variação gradual para aumentar o brilho | ☐ | ☐ | ☐ |
| Variação gradual para reduzir o brilho | ☐ | ☐ | ☐ |
| Código com valores intermediários | ☐ | ☐ | ☐ |

## Erros comuns a investigar

- O LED apenas pisca: confirme que está usando `analogWrite()`, não somente `digitalWrite()`.
- O brilho não parece mudar: use um pino PWM e verifique se há valores intermediários.
- A transição é rápida demais: ajuste o tamanho dos incrementos ou a pausa entre atualizações.

## Conclusão

- [ ] A entrega atende à parte obrigatória.
- [ ] Registrei o que ainda preciso corrigir ou entender.
