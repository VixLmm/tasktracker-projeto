# TaskTracker

Aplicação de linha de comando (CLI) em Python para gerenciar tarefas do dia a dia. Projeto cumulativo do Bootcamp II (Fase 2: Git, GitHub e Python).

## Funcionalidades

- Cadastrar tarefas com título, descrição, prioridade e data limite
- Visualizar todas as tarefas cadastradas
- Validação de dados na entrada

## Regras de negócio

- **Título:** obrigatório. Entradas vazias ou só com espaços são rejeitadas e o programa pede novamente.
- **Prioridade:** aceita apenas `Alta`, `Média` (ou `Media`) e `Baixa`. Qualquer outro valor gera erro e nova tentativa.
- **Data limite:** texto livre (sugestão: `DD/MM/AAAA`).
- **Status:** definido automaticamente como `Pendente` no cadastro.

## Tecnologias

- Python 3

## Como executar

Requisito: Python 3 instalado.

```bash
git clone https://github.com/VixLmm/tasktracker-projeto-bootcamp-2.git
cd tasktracker-projeto
python src/main.py
```

Menu da aplicação:

```
1. Cadastrar nova tarefa
2. Visualizar tarefas cadastradas
3. Sair
```

Observação: as tarefas ficam apenas em memória e são perdidas ao encerrar o programa.

## Estrutura do repositório

```
tasktracker-projeto/
├── README.md
├── .gitignore
├── docs/
│   └── planejamento_logico.pdf
└── src/
    └── main.py
```

## Autor

 Lucas Maubrigades Marotti - Bootcamp II
