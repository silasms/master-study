# Semana 1: Linguagem Matemática, Lógica e Técnicas de Demonstração
**Pasta:** `00_nivelamento_pre_calculo/`  
**Objetivo:** Construir uma base sólida, consciente e sem pressa em lógica formal, operações de conjuntos e nos quatro métodos essenciais de demonstração matemática, utilizando apenas aritmética e propriedades elementares dos números.

---

## 📖 1. Teoria Completa da Semana

Toda a matemática avançada (seja em Otimização, Cálculo ou Aprendizado de Máquina) é escrita na linguagem da **Lógica Proposicional**, **Quantificadores** e **Teoria dos Conjuntos**. Dominar essas ferramentas elimina qualquer sensação de "travar" na leitura de definições e teoremas.

---

### 1.1 Lógica Proposicional

* **Proposição ($P, Q$):** É uma sentença declarativa que possui valor lógico bem definido: ou é **Verdadeira ($V$)** ou é **Falsa ($F$)**, nunca ambas simultaneamente.
  * *Exemplo de proposição:* "7 é um número primo" (Verdadeira).
  * *Não é proposição:* "Qual é o valor de $x$?" (Pergunta) ou "$x + 2 = 5$" (Sentença aberta; só vira proposição quando especificamos o valor de $x$).

#### Conectivos Lógicos Fundamentais:

1. **Negação ($\neg P$ ou $\sim P$):** Inverte o valor-verdade.
   * Se $P$ é $V$, $\neg P$ é $F$. Se $P$ é $F$, $\neg P$ é $V$.

2. **Conjunção ($P \land Q$ - "e"):**
   * É verdadeira **apenas** quando $P$ e $Q$ são simultaneamente verdadeiros. Se qualquer um for falso, a conjunção é falsa.

3. **Disjunção ($P \lor Q$ - "ou"):**
   * É verdadeira quando **pelo menos um** dos dois é verdadeiro. Só é falsa quando ambos forem falsos.

4. **Condicional / Implicação ($P \implies Q$ - "Se $P$, então $Q$"):**
   * $P$ é chamado de **hipótese** (ou antecedente); $Q$ é a **tese** (ou consequente).
   * **Atenção à regra da implicação:** Uma promessa só é quebrada se a hipótese acontecer e a tese falhar!
     * Se $P$ é $V$ e $Q$ é $V \implies P \implies Q$ é **$V$**.
     * Se $P$ é $V$ e $Q$ é $F \implies P \implies Q$ é **$F$** (único caso de falsidade).
     * Se $P$ é $F$ e $Q$ é $V \implies P \implies Q$ é **$V$** (*verdade por vacuidade*).
     * Se $P$ é $F$ e $Q$ é $F \implies P \implies Q$ é **$V$**.
   * **Equivalência da Implicação:**
     $$P \implies Q \quad \equiv \quad \neg P \lor Q$$
   * **Negação da Implicação (Regra de Ouro):**
     $$\neg (P \implies Q) \quad \equiv \quad P \land \neg Q$$
     *(Para desmentir "Se chover, levo guarda-chuva", você precisa mostrar que choveu E você NÃO levou guarda-chuva).*

5. **Bicondicional / Dupla Implicação ($P \iff Q$ - "$P$ se, e somente se, $Q$"):**
   * É verdadeira quando $P$ e $Q$ possuem o mesmo valor lógico (ambos $V$ ou ambos $F$).
   * Equivale a afirmar as duas direções simultaneamente: $(P \implies Q) \land (Q \implies P)$.

#### Tabela-Verdade Resumida:

| $P$ | $Q$ | $\neg P$ | $P \land Q$ | $P \lor Q$ | $P \implies Q$ | $P \iff Q$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| $V$ | $V$ | $F$ | $V$ | $V$ | $V$ | $V$ |
| $V$ | $F$ | $F$ | $F$ | $V$ | $F$ | $F$ |
| $F$ | $V$ | $V$ | $F$ | $V$ | $V$ | $F$ |
| $F$ | $F$ | $V$ | $F$ | $F$ | $V$ | $V$ |

#### Leis de De Morgan para Proposições:
* $\neg(P \land Q) \equiv \neg P \lor \neg Q$
* $\neg(P \lor Q) \equiv \neg P \land \neg Q$

---

### 1.2 Quantificadores e Sentenças Abertas

Quando temos uma sentença que depende de uma variável, como $P(x)$: "$x$ é par", o valor lógico depende do conjunto universo onde $x$ reside. Usamos **quantificadores**:

1. **Quantificador Universal ($\forall$ - "Para todo", "Para qualquer"):**
   * $\forall x \in S, P(x)$: afirma que a propriedade $P(x)$ é verdadeira para **todos** os elementos do conjunto $S$.
   * Para provar que é falsa, basta exibir um único **contraexemplo** em $S$.
eoria Completa da Sem
2. **Quantificador Existencial ($\exists$ - "Existe pelo menos um"):**
   * $\exists x \in S \text{ tal que } P(x)$: afirma que há pelo menos um elemento em $S$ que satisfaz $P(x)$.
   * Para provar que é verdadeira, basta exibir **um exemplo**.

3. **Negação de Quantificadores (Regras de De Morgan com Quantificadores):**
   * Para negar que "todo elemento satisfaz $P$", basta dizer que "existe alguém que NÃO satisfaz $P$":
     $$\neg (\forall x \in S, P(x)) \quad \equiv \quad \exists x \in S \text{ tal que } \neg P(x)$$
   * Para negar que "existe algum elemento que satisfaz $P$", devemos afirmar que "todos os elementos NÃO satisfazem $P$":
     $$\neg (\exists x \in S \text{ tal que } P(x)) \quad \equiv \quad \forall x \in S, \neg P(x)$$

---

### 1.3 Teoria Elementar de Conjuntos

* **Conjuntos Numéricos Fundamentais:**
  * Naturais: $\mathbb{N} = \{1, 2, 3, \dots\}$ (ou incluindo o 0).
  * Inteiros: $\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}$.
  * Racionais: $\mathbb{Q} = \{ \frac{a}{b} \mid a, b \in \mathbb{Z}, b \neq 0 \}$.
  * Reais: $\mathbb{R}$ (inclui racionais e irracionais como $\sqrt{2}, \pi, e$).
* **Relações de Pertinência e Inclusão:**
  * Pertinência: $x \in A$ ($x$ é elemento de $A$); $x \notin A$ ($x$ não pertence a $A$).
  * Inclusão (Subconjunto): $A \subseteq B \iff (\forall x, x \in A \implies x \in B)$.
  * Igualdade de Conjuntos: $A = B \iff (A \subseteq B \land B \subseteq A)$.
* **Operações entre Conjuntos:**
  * **União ($A \cup B$):** $\{x \mid x \in A \lor x \in B\}$.
  * **Interseção ($A \cap B$):** $\{x \mid x \in A \land x \in B\}$. Se $A \cap B = \emptyset$, os conjuntos são disjuntos.
  * **Diferença ($A \setminus B$):** $\{x \mid x \in A \land x \notin B\}$.
  * **Complementar ($A^c$ ou $\overline{A}$ em relação a um universo $U$):** $\{x \in U \mid x \notin A\}$.
  * **Produto Cartesiano ($A \times B$):** $\{(a, b) \mid a \in A \land b \in B\}$.
* **Leis de De Morgan para Conjuntos:**
  * $(A \cup B)^c = A^c \cap B^c$
  * $(A \cap B)^c = A^c \cup B^c$

---

### 1.4 Definições Aritméticas Básicas Utilizadas nas Demonstrações

Para demonstrar afirmações sem misturar outras matérias, usaremos apenas definições da aritmética dos inteiros e racionais:

1. **Paridade:**
   * Um inteiro $n \in \mathbb{Z}$ é **par** se existe $k \in \mathbb{Z}$ tal que $n = 2k$.
   * Um inteiro $n \in \mathbb{Z}$ é **ímpar** se existe $k \in \mathbb{Z}$ tal que $n = 2k + 1$.
   * *Propriedade fundamental:* Todo número inteiro é ou exclusivamente par ou exclusivamente ímpar.

2. **Divisibilidade:**
   * Sejam $a, b \in \mathbb{Z}$ com $a \neq 0$. Dizemos que **$a$ divide $b$** (denotado por $a \mid b$) se existe um inteiro $k \in \mathbb{Z}$ tal que:
     $$b = a \cdot k$$
   * Exemplo: $3 \mid 12$ porque $12 = 3 \cdot 4$.

3. **Número Racional:**
   * Um número $x$ é racional ($x \in \mathbb{Q}$) se e somente se existem inteiros $a, b \in \mathbb{Z}$ com $b \neq 0$ tais que $x = \frac{a}{b}$. Podemos sempre assumir a fração irredutível, isto é, com $\operatorname{mdc}(a, b) = 1$.
   * Se um número real não pode ser escrito dessa forma, ele é **irracional**.

---

### 1.5 As Quatro Técnicas Fundamentais de Demonstração

#### Técnica 1: Prova Direta
* **Objetivo:** Provar uma implicação $P \implies Q$.
* **Como fazer:**
  1. Assuma que a hipótese $P$ é verdadeira.
  2. Use as definições matemáticas de $P$ (por exemplo, se $n$ é par, escreva $n = 2k$).
  3. Realize manipulações algébricas até chegar na forma da tese $Q$.
  4. Conclua que $Q$ é verdadeira.

#### Técnica 2: Prova por Contrapositiva
* **Fundamento:** A implicação $P \implies Q$ é **logicamente equivalente** a $\neg Q \implies \neg P$.
* **Quando usar:** Quando a negação da tese $\neg Q$ for mais fácil de manipular algebricamente do que a hipótese direta $P$.
* **Como fazer:**
  1. Identifique $P$ e $Q$.
  2. Escreva as negações $\neg Q$ e $\neg P$.
  3. Assuma que $\neg Q$ é verdadeira como sua nova hipótese de partida.
  4. Demonstre diretamente que $\neg P$ é consequência necessária.
  5. Conclua: como provamos $\neg Q \implies \neg P$, o teorema original $P \implies Q$ está provado.

#### Técnica 3: Prova por Contradição (*Reductio ad Absurdum*)
* **Fundamento:** Para provar que uma afirmação $P$ é verdadeira, assumimos que ela é falsa ($\neg P$) e mostramos que isso gera uma impossibilidade lógica irrefutável (como $0 = 1$, um número ser par e ímpar ao mesmo tempo, ou $A \land \neg A$).
* **Como fazer:**
  1. Escreva: *"Suponha, por absurdo, que a afirmação seja falsa"* (isto é, assuma $\neg P$).
  2. Trabalhe dedutivamente a partir dessa suposição usando propriedades válidas.
  3. Chegue a uma contradição explícita com alguma premissa estabelecida ou com um axioma da matemática.
  4. Conclua: *"Portanto, a suposição de que $P$ é falsa é impossível. Logo, $P$ é verdadeira"*.

#### Técnica 4: Princípio da Indução Matemática (PIM)
* **Objetivo:** Provar que uma propriedade $P(n)$ é verdadeira para todos os inteiros $n \ge n_0$ (geralmente $n \ge 1$).
* **Analogia:** Efeito dominó. Você derruba o primeiro dominó (base), e garante que qualquer dominó que cai derruba o próximo (passo indutivo).
* **Estrutura rigorosa em 3 passos:**
  1. **Passo 1 (Caso Base):** Verifique explicitamente que $P(n_0)$ é verdadeiro calculando os dois lados da igualdade para $n = n_0$.
  2. **Passo 2 (Hipótese Indutiva - HI):** Assuma que a afirmação é verdadeira para um número fixo e arbitrário $k \ge n_0$. Escreva explicitamente a fórmula para $k$: *"Assumimos que $P(k)$ vale"*.
  3. **Passo 3 (Passo Indutivo):** Mostre que, **usando obrigatoriamente a Hipótese Indutiva**, decorre que $P(k+1)$ também é verdadeira.
  4. **Conclusão:** Pelo PIM, a propriedade $P(n)$ vale para todo $n \ge n_0$.

---

## 📝 2. Exercícios da Semana 1 (Curva Gradual de Aprendizado)

Os exercícios estão organizados em 7 blocos progressivos. Cada bloco foca estritamente nos conceitos apresentados acima, partindo de fixação direta até demonstrações estruturadas no caderno.

---

### Bloco I: Lógica Proposicional e Tabelas-Verdade (Fixação)
*Objetivo: Dominar os conectivos e a equivalência fundamental da implicação.*

1. **Construção de Tabela-Verdade:** Construa a tabela-verdade completa para a fórmula proposicional:
   $$(P \implies Q) \land P$$
   Em quais linhas da tabela essa expressão resulta em Verdadeiro ($V$)? O que isso nos diz sobre a dedução lógica (*Modus Ponens*)?

2. **Equivalência da Implicação:** Construa lado a lado as tabelas-verdade de:
   * Proposição A: $P \implies Q$
   * Proposição B: $\neg P \lor Q$  
   Verifique linha por linha que ambas possuem exatamente a mesma coluna de resultados (provando que $P \implies Q \equiv \neg P \lor Q$).

3. **Negação de Sentenças Simples:** Escreva a negação formal das seguintes proposições em linguagem natural:
   * (a) "Hoje é sábado e vai fazer sol."
   * (b) "Se o número $x$ é primo, então $x$ é ímpar." *(Lembre-se: $\neg(P \implies Q) \equiv P \land \neg Q$)*.
   * (c) "Vou estudar no papel ou vou programar em Python."

---

### Bloco II: Quantificadores e Sentenças Abertas (Intermediário I)
*Objetivo: Ganhar fluência com $\forall, \exists$ e suas negações sem sair dos conjuntos numéricos básicos.*

4. **Verdadeiro ou Falso com Justificativa:** Determine se cada afirmação abaixo é verdadeira ou falsa nos conjuntos numéricos indicados. Se for falsa, exiba um contraexemplo:
   * (a) $\forall x \in \mathbb{R}, \; x^2 > 0$
   * (b) $\forall x \in \mathbb{R}, \; x^2 \ge 0$
   * (c) $\exists x \in \mathbb{Z} \text{ tal que } 2x = 1$
   * (d) $\forall x \in \mathbb{Z}, \; \exists y \in \mathbb{Z} \text{ tal que } x + y = 0$

5. **Negação com Quantificadores:** Aplique as regras de De Morgan para escrever a negação formal de cada proposição (trocando os quantificadores e negando a condição interna):
   * (a) $\forall x \in \mathbb{N}, \; x \ge 1$
   * (b) $\exists x \in \mathbb{R} \text{ tal que } x^2 + 1 = 0$
   * (c) $\forall x \in \mathbb{Z}, \; (x \text{ é par} \implies x^2 \text{ é par})$

---

### Bloco III: Teoria de Conjuntos (Intermediário II)
*Objetivo: Manipular pertinência, subconjuntos e operações booleanas de conjuntos.*

6. **Operações Básicas:** Sejam os conjuntos universo $U = \{1, 2, 3, 4, 5, 6, 7, 8\}$, $A = \{2, 4, 6, 8\}$ e $B = \{1, 2, 3, 4\}$. Encontre explicitamente:
   * (a) $A \cup B$
   * (b) $A \cap B$
   * (c) $A \setminus B$ e $B \setminus A$
   * (d) O complementar $A^c$ em relação a $U$.

7. **Dupla Inclusão para Prova de Conjuntos:** Prove formalmente que, para quaisquer conjuntos $A$ e $B$:
   $$A \cap B = B \cap A$$
   *(Estrutura da prova: mostre que $x \in A \cap B \implies x \in B \cap A$, e vice-versa).*

8. **Produto Cartesiano:** Sejam $A = \{1, 2\}$ e $B = \{x, y, z\}$.
   * (a) Escreva todos os elementos do conjunto $A \times B$.
   * (b) Qual é a cardinalidade (número de elementos) de $A \times B$? Qual regra geral relaciona $|A \times B|$ a $|A|$ e $|B|$?

---

### Bloco IV: Prova Direta (Demonstrações no Caderno)
*Objetivo: Escrever argumentos dedutivos lineares a partir de definições aritméticas.*

9. **Soma de Números Pares:** Prove diretamente que a soma de dois números inteiros pares é sempre um número inteiro par.
   *(Hipótese: $a = 2k_1$ e $b = 2k_2$. Tese: $a + b = 2m$).*

10. **Paridade de Produto:** Prove diretamente que o produto de dois números inteiros ímpares é sempre um número inteiro ímpar.

11. **Transitividade da Divisibilidade:** Sejam $a, b, c \in \mathbb{Z}$ com $a \neq 0$ e $b \neq 0$. Prove diretamente que:
    $$\text{Se } a \mid b \text{ e } b \mid c, \text{ então } a \mid c$$

12. **Soma de Dois Racionais:** Prove diretamente a partir da definição de $\mathbb{Q}$ que a soma de dois números racionais é sempre um número racional.

---

### Bloco V: Prova por Contrapositiva (Demonstrações no Caderno)
*Objetivo: Aprender a inverter a implicação quando a hipótese original é difícil de desmembrar.*

13. **Paridade Quadrática Clássica:** Sejam $n \in \mathbb{Z}$. Prove por contrapositiva que:
    $$\text{Se } n^2 \text{ é par, então } n \text{ é par}$$
    *(Enuncie a contrapositiva claramente antes de iniciar a demonstração).*

14. **Expressão Linear e Paridade:** Seja $n \in \mathbb{Z}$. Prove por contrapositiva que:
    $$\text{Se } 3n + 2 \text{ é ímpar, então } n \text{ é ímpar}$$

15. **Desigualdade com Soma:** Sejam $x, y \in \mathbb{R}$. Prove por contrapositiva que:
    $$\text{Se } x + y \ge 10, \text{ então } x \ge 5 \text{ ou } y \ge 5$$
    *(Dica: use a Lei de De Morgan para negar "x $\ge$ 5 ou y $\ge$ 5").*

---

### Bloco VI: Prova por Contradição (Demonstrações no Caderno)
*Objetivo: Assumir o absurdo e derivar uma quebra lógica irrefutável.*

16. **Não Existência do Maior Inteiro:** Prove por contradição que não existe um "maior número inteiro".
    *(Assuma que existe um inteiro $M$ tal que $M \ge n$ para todo $n \in \mathbb{Z}$, e analise $M + 1$).*

17. **Soma de Racional com Irracional:** Prove por contradição que a soma de um número racional com um número irracional é sempre um número irracional.
    *(Assuma que $r \in \mathbb{Q}$, $x \notin \mathbb{Q}$, e que a soma $s = r + x$ é racional).*

18. **Irracionalidade de $\sqrt{2}$ (O Teorema Clássico):** Prove por contradição que $\sqrt{2}$ não é um número racional.
    *(Siga o roteiro: assuma $\sqrt{2} = \frac{a}{b}$ irredutível, eleve ao quadrado, use a propriedade do exercício 13 sobre paridade e deduza que $a$ e $b$ são ambos pares, contradizendo a irredutibilidade).*

---

### Bloco VII: Princípio da Indução Matemática (Demonstrações no Caderno)
*Objetivo: Praticar a técnica do dominó para fórmulas fechadas e propriedades dos números naturais.*

19. **A Soma dos Primeiros $n$ Números Naturais:** Usando indução matemática, prove que para todo $n \ge 1$:
    $$\sum_{i=1}^{n} i = 1 + 2 + 3 + \dots + n = \frac{n(n+1)}{2}$$

20. **Soma dos Primeiros $n$ Números Ímpares:** Usando indução matemática, prove que para todo $n \ge 1$:
    $$1 + 3 + 5 + \dots + (2n - 1) = \sum_{i=1}^{n} (2i - 1) = n^2$$

21. **Soma de Potências de 2:** Usando indução matemática, prove que para todo $n \ge 1$:
    $$1 + 2 + 4 + \dots + 2^{n-1} = \sum_{i=1}^{n} 2^{i-1} = 2^n - 1$$

22. **Desigualdade com Indução:** Usando indução matemática, prove que para todo número natural $n \ge 1$:
    $$2^n > n$$

---

## 🧭 Como Estudar Esta Semana no Seu Ritmo
1. Leia as seções de teoria prestando atenção nas definições em caixas e tabelas.
2. Pegue seu caderno de estudos e faça os exercícios em ordem:
   * Os **Blocos I e II** são rápidos, para aquecer o cérebro com símbolos e tabelas.
   * O **Bloco III** firma a linguagem de conjuntos.
   * Os **Blocos IV, V, VI e VII** são onde você desenvolve a escrita formal das 4 técnicas de prova.
3. Se travar em algum passo, não se preocupe! Consulte o arquivo de soluções completas passo a passo:  
   👉 **[`semana_01_resolucoes.md`](file:///home/silas/Documents/mestrado/00_nivelamento_pre_calculo/semana_01_resolucoes.md)**
