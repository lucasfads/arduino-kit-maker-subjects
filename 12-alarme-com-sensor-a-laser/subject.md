# 12 — Alarme com sensor a laser

> Detecte a interrupção de um feixe de luz e acione um alarme sonoro.

## Objetivos de aprendizagem

- Reaplicar a leitura analógica de um LDR.
- Combinar sensor, atuador e limiar.
- Controlar o buzzer com `tone()` e `noTone()`.
- Entender o conceito de alarme por interrupção de feixe.

## Entrega

| Item | Definição |
| --- | --- |
| Pasta | `12-alarme-com-sensor-a-laser/` |
| Arquivo | `alarme-com-sensor-a-laser.ino` |
| Hardware | 1 buzzer, 1 diodo laser de 5 V, 1 LDR, 1 resistor de 10 kΩ, 1 resistor de 220 Ω e 9 jumpers |
| Pinos | LDR em `A0`; buzzer em `6` |
| APIs esperadas | `analogRead()`, `tone()`, `noTone()` e condicionais |

## Parte obrigatória

Posicione o laser para iluminar diretamente o LDR. Leia o LDR em `A0` e mantenha o buzzer silencioso enquanto a leitura for igual ou superior a `950`.

Quando o feixe for bloqueado e a leitura cair abaixo de `950`, o buzzer deve emitir um tom de aproximadamente 440 Hz. O alarme deve parar assim que o feixe voltar a atingir o sensor.

## Critérios de aceite

- O buzzer permanece silencioso com o feixe livre.
- Cobrir o LDR ou interromper o laser aciona o alarme.
- Restaurar o feixe interrompe o som.
- A leitura do LDR e o limiar são usados no código.

## Bônus (opcional)

Adicione um LED que indique visualmente o estado de alarme.

## Segurança

Nunca aponte o laser para olhos, pessoas ou superfícies refletivas na altura dos olhos.
