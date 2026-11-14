# Mundo de Wumpus — Agente Inteligente (IA)

Implementação de um agente inteligente baseado em conhecimento e inferência probabilística para resolução do problema clássico do **Mundo de Wumpus** em ambientes dinâmicos $N \times N$.

---

## Estrutura do Projeto

- `assets/` — Sprites, ícones e fontes da interface gráfica
- `docs/` — Diagramas, gráficos de resultados e apresentação
- `src/environment/` — Regras do mundo NxN, geração procedural e sensores (`world.py`, `entities.py`)
- `src/agent/` — Base de conhecimento, inferência e pathfinding (`knowledge_base.py`, `inference.py`, `pathfinding.py`)
- `src/ui/` — Interface gráfica em Pygame e painel de métricas (`renderer.py`, `components.py`)
- `src/main.py` — Ponto de entrada da aplicação
- `tests/` — Testes unitários automatizados (modo headless)

---

## Configuração do Ambiente Local

1. **Clone o repositório:**
   - **Via SSH:** `git clone git@github.com:patricia-helen/wumpus-world-ai.git`
   - **Via HTTPS:** `git clone https://github.com/patricia-helen/wumpus-world-ai.git`

2. **Entre na pasta e ative o ambiente virtual:**
   - `cd wumpus-world-ai`
   - `python3 -m venv venv`
   - `source venv/bin/activate` (Linux/macOS) ou `.\venv\Scripts\Activate.ps1` (Windows)

3. **Instale as dependências e execute:**
   - `pip install -r requirements.txt`
   - *Nota: O projeto utiliza `pygame-ce` (Community Edition) para compatibilidade com Python 3.12+, mantendo a importação padrão `import pygame`.*
   - `python src/main.py`

---

## Organização Ágil: Sprints e Quadro Kanban (GitHub Projects)

Para que todos acompanhem o progresso sem sobrecarga ou dúvidas sobre o que fazer, organizamos o desenvolvimento em **Sprints** e gerenciamos as tarefas na aba **Projects** deste repositório.

### O que são Sprints e como funcionam no nosso projeto?
Uma **Sprint** é um ciclo curto de trabalho (neste projeto, ciclos de 5 a 7 dias) com uma meta clara de entrega funcionando ao final. Em vez de tentar fazer tudo de uma vez na última semana, dividimos o sistema em etapas incrementais:
- **Sprint 1 (16/11 a 22/11 — MVP Funcional):** Mundo NxN básico + agente andando em casas 100% seguras + grid simples na tela.
- **Sprint 2 (23/11 a 29/11 — Inteligência Avançada):** Cálculo de probabilidade sob incerteza + disparo de flecha + múltiplos Wumpus + visualização da mente do agente.
- **Sprint 3 (30/11 a 04/12 — Testes e Polimento):** Simulações em lote, gráficos de métricas e finalização do código (*Code Freeze* em 04/12).
- **Contingência e Ensaio (05/12 a 13/12):** Margem de segurança para ajustes finos, slides e ensaio para a entrega oficial em **14/12**.

### Como usar o Quadro Kanban (GitHub Projects)
Na aba **Projects** do repositório, cada tarefa da Sprint aparece como um cartão que deve ser movido conforme o andamento:
1. **Todo (A Fazer):** Tarefas planejadas para a Sprint atual que ainda não foram iniciadas.
2. **In Progress (Fazendo / Em Progresso):** Quando você começar a programar uma tarefa, **arraste o cartão dela para esta coluna** (isso avisa a equipe que você já está trabalhando nela).
3. **In Review (Em Revisão):** Quando terminar o código e abrir o **Pull Request (PR)** no GitHub, mova o cartão para cá para que um colega revise seu código.
4. **Done (Concluído / Feito):** Assim que o Pull Request for aprovado e mesclado na branch `develop`, o cartão vai para esta coluna.

---

## Fluxo de Trabalho no GitHub (Git Flow)

Para evitar conflitos de código e manter o histórico limpo, seguimos estas regras:

- **`main`**: Código estável e testado (atualizada apenas ao final de cada Sprint). **Proibido push direto.**
- **`develop`**: Branch de integração onde as funcionalidades são unidas. **Proibido push direto.**
- **`feat/<nome-da-tarefa>`**: Branch individual criada sempre a partir da `develop`.

### Passo a Passo para Desenvolver uma Tarefa

1. **Atualize a `develop` local:**
   `git checkout develop && git pull origin develop`
2. **Crie sua branch de trabalho:**
   `git checkout -b feat/nome-da-tarefa`
3. **Salve e envie suas alterações:**
   `git add . && git commit -m "feat: descricao" && git push -u origin feat/nome-da-tarefa`
4. **Abra um Pull Request (PR):**
   No GitHub, abra um PR da sua branch `feat/...` apontando para **`develop`** e peça revisão de 1 colega.
