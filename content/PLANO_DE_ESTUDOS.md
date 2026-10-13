# Plano de Estudos para Mestrado em Inteligência Artificial e Otimização
**Instituições Alvo:** UFRJ (COPPE/PESC), USP, PUC-Rio  
**Área de Concentração:** Aprendizado de Máquina, Otimização Combinatória e Pesquisa Operacional  
**Autor:** Silas Medeiros da Silva  
**Data de Início:** 13 de Outubro de 2026  

---

## 🧭 1. Filosofia e Diretrizes do Plano

Este plano foi concebido com uma premissa fundamental: **construir uma base matemática sólida do zero**, sem atalhos, sem assumir pré-requisitos não consolidados e sem depender de notas ou históricos prévios.

O objetivo é transformar você em um pesquisador capaz de:
1. **Ler e dissecar artigos científicos** de ponta em *Machine Learning* e *Pesquisa Operacional* compreendendo cada equação, teorema e demonstração.
2. **Formular matematicamente problemas do mundo real** (especialmente os problemas logísticos e industriais tratados na COPPE e PUC-Rio) em termos de programação matemática e aprendizado estatístico.
3. **Unir rigor matemático à excelência de engenharia**, convertendo modelos formais em código de produção escalável, robusto e reprodutível.

### A Tríade Metodológica de Estudo
Para cada tópico matemático, siga rigorosamente três etapas:
1. **Intuição & Rigor Conceitual (40% do tempo):** Compreender o porquê do conceito, sua interpretação geométrica e definições formais com provas-chave.
2. **Resolução de Exercícios no Papel (40% do tempo):** Fazer contas e demonstrações à mão. A fluência matemática só se desenvolve na ponta do lápis.
3. **Validação Computacional (20% do tempo):** Implementar o conceito em Python (NumPy, SciPy, Matplotlib ou PuLP/OR-Tools) ou Go, validando numericamente os resultados.

---

## 🗺️ 2. Visão Geral das Fases

```
[ Fase 0: Nivelamento e Pré-Cálculo ] (Semanas 1 - 3)
                 │
                 ▼
[ Fase 1: Cálculo Diferencial e Integral I ] (Semanas 4 - 8)
                 │
                 ▼
[ Fase 2: Álgebra Linear Estrutural e Aplicada ] (Semanas 9 - 16)
                 │
                 ▼
[ Fase 3: Cálculo Multivariável e Otimização Convexa ] (Semanas 17 - 22)
                 │
                 ▼
[ Fase 4: Probabilidade e Inferência Estatística ] (Semanas 23 - 28)
                 │
                 ▼
[ Fase 5: Otimização Combinatória e Pesquisa Operacional ] (Semanas 29 - 36)
```

---

## 📚 3. Cronograma Detalhado Fase a Fase

---

### 📍 FASE 0: Nivelamento, Lógica e Pré-Cálculo
**Duração estimada:** 3 semanas  
**Objetivo:** Eliminar qualquer micro-lacuna em manipulação algébrica, notação formal e técnicas de demonstração antes de entrar no cálculo.

#### Tópicos de Estudo:
* **Semana 1: Linguagem Matemática e Demonstrações**
  * Lógica proposicional: implicação ($\implies$), equivalência ($\iff$), quantificadores ($\forall, \exists$).
  * Métodos de prova: Prova direta, prova por contrapositiva, prova por contradição (*reductio ad absurdum*).
  * Princípio da Indução Matemática (fundamental para algoritmos e complexidade).
  * Teoria básica de conjuntos: pertinência, inclusão, união, interseção, produto cartesiano, cardinalidade.
* **Semana 2: Manipulação Algébrica e Notação Formal**
  * Somatórios ($\sum$) e Produtórios ($\prod$): propriedades, mudanças de índice, somas telescópicas, progressões (PA e PG).
  * Inequações, valor absoluto/módulo e desigualdade triangular.
  * Geometria analítica básica: retas, planos, distâncias euclidianas.
* **Semana 3: Estudo Rigoroso de Funções**
  * Conceito de função: domínio, contradomínio, imagem.
  * Injetividade, sobrejetividade e bijetividade; funções inversas e compostas.
  * Funções elementares: polinomiais, racionais, exponenciais, logarítmicas (propriedades de $\ln$ e $\log$), funções trigonométricas.
  * Comportamento assintótico intuitivo e limites no infinito de forma qualitativa.

#### Bibliografia e Materiais:
* *Livro:* **Fundamentos de Matemática Elementar** (Gelson Iezzi) – Volumes 1 (Conjuntos e Funções) e 2 (Logaritmos).
* *Alternativa Internacional:* **Precalculus** (James Stewart ou Robert Blitzer).
* *Canal/Curso:* Khan Academy (Trilhas de Álgebra Avançada e Pré-Cálculo).

---

### 📍 FASE 1: Cálculo Diferencial e Integral Univariável (Cálculo I)
**Duração estimada:** 5 semanas  
**Objetivo:** Dominar taxas de variação, acumulação, limites, expansões em séries e otimização univariada.

#### Tópicos de Estudo:
* **Semana 4: Limites e Continuidade**
  * Conceito intuitivo e formal de limite ($\epsilon-\delta$ de forma conceitual).
  * Limites laterais, limites no infinito e limites infinitos.
  * Teorema do Confronto (Teorema do Sanduíche).
  * Continuidade de funções e o Teorema do Valor Intermediário (TVI).
* **Semana 5: A Derivada e Regras de Derivação**
  * Definição de derivada como taxa instantânea de variação e inclinação da reta tangente: $f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$.
  * Derivadas de funções fundamentais (polinômios, $e^x$, $\ln x$, trigonométricas).
  * Regras operatórias: soma, produto, quociente.
  * **Regra da Cadeia:** o alicerce absoluto de todo o treinamento de redes neurais.
* **Semana 6: Aplicações de Derivadas e Otimização 1D**
  * Teorema de Rolle e Teorema do Valor Médio (TVM).
  * Pontos críticos: máximos e mínimos locais e globais.
  * Teste da 1ª e 2ª derivadas: concavidade, convexidade em 1D e pontos de inflexão.
  * Método de Newton-Raphson para busca de raízes e otimização unidimensional (implementar em Python).
* **Semana 7: Integral e Teorema Fundamental do Cálculo**
  * A integral como limite de somas de Riemann (acumulação de área).
  * O Teorema Fundamental do Cálculo (TFC) unindo derivação e integração.
  * Técnicas essenciais: Integração por substituição (mudança de variáveis) e integração por partes.
  * Integrais impróprias (essenciais para variáveis aleatórias contínuas).
* **Semana 8: Sequências, Séries e Polinômios de Taylor**
  * Noções de convergência de sequências e séries numéricas.
  * **Polinômio de Taylor e Séries de Taylor:** aproximação linear ($f(x) \approx f(a) + f'(a)(x-a)$) e aproximação quadrática. O resto de Taylor.
  * Importância: entender por que algoritmos de otimização aproximam funções de perda por modelos lineares ou quadráticos locais.

#### Bibliografia e Materiais:
* *Livro:* **Cálculo - Volume 1** (James Stewart) OU **Um Curso de Cálculo - Vol. 1** (Hamilton Luiz Guidorizzi).
* *Vídeos:* Série *Essence of Calculus* (3Blue1Brown) – obrigatório assistir antes de cada bloco conceitual.

---

### 📍 FASE 2: Álgebra Linear Estrutural e Numérica
**Duração estimada:** 8 semanas  
**Objetivo:** Tornar-se completamente fluente em espaços vetoriais, geometria de matrizes, projeções, autovalores/autovetores e decomposições matriciais.

#### Tópicos de Estudo:
* **Semana 9: Vetores, Matrizes e Eliminação Gaussiana**
  * Vetores em $\mathbb{R}^n$: combinações lineares, produto escalar, ângulo entre vetores.
  * Multiplicação de matrizes sob 4 perspectivas: produto interno, combinação linear de colunas, combinação linear de linhas, produto externo.
  * Sistemas de equações lineares ($Ax = b$), Eliminação Gaussiana e fatoração $LU$.
  * Matrizes invertíveis, matriz transposta e simétrica.
* **Semana 10: Espaços Vetoriais e Subespaços**
  * Definição de espaço vetorial real e subespaços.
  * Independência linear, conjunto gerador, base e dimensão.
  * Os **4 Subespaços Fundamentais de uma Matriz** (visão de Gilbert Strang):
    * Espaço Coluna $C(A)$
    * Espaço Nulo / Núcleo $N(A)$
    * Espaço Linha $C(A^T)$
    * Espaço Nulo à Esquerda $N(A^T)$
  * Teorema do Posto-Nulidade (*Rank-Nullity Theorem*).
* **Semana 11: Transformações Lineares e Mudança de Base**
  * Transformações lineares: definição, núcleo e imagem.
  * Matriz associada a uma transformação linear em bases quaisquer.
  * Mudança de base e matrizes semelhantes ($B = P^{-1}AP$).
* **Semana 12: Ortogonalidade, Projeções e Mínimos Quadrados**
  * Espaços com produto interno e desigualdade de Cauchy-Schwarz.
  * Subespaços ortogonais e complemento ortogonal: $C(A)^\perp = N(A^T)$.
  * Matrizes ortogonais (propriedade $Q^T Q = I$).
  * Algoritmo de ortogonalização de Gram-Schmidt e Decomposição $QR$.
  * **Projeções Ortogonais e Mínimos Quadrados (*Ordinary Least Squares*):** dedução formal da equação normal $A^T A \hat{x} = A^T b$.
* **Semana 13: Determinantes e Autovalores/Autovetores**
  * Determinante: propriedades geométricas (fator de escala de hipervolumes).
  * Equação característica: $\det(A - \lambda I) = 0$.
  * Autovetores, autoespaços e multiplicidades algébrica e geométrica.
  * Diagonalização de matrizes ($A = X \Lambda X^{-1}$).
* **Semana 14: Matrizes Simétricas e o Teorema Espectral**
  * Propriedades das matrizes simétricas reais: autovalores reais e autovetores ortogonais.
  * **Teorema Espectral:** $A = Q \Lambda Q^T = \sum \lambda_i q_i q_i^T$.
  * Formas quadráticas: $x^T A x$.
  * **Matrizes Positivas Definidas e Semidefinidas ($A \succ 0, A \succeq 0$):**
    * Testes de positividade (autovalores positivos, pivôs, determinantes principais).
    * Interpretação geométrica: elipsóides e bacias de atração convexas.
    * Fatoração de Cholesky ($A = L L^T$).
* **Semana 15: Decomposição em Valores Singulares (SVD)**
  * A geometria do SVD para qualquer matriz $m \times n$: $A = U \Sigma V^T$.
  * Relação do SVD com autovalores de $A^T A$ e $A A^T$.
  * Pseudo-inversa de Moore-Penrose ($A^+$).
  * Aproximação de baixo posto (Teorema de Eckart-Young-Mirsky) e Compressão matricial.
  * Relação direta com PCA (*Principal Component Analysis*).
* **Semana 16: Normas Matriciais e Álgebra Linear Computacional**
  * Normas de vetores: normas $p$ ($L_1, L_2, L_\infty$).
  * Normas de matrizes induzidas e Norma de Frobenius $\|A\|_F$.
  * Número de condição de uma matriz ($\kappa(A)$), estabilidade numérica e propagação de erros.
  * Implementação em Python/NumPy de decomposições ($LU, QR, SVD$) e benchmarks de desempenho.

#### Bibliografia e Materiais:
* *Livro Principal:* **Introduction to Linear Algebra** (Gilbert Strang) e **Linear Algebra and Learning from Data** (Gilbert Strang).
* *Livro Prático Aplicado:* **Introduction to Applied Linear Algebra – Vectors, Matrices, and Least Squares** (Stephen Boyd & Lieven Vandenberghe – disponível gratuitamente online).
* *Vídeos:* Playlist clássica do MIT 18.06 (Gilbert Strang) e série *Essence of Linear Algebra* (3Blue1Brown).

---

### 📍 FASE 3: Cálculo Multivariável e Otimização Convexa
**Duração estimada:** 6 semanas  
**Objetivo:** Dominar cálculo diferencial em $\mathbb{R}^n$, gradientes, hessianas e a teoria de otimização contínua que move todo o aprendizado de máquina moderno.

#### Tópicos de Estudo:
* **Semana 17: Funções de Múltiplas Variáveis e Cálculo Diferencial em $\mathbb{R}^n$**
  * Funções escalares e vetoriais ($f: \mathbb{R}^n \to \mathbb{R}$ e $f: \mathbb{R}^n \to \mathbb{R}^m$).
  * Superfícies, curvas de nível e hiperplanos tangentes.
  * Derivadas parciais e derivadas direcionais.
  * **Vetor Gradiente ($\nabla f$):** propriedades, direção de máximo crescimento e ortogonalidade às curvas de nível.
* **Semana 18: Jacobiana, Hessiana e Regra da Cadeia Multivariável**
  * Matriz Jacobiana ($Df(x)$ ou $J$) para campos vetoriais.
  * Matriz Hessiana ($\nabla^2 f(x)$): definição, simetria (Teorema de Schwarz) e interpretação como curvatura de 2ª ordem.
  * **Regra da Cadeia Multivariável Matricial:** forma matricial de derivadas compostas (o motor formal da retropropagação / *backpropagation*).
  * Série de Taylor de 2ª ordem para funções multivariáveis: $f(x) \approx f(x_0) + \nabla f(x_0)^T (x - x_0) + \frac{1}{2}(x - x_0)^T \nabla^2 f(x_0) (x - x_0)$.
* **Semana 19: Conjuntos Convexos e Funções Convexas**
  * Conjuntos convexos, hiperplanos separadores e de suporte.
  * Funções convexas: definição pela corda ($f(\theta x + (1-\theta)y) \le \theta f(x) + (1-\theta)f(y)$).
  * Condição de 1ª ordem para convexidade: $f(y) \ge f(x) + \nabla f(x)^T (y - x)$.
  * Condição de 2ª ordem para convexidade: $\nabla^2 f(x) \succeq 0$ (Hessiana positiva semidefinida em todo o domínio).
  * Propriedade de ouro: todo mínimo local de uma função convexa em conjunto convexo é mínimo global.
* **Semana 20: Algoritmos de Otimização sem Restrições**
  * Formulação: $\min_{x \in \mathbb{R}^n} f(x)$.
  * Condições de otimalidade de 1ª ordem ($\nabla f(x^*) = 0$) e 2ª ordem ($\nabla^2 f(x^*) \succeq 0$).
  * **Descida do Gradiente (*Gradient Descent*):** taxa de aprendizado (*step size* / *backtracking line search*), taxa de convergência.
  * Descida do Gradiente Estocástica (SGD) e momentum.
  * **Método de Newton:** convergência quadrática, inversão da Hessiana e variações quasi-Newton (BFGS / L-BFGS).
* **Semana 21: Otimização com Restrições e Multiplicadores de Lagrange**
  * Problemas com restrições de igualdade: $\min f(x)$ sujeito a $h_i(x) = 0$.
  * A geometria dos multiplicadores de Lagrange: alinhamento dos gradientes da função objetivo e das restrições.
  * A função Lagrangeana $\mathcal{L}(x, \nu) = f(x) + \sum \nu_i h_i(x)$.
* **Semana 22: Dualidade e as Condições KKT (Karush-Kuhn-Tucker)**
  * Problema geral de otimização convexa: $\min f(x)$ s.a. $g_i(x) \le 0, h_j(x) = 0$.
  * Função Dual de Lagrange $g(\lambda, \nu)$ e o Problema Dual.
  * Dualidade fraca e Dualidade forte (Condição de Slater).
  * **Condições KKT:**
    1. Viabilidade primal: $g_i(x^*) \le 0, h_j(x^*) = 0$
    2. Viabilidade dual: $\lambda^* \ge 0$
    3. Folga complementar (*Complementary Slackness*): $\lambda_i^* g_i(x^*) = 0$
    4. Estacionariedade do gradiente: $\nabla f(x^*) + \sum \lambda_i^* \nabla g_i(x^*) + \sum \nu_j^* \nabla h_j(x^*) = 0$
  * Aplicação direta em Support Vector Machines (SVM) e problemas de alocação de recursos.

#### Bibliografia e Materiais:
* *Livro:* **Cálculo - Volume 2** (James Stewart) – capítulos de cálculo vetorial.
* *A Bíblia da Área:* **Convex Optimization** (Stephen Boyd & Lieven Vandenberghe – disponível em PDF gratuito pelo Stanford).
* *Curso:* Stanford EE364a (*Convex Optimization I* com Boyd – vídeos no YouTube).

---

### 📍 FASE 4: Probabilidade e Inferência Estatística para IA
**Duração estimada:** 6 semanas  
**Objetivo:** Dominar a modelagem de incerteza, distribuições multivariadas e métodos de estimação e decisão probabilística.

#### Tópicos de Estudo:
* **Semana 23: Fundamentos e Espaços de Probabilidade**
  * Axiomas de Kolmogorov, espaço amostral e eventos.
  * Probabilidade condicional, regra da probabilidade total e **Teorema de Bayes**.
  * Independência de eventos.
* **Semana 24: Variáveis Aleatórias Discretas e Contínuas**
  * Função de probabilidade (PMF), função densidade de probabilidade (PDF) e função de distribuição acumulada (CDF).
  * Esperança matemática ($E[X]$) e suas propriedades de linearidade.
  * Variância ($\mathrm{Var}(X)$), desvio padrão e momentos de ordem superior.
  * Distribuições clássicas: Bernoulli, Binomial, Poisson, Geométrica, Uniforme, Exponencial.
* **Semana 25: Variáveis Aleatórias Conjuntas e Vetores Aleatórios**
  * Distribuição conjunta, distribuições marginais e condicionais.
  * Independência de variáveis aleatórias.
  * Covariância e Coeficiente de Correlação de Pearson.
  * **A Distribuição Gaussiana Multivariada $\mathcal{N}(\mu, \Sigma)$:**
    * Matriz de covariância $\Sigma$ (que é sempre simétrica positiva semidefinida!).
    * Formas quadráticas no expoente: $(x - \mu)^T \Sigma^{-1} (x - \mu)$ (Distância de Mahalanobis).
    * Geometria dos contornos elípticos a partir dos autovalores e autovetores de $\Sigma$.
* **Semana 26: Desigualdades e Teoremas Limites**
  * Desigualdade de Markov e Desigualdade de Chebyshev.
  * Desigualdade de Jensen para funções convexas ($f(E[X]) \le E[f(X)]$).
  * Lei Fraca e Lei Forte dos Grandes Números.
  * **Teorema Central do Limite (TCL):** significado teórico e importância prática em ML.
* **Semana 27: Estimação de Parâmetros e Inferência**
  * Amostras aleatórias e estatísticas amostrais (média e variância amostral, estimadores não viesados).
  * **Máxima Verossimilhança (MLE - Maximum Likelihood Estimation):**
    * Função de verossimilhança $L(\theta)$ e log-verossimilhança $\ln L(\theta)$.
    * Derivação do MLE para distribuição Normal, Bernoulli e Regressão Linear.
  * **Máximo a Posteriori (MAP):** a perspectiva Bayesiana conectada à regularização de modelos ($L_2 \equiv$ prior Gaussiano, $L_1 \equiv$ prior Laplace).
* **Semana 28: Introdução a Processos Estocásticos e Cadeias de Markov**
  * Cadeias de Markov em tempo discreto: matriz de transição de estados.
  * Estados recorrentes, transitórios e distribuições estacionárias ($\pi P = \pi$).
  * Aplicação em algoritmos probabilísticos, meta-heurísticas e amostragem MCMC.

#### Bibliografia e Materiais:
* *Livro:* **A First Course in Probability** (Sheldon Ross) OU **Probability and Statistics** (Morris H. DeGroot & Mark J. Schervish).
* *Livro com foco em ML:* **Mathematics for Machine Learning** (Deisenroth, Faisal, Ong – disponível em mml-book.com).
* *Capítulos selecionados:* Capítulos 1 e 2 de **Pattern Recognition and Machine Learning** (Christopher Bishop).

---

### 📍 FASE 5: Otimização Combinatória, Grafos e Pesquisa Operacional
**Duração estimada:** 8 semanas  
**Objetivo:** Alinhar-se com o núcleo temático dos laboratórios do Prof. Pedro González (COPPE/UFRJ) e do Prof. Thibaut Vidal (PUC-Rio).

#### Tópicos de Estudo:
* **Semana 29: Teoria dos Grafos Aplicada à Otimização**
  * Grafos orientados e não orientados, graus, caminhos, ciclos e conectividade.
  * Representação computacional: matriz de adjacência, matriz de incidência, listas de adjacência.
  * Árvores geradoras mínimas (Algoritmos de Kruskal e Prim).
  * Caminhos mínimos: Dijkstra, Bellman-Ford e algoritmo de Floyd-Warshall.
* **Semana 30: Fluxos em Redes e Emparelhamento**
  * Redes de fluxo: capacidades, conservação de fluxo, cortes.
  * Teorema do Fluxo Máximo e Corte Mínimo (*Max-Flow Min-Cut Theorem*).
  * Algoritmo de Ford-Fulkerson e Edmonds-Karp.
  * Problema de transporte, problema de transbordo e problema de atribuição/emparelhamento bipartido.
* **Semana 31: Programação Linear (PL) – Formulação e Geometria**
  * Formulação canônica e padrão: $\max c^T x$ sujeito a $Ax \le b, x \ge 0$.
  * Geometria de PL: poliedros convexos, vértices, soluções básicas viáveis (BFS - *Basic Feasible Solutions*).
  * O Teorema Fundamental da Programação Linear (solução ótima em vértices).
  * O Método Simplex: operações de pivoteamento, matriz de base $B$, custos reduzidos.
* **Semana 32: Teoria da Dualidade em Programação Linear**
  * Formulação do Problema Dual a partir do Primal.
  * Teorema da Dualidade Fraca e Forte.
  * Teorema das Folgas Complementares em PL.
  * Interpretação econômica dos multiplicadores duais: preços-sombra (*shadow prices*) e análise de sensibilidade.
* **Semana 33: Programação Linear Inteira Mista (MIP / PLI)**
  * Formulação de variáveis inteiras e binárias ($x_i \in \{0, 1\}$).
  * Modelagem de restrições lógicas: "se-então", "ou-ou", custos fixos, limites de capacidade (*Big-M*).
  * Problemas clássicos:
    * Problema da Mochila (*Knapsack Problem*)
    * Problema de Cobertura de Conjuntos (*Set Covering / Set Partitioning*)
    * Problema das Instalações / Localização de Facilidades (*Facility Location*)
* **Semana 34: O Problema do Caixeiro Viajante (TSP) e Roteamento de Veículos (VRP)**
  * *O tema de ouro dos grupos de pesquisa da COPPE e da PUC-Rio.*
  * Formulação do TSP: formulação de Dantzig-Fulkerson-Johnson (DFJ) vs. formulação de Miller-Tucker-Zemlin (MTZ) para eliminação de subrotas.
  * Extensão para Roteamento de Veículos com Capacidade (CVRP) e Janelas de Tempo (VRPTW).
  * Complexidade e explosão combinatória: por que métodos ingênuos falham.
* **Semana 35: Algoritmos Exatos: Branch and Bound e Planos de Corte**
  * Relaxação linear de problemas inteiros (LP Relaxation).
  * Algoritmo de **Branch and Bound** (árvore de busca, limites inferiores e superiores, poda).
  * Cortes de Gomory e cortes específicos de problemas (Branch and Cut).
  * Formulação forte vs. formulação fraca: o conceito de envoltória convexa (*convex hull*).
* **Semana 36: Heurísticas, Meta-heurísticas e a Ponte com IA**
  * Métodos construtivos (vizinho mais próximo, economia de Clarke & Wright).
  * Busca local e estruturas de vizinhança (2-opt, Relocate, Swap).
  * Meta-heurísticas modernas: *Iterated Local Search* (ILS), *Adaptive Large Neighborhood Search* (ALNS), Algoritmos Genéticos Híbridos (linha clássica do Prof. Thibaut Vidal).
  * **A Fronteira IA + Otimização:** Aprendizado por Reforço e Redes Neurais para guiar buscas heurísticas e aprender políticas de ramificação no Branch & Bound (*Learning to Optimize*).

#### Bibliografia e Materiais:
* *Livro de Programação Linear:* **Introduction to Linear Optimization** (Dimitris Bertsimas & John N. Tsitsiklis – livro-texto fundamental do MIT/COPPE).
* *Livro de Programação Inteira:* **Integer Programming** (Laurence A. Wolsey).
* *Artigo Clássico de Roteamento:* Vidal, T., Crainic, T. G., Gendreau, M., & Prins, C. (2014). *A unified solution framework for multi-attribute vehicle routing problems*. European Journal of Operational Research.
* *Ferramentas de Implementação Prática:* Python com bibliotecas **PuLP**, **Pyomo** ou **Google OR-Tools** (implementar modelos e resolver via solvers abertos como CBC, SCIP e HiGHS).

---

## 📅 4. Estrutura da Rotina Semanal de Estudos

Para garantir consistência sem esgotamento, siga uma distribuição de blocos de estudo:

| Dia da Semana | Atividade | Foco |
| :--- | :--- | :--- |
| **Segunda-feira** | Teoria & Livro-texto | Leitura atenta dos capítulos da semana, anotações de teoremas e definições. |
| **Terça-feira** | Vídeo-aulas / Intuição | Assistir às aulas de apoio (Strang, 3Blue1Brown, Boyd) para fixar a intuição geométrica. |
| **Quarta-feira** | Exercícios no Papel (Bloco 1) | Resolução de exercícios mecânicos e de fixação no caderno/folha. |
| **Quinta-feira** | Exercícios no Papel (Bloco 2) | Demonstrações, provas e problemas mais elaborados de fim de capítulo. |
| **Sexta-feira** | Validação em Código | Criar scripts em Python dentro da pasta da fase correspondente validando os conceitos numericamente. |
| **Sábado** | Revisão Ativa & Síntese | Escrever o resumo da semana em Markdown na pasta do módulo e resolver pendências. |
| **Domingo** | Descanso / Leitura Livre | Descanso mental ou leitura de artigos sem compromisso de exercícios. |

---

## 🗂️ 5. Como Usar esta Pasta `mestrado`

A estrutura de diretórios foi organizada para registrar todo o seu ciclo de preparação até a defesa da dissertação:

```text
/home/silas/Documents/mestrado/
├── PLANO_DE_ESTUDOS.md                                # Este documento (plano mestre)
├── 00_nivelamento_pre_calculo/                        # Notas, exercícios e resumos de lógica e pré-cálculo
├── 01_calculo_univariavel/                            # Limites, derivadas, integrais e Taylor
├── 02_algebra_linear/                                 # Espaços vetoriais, SVD, autovalores, códigos NumPy
├── 03_calculo_multivariavel_otimizacao/               # Gradientes, Hessianas, KKT, códigos de otimização
├── 04_probabilidade_estatistica/                      # Variáveis aleatórias, Gaussianas multivariadas, MLE/MAP
├── 05_otimizacao_combinatoria_pesquisa_operacional/   # Modelos PL/MIP, TSP/VRP, heurísticas e OR-Tools
├── artigos_e_propostas/                               # Papers dos professores, editais e PDF original
└── anotacoes_gerais/                                  # Resumos de reuniões, ideias de projeto e atas
```

---

## 🎯 6. Checklist Global de Progresso

- [ ] **Fase 0: Nivelamento e Pré-Cálculo**
  - [ ] Semana 1: Lógica, Técnicas de Prova e Conjuntos
  - [ ] Semana 2: Somatórios, Produtórios, Inequações e Geometria Analítica
  - [ ] Semana 3: Funções Injetoras/Sobrejetoras, Exponenciais, Logaritmos e Assíntotas
- [ ] **Fase 1: Cálculo I (Univariável)**
  - [ ] Semana 4: Limites, Continuidade e TVI
  - [ ] Semana 5: Derivadas e Regra da Cadeia
  - [ ] Semana 6: Máximos, Mínimos, Convexidade 1D e Newton-Raphson
  - [ ] Semana 7: Integrais, TFC e Técnicas de Integração
  - [ ] Semana 8: Sequências, Séries e Polinômios de Taylor
- [ ] **Fase 2: Álgebra Linear**
  - [ ] Semana 9: Eliminação Gaussiana e Multiplicação Matricial Avançada
  - [ ] Semana 10: 4 Subespaços Fundamentais e Teorema Posto-Nulidade
  - [ ] Semana 11: Transformações Lineares e Mudança de Base
  - [ ] Semana 12: Ortogonalidade, Projeções e Mínimos Quadrados (OLS)
  - [ ] Semana 13: Determinantes e Autovalores/Autovetores
  - [ ] Semana 14: Matrizes Simétricas, Teorema Espectral e Positividade Definida
  - [ ] Semana 15: Decomposição em Valores Singulares (SVD) e PCA
  - [ ] Semana 16: Normas Vetoriais/Matriciais e Estabilidade Numérica
- [ ] **Fase 3: Cálculo Multivariável & Otimização Convexa**
  - [ ] Semana 17: Gradientes, Derivadas Direcionais e Superfícies
  - [ ] Semana 18: Jacobiana, Hessiana, Regra da Cadeia Matricial e Taylor 2D
  - [ ] Semana 19: Conjuntos Convexos e Funções Convexas
  - [ ] Semana 20: Algoritmos de Otimização (Gradient Descent, SGD, Newton)
  - [ ] Semana 21: Multiplicadores de Lagrange
  - [ ] Semana 22: Dualidade de Lagrange e Condições KKT
- [ ] **Fase 4: Probabilidade e Estatística**
  - [ ] Semana 23: Axiomas, Bayes e Probabilidade Condicional
  - [ ] Semana 24: Variáveis Aleatórias, PMF/PDF/CDF, Esperança e Variância
  - [ ] Semana 25: Distribuição Conjunta e Gaussiana Multivariada
  - [ ] Semana 26: Desigualdades (Markov, Chebyshev, Jensen) e TCL
  - [ ] Semana 27: Estimação de Parâmetros: MLE e MAP
  - [ ] Semana 28: Cadeias de Markov e Distribuições Estacionárias
- [ ] **Fase 5: Otimização Combinatória e Pesquisa Operacional**
  - [ ] Semana 29: Teoria dos Grafos (Árvores Geradoras e Caminhos Mínimos)
  - [ ] Semana 30: Fluxos em Redes e Emparelhamento
  - [ ] Semana 31: Programação Linear, Poliedros e o Método Simplex
  - [ ] Semana 32: Dualidade em PL, Preços-Sombra e Folgas Complementares
  - [ ] Semana 33: Programação Inteira Mista (MIP) e Modelagem Lógica
  - [ ] Semana 34: Formulação do TSP e VRP (MTZ vs. DFJ)
  - [ ] Semana 35: Branch and Bound e Planos de Corte
  - [ ] Semana 36: Heurísticas (ILS, ALNS) e Integração de IA com Otimização
