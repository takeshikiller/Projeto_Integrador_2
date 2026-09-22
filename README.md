# Sistema de Achados e Perdidos

## O que é
Um protótipo funcional em página web que digitaliza o processo de achados e perdidos da escola. Os alunos podem pesquisar online antes de irem até a secretaria.

---

## Como funciona

### 1. Cadastro (Secretaria / Funcionário)
Quando um objeto é encontrado, o funcionário preenche uma ficha com:
* Nome do objeto
* Descrição
* Local onde foi achado
* Data
* Onde pode ser retirado
* Foto (opcional)

O registro fica salvo com o status **"aguardando retirada"**. Após a entrega, o funcionário pode alterar o status para **"devolvido"** (permitindo reabrir se necessário) ou **excluir** o registro.

### 2. Busca (Aluno)
O aluno acessa a página, digita uma palavra-chave (nome do objeto, local, etc.) e visualiza na hora as fichas correspondentes, com foto e detalhes para saber onde buscar o item.

---

## Limitação importante do protótipo
Os dados ficam salvos no armazenamento local (`localStorage`) do navegador de quem está usando a página. Isso funciona bem para testes e demonstrações, mas cada pessoa vê apenas os registros feitos no seu próprio dispositivo, sem uma lista compartilhada entre secretaria e alunos. Para uso coletivo real, o próximo passo seria conectá-lo a um banco de dados compartilhado.
