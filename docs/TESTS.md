# 📋 Checklist de Testes Manuais — WebMVC Contatos

Este documento contém o planejamento de testes manuais para garantir o correto funcionamento das camadas e fluxos da aplicação WebMVC de Contatos.

---

## 🔑 1. Tela Inicial e Listagem de Contatos
- [ ] O sistema carrega a página inicial sem erros de banco de dados ou PHP.
- [ ] Todos os contatos cadastrados aparecem listados de forma legível.
- [ ] A tabela ou lista exibe corretamente os campos (Nome, E-mail, Telefone).

## ➕ 2. Cadastro de Novos Contatos
- [ ] O formulário de cadastro abre corretamente ao clicar em "Novo Contato" (ou equivalente).
- [ ] É possível preencher todos os campos obrigatórios.
- [ ] Ao clicar em "Salvar", os dados são gravados no banco e o usuário é redirecionado de volta para a listagem.
- [ ] O novo contato aparece imediatamente no topo ou no fim da lista.
- [ ] **Validação:** O sistema impede o envio se campos obrigatórios (como Nome ou E-mail) estiverem vazios?

## ✏️ 3. Edição/Atualização de Contatos
- [ ] Ao clicar em "Editar" em um registro, o formulário abre preenchido com as informações atuais daquele contato.
- [ ] Se um campo for alterado e salvo, as modificações são reflected corretamentes na listagem.
- [ ] Cancelar a edição não altera os dados originais do contato.

## ❌ 4. Exclusão de Contatos
- [ ] Ao clicar em "Excluir", o sistema solicita uma confirmação (alerta em JavaScript ou página de confirmação).
- [ ] Após confirmar a exclusão, o contato some definitivamente da listagem.
- [ ] Cancelar a exclusão mantém o registro intacto.

## 🐛 5. Testes de Layout e Links
- [ ] Todos os links do menu/navegação estão direcionando para as páginas corretas (sem erro 404).
- [ ] A interface mantém uma organização visual aceitável (sem textos desalinhados ou botões quebrados).