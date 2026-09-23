## Requisitos Funcionais

## Avisos

## RF01: O sistema deve permitir cadastrar um aviso com título, mensagem, prioridade (normal/urgente) e público-alvo.
## RF02: O sistema deve listar os avisos publicados em ordem cronológica decrescente.
## RF03: O sistema deve exibir visualmente a prioridade e o público-alvo de cada aviso.

## Reuniões

## RF04: O sistema deve permitir marcar reuniões com assunto, data, horário, local e participantes.
## RF05: O sistema deve listar as reuniões agendadas em ordem cronológica crescente.
## RF06: O campo de local e participantes deve ser opcional.

## Comissões

## RF07: O sistema deve permitir indicar um professor para uma comissão, com nome do professor, nome da comissão e observação opcional.
## RF08: O sistema deve listar todas as indicações enviadas, com data e hora do registro.

## Gerais

## RF09: O sistema deve manter contadores atualizados de itens em cada seção (avisos, reuniões, comissões).
## RF10: O sistema deve persistir os dados entre sessões no mesmo navegador/dispositivo.
## RF11: O sistema deve validar campos obrigatórios antes de permitir o envio de qualquer formulário.
## Requisitos Não Funcionais
## RNF01 (Usabilidade): Interface responsiva, adaptada tanto para desktop quanto para dispositivos móveis.
## RNF02 (Portabilidade): Deve funcionar em qualquer navegador moderno sem necessidade de instalação.
## RNF03 (Desempenho): Carregamento e resposta das ações (cadastro, listagem) devem ocorrer em menos de 1 segundo.
## RNF04 (Confiabilidade): Erros de leitura/escrita no armazenamento local não devem quebrar a aplicação (tratamento de exceções).
## RNF05 (Acessibilidade visual): Suporte a tema claro e escuro conforme preferência do sistema operacional.
## RNF06 (Manutenibilidade): Código estruturado em um único arquivo autocontido, facilitando distribuição e futura migração para uma arquitetura com backend.
## RNF07 (Escalabilidade — limitação atual): Este protótipo armazena dados localmente no navegador; para uso real em múltiplos dispositivos e usuários simultâneos, seria necessário um backend com banco de dados compartilhado.
## RNF08 (Segurança — limitação atual): O protótipo não possui autenticação de usuários; qualquer pessoa com acesso ao link pode cadastrar avisos, reuniões e indicações. Uma versão de produção exigiria login e controle de permissões (ex: só coordenação pode indicar comissões).
