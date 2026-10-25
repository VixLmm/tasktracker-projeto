cat > README.md << 'EOF'
# TaskTracker

Aplicação de linha de comando (CLI) em Python para gerenciar tarefas do dia a dia. Projeto cumulativo do Bootcamp II (Fase 2: Git, GitHub e Python | Fase 3: Docker e orquestração).

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
- Docker e Docker Compose

## Como executar

### Com Docker (recomendado)

Requisito: Docker e Docker Compose instalados.

```bash
git clone https://github.com/<seu-usuario>/tasktracker-projeto.git
cd tasktracker-projeto
```

Como construir a imagem:

```bash
docker build -t tasktracker .
```

Como rodar o container em modo isolado:

```bash
docker run -it tasktracker
```

Como rodar via orquestração (Recomendado):

```bash
docker compose run --rm tasktracker-app
```

> O `docker-compose.yml` ativa `stdin_open` e `tty`, necessários para que o menu interativo (`input()`) funcione dentro do container. Por isso usamos `docker compose run` em vez de `docker compose up`.

### Sem Docker

Requisito: Python 3 instalado.

```bash
python src/main.py
```

### Menu da aplicação

```
1. Cadastrar nova tarefa
2. Visualizar tarefas cadastradas
3. Sair
```

Observação: as tarefas ficam apenas em memória e são perdidas ao encerrar o programa.

## Estrutura do repositório

```
tasktracker-projeto/
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── README.md
├── docs/
│   └── planejamento_logico.pdf
└── src/
    └── main.py
```

## Autor

Lucas Maubrigades Marotti - Bootcamp II
EOF
