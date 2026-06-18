# Guia de Contribuição

Este projeto é um esforço coletivo dos alunos da disciplina **Fundamentos de Sistemas para Internet**. O objetivo é construir e evoluir uma aplicação seguindo estritamente a arquitetura em camadas. Para garantir que o projeto permaneça organizado e funcional, siga as regras abaixo.

## 1. Fluxo de Desenvolvimento
Não trabalhe diretamente na branch `main`. Siga este fluxo:

1. **Criação de Branch:** Antes de começar, crie uma branch específica para sua tarefa:
   `git checkout -b feature/nome-da-funcionalidade` ou `fix/correcao-de-erro`.
2. **Desenvolvimento:** Respeite a separação de camadas:
   - **Controller:** Recebe a requisição e delega para o Service.
   - **Service:** Processa a lógica de negócio e validações.
   - **Repository:** Interage diretamente com o banco de dados via PDO.
3. **Commit:** Escreva mensagens claras no padrão: `feat: [descrição]` ou `fix: [descrição]`.
4. **Pull Request (PR):** Ao concluir, abra um PR para a branch `main`.

## 2. Regras de Ouro
- **Code Review:** Todo PR deve ser revisado por pelo menos um colega. O objetivo é validar se a lógica está na camada correta. Se o código estiver "misturado" (ex: SQL dentro do Controller), o PR não será aprovado.
- **Segurança:** Nunca inclua credenciais de banco de dados no repositório. O arquivo `config/Database.php` deve conter apenas configurações genéricas de ambiente local.
- **Não ao Merge Direto:** Ninguém deve aprovar o próprio PR. Aguarde a revisão de um colega.

## 3. Manutenção da Estrutura
- **Documentação:** Se você alterar algo na estrutura do banco de dados (`database/schema.sql`) ou criar novas rotas, **obrigatoriamente** atualize o `README.md`.
- **Limpeza:** Antes de abrir o PR, verifique se seu código não contém comentários de teste, *var_dumps* ou códigos mortos.

## 4. Comunicação
- Surgiu uma dúvida sobre como implementar uma funcionalidade no Service? Abra uma **Issue** ou inicie uma conversa no grupo da turma.
- Se o projeto quebrar após um merge, notifique imediatamente o autor do PR e o revisor para que possamos corrigir juntos.

---
*Lembre-se: este é um projeto didático. O foco é aprender a organizar o código em camadas. Se estiver em dúvida, pergunte antes de fazer o merge.*
