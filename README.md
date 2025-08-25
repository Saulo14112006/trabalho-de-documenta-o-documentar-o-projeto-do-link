# trabalho-de-documenta-o-documentar-o-projeto-do-link

# Kanban Local

Um Kanban simples que roda localmente usando Java e HTML, para gerenciar tarefas.

## Como rodar

1. Baixe o projeto.
2. Abra no IntelliJ.
3. Execute a classe `App`.
4. Abra o navegador em `http://localhost:8080`.

## Funcionalidades

- Criar tarefas com título e descrição.
- Mover tarefas entre To-Do, Doing e Done.
- Deletar tarefas.
- Salvar tarefas localmente em CSV.

## Comentários do projeto

- O `main()` inicializa o servidor HTTP na porta 8080.
- A função `carregar()` lê o arquivo `data_tasks.csv` e popula os arrays de tarefas.
- Quando você acessa a raiz `/` no navegador, o `RootHandler` envia o HTML do Kanban.
- O JavaScript do navegador faz requisições à API REST (`/api/tasks`) para listar, criar, mover e deletar tarefas.
- Todas as alterações são salvas no CSV.
- O projeto está todo em uma única classe, o que facilita ver tudo em um lugar, mas dificulta manutenção.
- O código mistura Java e HTML, tornando a leitura e manutenção mais complexa.
- Poderia ser dividido em múltiplas classes e módulos para melhor organização.

## Observações / Melhorias

- Separar a lógica do servidor e a lógica de persistência em classes diferentes.
- Criar uma camada de serviço para manipulação de tarefas.
- Usar templates HTML externos para separar o front-end do back-end.
- Possível migração para um framework web para maior escalabilidade.

MIT License
