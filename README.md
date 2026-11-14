# Mundo de Wumpus — Agente Inteligente (IA)

Implementação de um agente inteligente baseado em conhecimento e inferência probabilística para resolução do problema clássico do **Mundo de Wumpus** em ambientes dinâmicos N x N.

## Estrutura do Projeto

- `assets/` — Sprites, ícones e fontes da interface gráfica
- `docs/` — Diagramas, gráficos de resultados e apresentação
- `src/environment/` — Regras do mundo NxN, geração procedural e sensores (`world.py`, `entities.py`)
- `src/agent/` — Base de conhecimento, inferência e pathfinding (`knowledge_base.py`, `inference.py`, `pathfinding.py`)
- `src/ui/` — Interface gráfica em Pygame e painel de métricas (`renderer.py`, `components.py`)
- `src/main.py` — Ponto de entrada da aplicação
- `tests/` — Testes unitários automatizados (modo headless)

## Configuração do Ambiente Local

1. **Clone o repositório:**
   - Via SSH: `git clone git@github.com:patricia-helen/wumpus-world-ai.git`
   - Via HTTPS: `git clone https://github.com/patricia-helen/wumpus-world-ai.git`

2. **Entre na pasta e ative o ambiente virtual:**
   - `cd wumpus-world-ai`
   - `python3 -m venv venv`
   - `source venv/bin/activate` (Linux/macOS) ou `.\venv\Scripts\Activate.ps1` (Windows)

3. **Instale as dependências e execute:**
   - `pip install -r requirements.txt`
   - `python src/main.py`

## Fluxo de Trabalho no GitHub (Git Flow)

- **`main`**: Código estável e testado (atualizada apenas ao final de cada Sprint). Proibido push direto.
- **`develop`**: Branch de integração onde as funcionalidades são unidas. Proibido push direto.
- **`feat/<nome-da-tarefa>`**: Branch individual criada sempre a partir da `develop`.

### Passo a Passo para Desenvolver uma Tarefa

1. Atualize a `develop`: `git checkout develop && git pull origin develop`
2. Crie sua branch: `git checkout -b feat/nome-da-tarefa`
3. Faça commit e push: `git add . && git commit -m "feat: descricao" && git push -u origin feat/nome-da-tarefa`
4. Abra um **Pull Request (PR)** da sua branch `feat/...` apontando para **`develop`** e peça revisão de 1 colega.
