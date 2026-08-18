# 💧 Sistema IoT de Monitoramento Inteligente de Água

> **Solução inteligente e em tempo real contra o desperdício, vazamentos e riscos de desabastecimento em reservatórios urbanos, comerciais e residenciais.**

---

## 📌 Problema

Comunidades, empresas e sistemas urbanos enfrentam perdas frequentes de água decorrentes de **vazamentos não detectados** e da **falta de visibilidade em tempo real** sobre:
* 📉 Nível atual dos reservatórios
* 🧪 Qualidade da água armazenada
* ⚠️ Risco iminente de desabastecimento

A ausência de dados precisos e contínuos dificulta a tomada de decisão preventiva, resultando em desperdício de recursos e prejuízos financeiros.

---

## 💡 Solução

Uma **plataforma integrada de IoT** que utiliza sensores instalados nos reservatórios para realizar medições contínuas e automatizadas de **nível, vazão e parâmetros de qualidade** (pH, turbidez e temperatura). 

Os dados coletados são transmitidos via rede sem fio para um **painel administrativo centralizado**, que oferece:
* 🔔 **Alertas Instantâneos:** Notificações automáticas em caso de anomalias (vazamentos, quedas bruscas de nível ou desvios de qualidade).
* 📊 **Previsão de Autonomia:** Cálculo preditivo do tempo restante de abastecimento com base no padrão de consumo atual.
* 📈 **Dashboard em Tempo Real:** Visualização clara através de gráficos e métricas fundamentais.

---

## 🛠️ Tecnologias Utilizadas

A arquitetura do sistema foi projetada para garantir **alta precisão, baixa latência e escalabilidade**:

| Camada | Tecnologias / Ferramentas | Descrição |
| :--- | :--- | :--- |
| **Hardware & IoT** | `ESP32` • `Sensores Ultrassônicos` • `Sensor de Fluxo` • `LoRaWAN / Wi-Fi` | Coleta de dados dos sensores de nível, vazão e parâmetros físico-químicos. |
| **Firmware** | `C++` • `Arduino IDE` • `ESP-IDF` | Programação de baixo nível para leitura, tratamento local e transmissão de dados. |
| **Mensageria IoT** | `MQTT` • `Eclipse Mosquitto` • `HiveMQ` | Protocolo leve e pub/sub para comunicação em tempo real entre dispositivos e servidor. |
| **Backend** | `Node.js` • `TypeScript` | API RESTful e gerenciador do fluxo de dados e regras de negócio. |
| **Banco de Dados** | `InfluxDB` | Banco de dados otimizado para séries temporais (*time-series*), ideal para leituras contínuas. |
| **Frontend** | `React.js` • `Tailwind CSS` • `Chart.js` / `Recharts` | Interface web moderna, responsiva e interativa com visualização de gráficos e dashboards. |

---

## 🏗️ Arquitetura do Sistema

```txt
┌────────────────┐      MQTT       ┌────────────────┐
│ Sensores &     │ ──────────────> │ Broker MQTT    │
│ ESP32          │                 │ (Mosquitto)    │
└────────────────┘                 └───────┬────────┘
                                           │
                                           ▼
┌────────────────┐   InfluxDB Query┌────────────────┐
│ Dashboard Web  │ <────────────── │ Backend API    │
│ (React + Chart)│                 │ (Node + TS)    │
└────────────────┘                 └────────────────┘
