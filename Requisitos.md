Requisitos Funcionais (O que o sistema deve fazer)

RF01 - Coleta Contínua de Dados: O sistema deve ler periodicamente os dados dos sensores (nível do reservatório, vazão de saída e parâmetros de qualidade).

RF02 - Transmissão de Leituras: O dispositivo IoT deve enviar as medições coletadas para o servidor via protocolo MQTT em intervalos configuráveis.

RF03 - Alertas de Anomalias: O sistema deve emitir notificações em tempo real (painel web e e-mail/SMS) quando detectar vazamentos ou níveis críticos de água.

RF04 - Visualização em Painel (Dashboard): A interface web deve exibir gráficos dinâmicos com o nível atual da água, histórico de consumo e indicadores de qualidade.

RF05 - Previsão de Autonomia: O sistema deve calcular e exibir uma estimativa do tempo restante até o esgotamento do reservatório com base no fluxo médio de consumo.

RF06 - Gestão de Dispositivos e Reservatórios: O usuário administrador deve poder cadastrar, editar e remover reservatórios e seus respectivos módulos ESP32.

Requisitos Não Funcionais (Atributos de qualidade e restrições)

RNF01 - Baixa Latência: As leituras enviadas pelos sensores devem ser processadas e refletidas no painel de controle em menos de 3 segundos.

RNF02 - Eficiência Energética: O código do firmware no ESP32 deve utilizar modos de baixo consumo (deep sleep) entre as leituras para economizar bateria em locais sem rede elétrica direta.

RNF03 - Tolerância a Falhas Conectivas: Caso a conexão sem fio seja perdida, o microcontrolador deve armazenar localmente as leituras mais recentes e sincronizá-las assim que a rede for restabelecida.

RNF04 - Escalabilidade de Dados: O banco de dados de séries temporais (InfluxDB) deve suportar a gravação contínua de centenas de leituras por segundo sem perda de desempenho.

RNF05 - Segurança de Comunicação: Toda a troca de mensagens via MQTT e chamadas de API web deve utilizar criptografia TLS/SSL e autenticação por tokens seguros.

RNF06 - Responsividade da Interface: O painel web deve ser adaptável e funcional em telas de smartphones, tablets e computadores desktop.
