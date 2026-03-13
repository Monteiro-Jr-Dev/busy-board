# Busy Board — Arthur 🎛️

Painel interativo (*busy board*) construído com Arduino para meu sobrinho Arthur (Tutu), de 2 anos. O painel combina elementos visuais, sonoros e físicos para estimular a coordenação motora e a curiosidade da criança.

> Confira o timelapse do processo de construção no [Instagram](https://www.instagram.com/p/C8vp7LLtqyC/).

---

## Funcionalidades

| Componente | Descrição |
|---|---|
| **LED Chaser** | 24 LEDs controlados por registradores de deslocamento 74HC595, com 13 padrões de animação sorteados aleatoriamente |
| **Botões Musicais** | Botões que acionam sequências de notas musicais |
| **Controle de Hélice** | Ventilador com velocidade ajustada por potenciômetro e lógica de partida |
| **Campainha** | Campainha acionada com sinal 12V alternado, criado com ponte H a partir de 12V CC. |
| **Display OLED** | Tela SSD1306 128×64 que exibe animações de sprite e o nome "Painel de Tutu" |
| **Chave Seletora** | Chave que troca o padrão do LED chaser e a animação do display |

---

## Hardware

- Arduino (Uno/Nano ou compatível)
- Display OLED SSD1306 (I²C, 128×64)
- 3× Registrador de deslocamento 74HC595
- 24 LEDs
- Potenciômetro
- Motor DC (hélice/ventilador)
- Buzzer passivo
- Botões de pressão
- Chave seletora

## Software / Bibliotecas

- [Adafruit GFX Library](https://github.com/adafruit/Adafruit-GFX-Library)
- [Adafruit SSD1306](https://github.com/adafruit/Adafruit_SSD1306)

---

## Mapeamento de Pinos

| Pino | Função |
|------|--------|
| D0, D1 | Campainha |
| D2 | Data — LED Chaser |
| D3 | Ventilador (PWM OUT) |
| D4 | Chave seletora |
| D5 | Clock — 74HC595 |
| D6 | Data — Musical |
| D7 | Latch — Musical |
| D8 | Latch — Chaser |
| A0 | Potenciômetro do ventilador |
