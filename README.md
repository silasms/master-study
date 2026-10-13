# 🎓 Mestrado em IA & Otimização · Digital Garden & Estudos

> **Pesquisador & Engenheiro:** Silas Medeiros da Silva  
> **Linha de Pesquisa:** Aprendizado de Máquina, Otimização Combinatória e Pesquisa Operacional  
> **Instituições Alvo:** UFRJ (COPPE/PESC), PUC-Rio (DI) e USP (IME)  

Este repositório reúne todo o material de nivelamento e aprofundamento matemático, resoluções analíticas de exercícios, implementações de engenharia e notas de pesquisa para o mestrado. 

O projeto funciona nativamente como um **Digital Garden** construído com **[Quartz v4](https://quartz.jzhao.xyz/)**, renderizando fórmulas $\LaTeX$ (via KaTeX), mapas conceituais (Graph View) e navegação interativa.

---

## 🗂️ Estrutura do Repositório

```text
.
├── content/                                       # Fonte de verdade das notas públicas (.md)
│   ├── index.md                                   # Página inicial do Digital Garden
│   ├── 00_nivelamento_pre_calculo/                # Fase 0: Lógica formal, técnicas de prova e funções
│   ├── 01_calculo_univariavel/                    # Fase 1: Limites, derivadas, integrais e Taylor
│   ├── 02_algebra_linear/                         # Fase 2: Subespaços, projeções, espectral e SVD
│   ├── 03_calculo_multivariavel_otimizacao/        # Fase 3: Gradientes, Hessianas, convexidade e KKT
│   ├── 04_probabilidade_estatistica/              # Fase 4: Gaussianas multivariadas, MLE, MAP e Markov
│   └── 05_otimizacao_combinatoria_pesquisa_operacional/ # Fase 5: Grafos, Simplex, MIP, VRP e meta-heurísticas
├── quartz/                                        # Componentes e motor do Quartz
├── quartz.config.ts                               # Configuração de temas, KaTeX e metadados
├── quartz.layout.ts                               # Layout das páginas (Explorer, Graph, TOC)
├── Dockerfile                                     # Build multi-stage para containerização
├── docker-compose.yml                             # Orquestração do serviço (porta 8080)
└── package.json                                   # Dependências do Quartz
```

---

## 🚀 Como Executar Localmente

### Pré-requisitos
- **Node.js:** Versão 20 ou 22 (recomendado via `nvm`)
- **npm:** Versão 10+

### Instalação e Execução
```bash
# 1. Ativar Node 22 (se usar nvm)
nvm use 22

# 2. Instalar dependências
npm install

# 3. Rodar servidor de desenvolvimento com hot-reload
npx quartz build --serve
```
O servidor estará acessível em `http://localhost:8080`. Qualquer alteração salva dentro de `content/` atualiza o navegador instantaneamente.

---

## 🐳 Como Executar via Docker

O repositório já inclui `Dockerfile` e `docker-compose.yml` prontos:

```bash
# Iniciar o container em segundo plano (reinicia automaticamente)
docker compose up -d --build

# Ver logs da compilação e acessos
docker compose logs -f

# Parar o serviço
docker compose down
```

---

## 🌐 Acesso Remoto no Servidor (Oracle Cloud)

Para acessar o servidor remoto onde o container está rodando 24/7:
```bash
# Conectar ao servidor
ssh oracle

# Ir até o diretório do projeto
cd ~/mestrado

# Visualizar status dos containers
docker compose ps
```

Para abrir o site no navegador da sua máquina local através de um túnel SSH seguro e direto:
```bash
ssh -L 8080:localhost:8080 oracle
```
E acesse `http://localhost:8080` no seu navegador.
