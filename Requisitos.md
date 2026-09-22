## Requisitos funcionais (o que o sistema faz)

## RF01 — Cadastrar um objeto encontrado, com nome, descrição, local onde foi achado, data e local de retirada
## RF02 — Anexar uma foto do objeto ao cadastro (opcional)
## RF03 — Salvar automaticamente cada objeto cadastrado
## RF04 — Listar todos os objetos cadastrados
## RF05 — Buscar objetos por palavra-chave (nome, descrição ou local)
## RF06 — Filtrar objetos por status: aguardando retirada ou já devolvido
## RF07 — Marcar um objeto como devolvido (ou reabrir, caso tenha sido marcado por engano)
## RF08 — Excluir um registro, com confirmação antes de apagar
## RF09 — Mostrar mensagem clara quando não houver objetos cadastrados ou quando a busca não encontrar resultados
## RF10 — Exibir a contagem de itens exibidos em relação ao total cadastrado

## Requisitos não funcionais (como o sistema se comporta)

## RNF01 — Usabilidade: interface simples, sem necessidade de treinamento para secretaria ou alunos
## RNF02 — Responsividade: funciona tanto em computador quanto em celular
## RNF03 — Desempenho: busca e filtro respondem instantaneamente (processamento no próprio navegador, sem esperar servidor)
## RNF04 — Portabilidade: roda direto no navegador, sem instalação
## RNF05 — Compatibilidade: funciona nos navegadores modernos mais comuns (Chrome, Firefox, Edge, Safari)
## RNF06 — Acessibilidade básica: contraste adequado de cores e indicação visível de foco ao navegar pelo teclado
## RNF07 — Persistência: os dados cadastrados não se perdem ao fechar e reabrir a página, pois ficam salvos localmente
## Limitação atual (importante registrar)
## RNF08 — Os dados ficam salvos apenas no navegador de quem está usando a página — não há uma base compartilhada entre secretaria e alunos ainda. Isso é aceitável para um protótipo de demonstração, mas seria o primeiro ponto a evoluir para um sistema de uso real na escola (banco de dados compartilhado, como conversamos para o sistema de chamados de manutenção).
