# 📡 EchoScan32: Sistema de Varredura e Detecção de Obstáculos com ESP32

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![C++](https://img.shields.io/badge/Language-C%2B%2B-blue.svg)](https://isocpp.org/)
[![ESP32](https://img.shields.io/badge/Hardware-ESP32-red.svg)](https://www.espressif.com/)
[![Wokwi Simulator](https://img.shields.io/badge/Simulation-Wokwi-green.svg)](https://wokwi.com/)

O **EchoScan32** é um projeto de sistema embarcado de controle de radar autônomo projetado para robôs móveis. Utilizando o microcontrolador **ESP32**, um sensor ultrassônico **HC-SR04** montado sobre um **servo motor SG90**, o sistema realiza uma varredura angular contínua de 0° a 180°, processando distâncias em tempo real e ativando um sistema de alerta áudio-visual para impedimentos em um raio crítico.

---

## 🎯 Objetivos do Projeto

- **Monitoramento em Tempo Real:** Mapear obstáculos em um raio de até 400 cm em múltiplos ângulos de varredura.
- **Sinalização Ativa:** Ativar alarme sonoro (Buzzer) e sinalização luminosa (LED) quando a distância for inferior a **20 cm**.
- **Envio de Dados Telemétricos:** Transmitir leituras estruturadas via comunicação Serial (`115200 baud`) para uso em monitores de telemetria e gráficos.
- **Arquitetura Modular:** Código em C++ estruturado para fácil integração com controladores de motores de tração (robôs diferenciais/omnidirecionais).

---

## 🛠️ Hardware & Componentes Simulados

| Componente | Função no Sistema | Pino no ESP32 |
| :--- | :--- | :--- |
| **ESP32 DevKit v1** | Unidade de Processamento Central | N/A |
| **Sensor Ultrassônico HC-SR04** | Medição de distância por pulso sonoro | `TRIG: GPIO 5` / `ECHO: GPIO 18` |
| **Servo Motor SG90** | Controle de rotação do radar (0° - 180°) | `PWM: GPIO 19` |
| **Buzzer Passivo** | Alerta sonoro de emergência | `GPIO 21` |
| **LED Vermelho + Resistor 220Ω** | Sinalização visual de obstáculo próximo | `GPIO 2` |

---

## 💻 Diagrama de Circuito & Simulação

O projeto foi totalmente projetado e validado no simulador online **Wokwi**.

🔗 **[Clique aqui para abrir a simulação interativa no Wokwi](SEU_LINK_DO_WOKWI_AQUI)**

> *Dica: Insira um GIF ou imagem da sua simulação rodando nesta seção para tornar o repositório ainda mais visual!*

---

## 🚀 Como Executar o Código

### Pré-requisitos

1. **Placa ou Simulador:** Placa ESP32 física ou acesso ao [Wokwi](https://wokwi.com).
2. **Ambiente de Desenvolvimento:** Arduino IDE 2.x ou extensão PlatformIO no VS Code.
3. **Bibliotecas Necessárias:**
   - `ESP32Servo` (por Kevin Harrington)

### Passo a Passo (Arduino IDE)

1. Clone este repositório no seu computador:
   ```bash
   git clone [https://github.com/SEU-USUARIO/echoscan-esp32-radar.git](https://github.com/SEU-USUARIO/echoscan-esp32-radar.git)
