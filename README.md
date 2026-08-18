💧 Gestão Hídrica Inteligente para Escola Técnica
Monitoramento em tempo real do pivô de irrigação, da piscicultura e do consumo de água da escola.

📌 O Problema
🌾 Pivô de Irrigação: Risco de irrigar demais, gastando água e energia sem necessidade.

🐟 Piscicultura: Variações na água (pH e temperatura) que podem matar os peixes.

🏫 Uso Escolar: Vazamentos, transbordamento de caixas d'água e falta de água nos horários de pico.

💡 A Solução
Um painel único no computador ou celular que recebe dados de sensores espalhados pela escola:

No Pivô: Liga a irrigação automaticamente apenas quando o solo estiver seco.

Na Piscicultura: Mede pH, temperatura e turbidez da água, enviando alertas antes de afetar os peixes.

Na Escola: Controla o nível das caixas d'água e avisa se houver vazamentos.

🛠️ Tecnologias Principais
Sensores + ESP32: Leitura do solo, água e caixas d'água transmitida sem fio.

Servidor (Node.js + MQTT): Recebe os dados e decide quando ligar as bombas ou mandar alertas.

Painel Web (React): Tela simples para alunos, professores e equipe de manutenção acompanharem tudo.

🏗️ Como Funciona (Fluxo Simplificado)
Plaintext
[ Sensores no Campo, Tanques e Caixas ]
                 │
                 ▼ (Envio Sem Fio)
         [ Placa ESP32 ]
                 │
                 ▼ (Internet / Wi-Fi)
    [ Servidor Central (Cérebro) ]
       │                     │
       ▼                     ▼
[ Aciona Bombas / Relés ]  [ Envia Alertas no Painel Web ]
