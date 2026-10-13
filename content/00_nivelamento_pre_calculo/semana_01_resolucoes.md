# Resoluções Comentadas Passo a Passo – Semana 1
**Pasta:** `00_nivelamento_pre_calculo/`  
**Objetivo:** Servir como guia de consulta e correção consciente para os exercícios do arquivo [`semana_01_logica_e_demonstracoes.md`](./semana_01_logica_e_demonstracoes.md).

---

## 📌 Bloco I: Lógica Proposicional e Tabelas-Verdade

---

### Questão 1: Tabela-Verdade de $(P \implies Q) \land P$

> **Enunciado:** Construa a tabela-verdade completa para a fórmula proposicional $(P \implies Q) \land P$. Em quais linhas da tabela essa expressão resulta em Verdadeiro ($V$)? O que isso nos diz sobre a dedução lógica (*Modus Ponens*)?

#### 1. Construção Passo a Passo da Tabela-Verdade

Listamos todas as 4 combinações possíveis para as proposições primitivas $P$ e $Q$:

| Linha | $P$ | $Q$ | $P \implies Q$ | $(P \implies Q) \land P$ |
| :---: | :---: | :---: | :---: | :---: |
| 1 | $V$ | $V$ | $V$ | **$V$** |
| 2 | $V$ | $F$ | $F$ | **$F$** |
| 3 | $F$ | $V$ | $V$ | **$F$** |
| 4 | $F$ | $F$ | $V$ | **$F$** |

* Detalhe da Linha 1: $P \implies Q$ é $V$; como $P$ é $V$, temos $V \land V \implies V$.
* Detalhe da Linha 2: $P \implies Q$ é $F$; $F \land V \implies F$.
* Detalhe da Linha 3: $P \implies Q$ é $V$, mas $P$ é $F$; $V \land F \implies F$.
* Detalhe da Linha 4: $P \implies Q$ é $V$, mas $P$ é $F$; $V \land F \implies F$.

#### 2. Análise do Resultado e Modus Ponens
A expressão só é verdadeira na **Linha 1**, que é exatamente a linha onde **$Q$ também é verdadeiro**.  
Isso fundamenta a regra de dedução clássica chamada **Modus Ponens**:
$$\text{Se sabemos que } P \implies Q \text{ é verdade, e sabemos que } P \text{ é verdade, somos obrigados a concluir que } Q \text{ é verdade.}$$

---

### Questão 2: Equivalência Lógica $P \implies Q \equiv \neg P \lor Q$

> **Enunciado:** Construa lado a lado as tabelas-verdade de $P \implies Q$ e $\neg P \lor Q$. Verifique que ambas possuem exatamente a mesma coluna de resultados.

#### 1. Tabela Comparativa

| $P$ | $Q$ | $\neg P$ | $P \implies Q$ | $\neg P \lor Q$ |
| :---: | :---: | :---: | :---: | :---: |
| $V$ | $V$ | $F$ | **$V$** | $F \lor V \equiv$ **$V$** |
| $V$ | $F$ | $F$ | **$F$** | $F \lor F \equiv$ **$F$** |
| $F$ | $V$ | $V$ | **$V$** | $V \lor V \equiv$ **$V$** |
| $F$ | $F$ | $V$ | **$V$** | $V \lor F \equiv$ **$V$** |

#### 2. Conclusão
Comparando as duas últimas colunas, os valores-verdade são idênticos em todas as 4 linhas: $(V, F, V, V)$.  
Portanto, as duas proposições são **logicamente equivalentes**:
$$P \implies Q \quad \equiv \quad \neg P \lor Q$$

---

### Questão 3: Negação de Sentenças Simples em Linguagem Natural

> **Enunciado:** Escreva a negação formal das seguintes proposições:
> * (a) "Hoje é sábado e vai fazer sol."
> * (b) "Se o número $x$ é primo, então $x$ é ímpar."
> * (c) "Vou estudar no papel ou vou programar em Python."

#### Resolução:

* **Item (a):**
  * Estrutura: $P \land Q$, onde $P$ = "Hoje é sábado" e $Q$ = "vai fazer sol".
  * Regra de De Morgan: $\neg(P \land Q) \equiv \neg P \lor \neg Q$.
  * **Resposta:** *"Hoje não é sábado **ou** não vai fazer sol."*

* **Item (b):**
  * Estrutura: $P \implies Q$, onde $P$ = "o número $x$ é primo" e $Q$ = "$x$ é ímpar".
  * Regra da negação da implicação: $\neg(P \implies Q) \equiv P \land \neg Q$.
  * **Resposta:** *"O número $x$ é primo **e** $x$ não é ímpar (isto é, $x$ é par)."*  
    *(Nota: este contraexemplo existe de fato na matemática: o número 2!)*

* **Item (c):**
  * Estrutura: $P \lor Q$, onde $P$ = "Vou estudar no papel" e $Q$ = "vou programar em Python".
  * Regra de De Morgan: $\neg(P \lor Q) \equiv \neg P \land \neg Q$.
  * **Resposta:** *"Não vou estudar no papel **e** não vou programar em Python."*

---

## 📌 Bloco II: Quantificadores e Sentenças Abertas

---

### Questão 4: Análise de Proposições com Quantificadores

> **Enunciado:** Determine se cada afirmação é verdadeira ou falsa. Se for falsa, exiba um contraexemplo:
> * (a) $\forall x \in \mathbb{R}, \; x^2 > 0$
> * (b) $\forall x \in \mathbb{R}, \; x^2 \ge 0$
> * (c) $\exists x \in \mathbb{Z} \text{ tal que } 2x = 1$
> * (d) $\forall x \in \mathbb{Z}, \; \exists y \in \mathbb{Z} \text{ tal que } x + y = 0$

#### Resolução:

* **Item (a): FALSA.**
  * *Contraexemplo:* Tome $x = 0 \in \mathbb{R}$. Temos $0^2 = 0$, e $0$ **não é estritamente maior que 0** ($0 > 0$ é falso). Logo, a afirmação não vale para todo $x$.

* **Item (b): VERDADEIRA.**
  * *Justificativa:* O quadrado de qualquer número real é sempre maior ou igual a zero (se $x > 0$, $x^2 > 0$; se $x < 0$, $(-x)^2 > 0$; se $x = 0$, $x^2 = 0$).

* **Item (c): FALSA.**
  * *Justificativa:* A equação $2x = 1$ tem como única solução $x = \frac{1}{2}$. Como $\frac{1}{2} \notin \mathbb{Z}$ (não é um número inteiro), não existe nenhum inteiro que satisfaça a equação.

* **Item (d): VERDADEIRA.**
  * *Justificativa:* Dado qualquer $x \in \mathbb{Z}$, basta escolher $y = -x$. Como o inverso aditivo de qualquer inteiro também é um inteiro (isto é, $-x \in \mathbb{Z}$), temos $x + (-x) = 0$.

---

### Questão 5: Negações Formais com Quantificadores

> **Enunciado:** Escreva a negação formal das seguintes proposições:
> * (a) $\forall x \in \mathbb{N}, \; x \ge 1$
> * (b) $\exists x \in \mathbb{R} \text{ tal que } x^2 + 1 = 0$
> * (c) $\forall x \in \mathbb{Z}, \; (x \text{ é par} \implies x^2 \text{ é par})$

#### Resolução:

* **Item (a):**
  * Proposição original: $\forall x \in \mathbb{N}, \; x \ge 1$.
  * Negação: trocamos $\forall$ por $\exists$ e negamos a condição $x \ge 1$ (cuja negação é $x < 1$).
  * **Resposta:** $\exists x \in \mathbb{N} \text{ tal que } x < 1$.

* **Item (b):**
  * Proposição original: $\exists x \in \mathbb{R} \text{ tal que } x^2 + 1 = 0$.
  * Negação: trocamos $\exists$ por $\forall$ e negamos a igualdade $=$ (virando $\neq$).
  * **Resposta:** $\forall x \in \mathbb{R}, \; x^2 + 1 \neq 0$.

* **Item (c):**
  * Proposição original: $\forall x \in \mathbb{Z}, \; (P(x) \implies Q(x))$, onde $P(x)$: "$x$ é par" e $Q(x)$: "$x^2$ é par".
  * Passo 1: O quantificador $\forall$ vira $\exists$.
  * Passo 2: Negamos a implicação interna: $\neg(P \implies Q) \equiv P \land \neg Q$.
  * **Resposta:** $\exists x \in \mathbb{Z} \text{ tal que } (x \text{ é par} \land x^2 \text{ é ímpar})$.

---

## 📌 Bloco III: Teoria de Conjuntos

---

### Questão 6: Operações Básicas de Conjuntos

> **Enunciado:** Dados $U = \{1, 2, 3, 4, 5, 6, 7, 8\}$, $A = \{2, 4, 6, 8\}$ e $B = \{1, 2, 3, 4\}$. Encontre:
> * (a) $A \cup B$
> * (b) $A \cap B$
> * (c) $A \setminus B$ e $B \setminus A$
> * (d) $A^c$

#### Resolução:

* **(a) União ($A \cup B$):** Todos os elementos que estão em $A$ ou em $B$:
  $$A \cup B = \{1, 2, 3, 4, 6, 8\}$$

* **(b) Interseção ($A \cap B$):** Elementos comuns a ambos:
  $$A \cap B = \{2, 4\}$$

* **(c) Diferença:**
  * $A \setminus B$ (estão em $A$, mas não estão em $B$): eliminando 2 e 4 de $A$, sobram:
    $$A \setminus B = \{6, 8\}$$
  * $B \setminus A$ (estão em $B$, mas não estão em $A$): eliminando 2 e 4 de $B$, sobram:
    $$B \setminus A = \{1, 3\}$$

* **(d) Complementar ($A^c$ em relação a $U$):** Todos os elementos de $U$ que não estão em $A$:
  $$A^c = U \setminus A = \{1, 3, 5, 7\}$$

---

### Questão 7: Demonstração de Igualdade por Dupla Inclusão

> **Enunciado:** Prove formalmente que $A \cap B = B \cap A$.

#### Demonstração Formal:
Para provar que dois conjuntos são iguais, devemos provar duas inclusões: $A \cap B \subseteq B \cap A$ e $B \cap A \subseteq A \cap B$.

* **Parte 1: Provar que $A \cap B \subseteq B \cap A$**
  1. Seja $x$ um elemento arbitrário tal que $x \in A \cap B$.
  2. Pela definição de interseção, isso significa que $(x \in A) \land (x \in B)$.
  3. Pela comutatividade da conjunção lógica ($P \land Q \equiv Q \land P$), isso é equivalente a $(x \in B) \land (x \in A)$.
  4. Pela definição de interseção, isso significa que $x \in B \cap A$.
  5. Como todo elemento de $A \cap B$ pertence a $B \cap A$, concluímos que $A \cap B \subseteq B \cap A$.

* **Parte 2: Provar que $B \cap A \subseteq A \cap B$**
  1. O argumento é análogo: se $x \in B \cap A$, então $(x \in B) \land (x \in A) \implies (x \in A) \land (x \in B) \implies x \in A \cap B$.
  2. Logo, $B \cap A \subseteq A \cap B$.

* **Conclusão:**  
  Como $A \cap B \subseteq B \cap A$ e $B \cap A \subseteq A \cap B$, segue que $A \cap B = B \cap A$. $\blacksquare$

---

### Questão 8: Produto Cartesiano e Cardinalidade

> **Enunciado:** Sejam $A = \{1, 2\}$ e $B = \{x, y, z\}$.
> * (a) Escreva todos os elementos do conjunto $A \times B$.
> * (b) Qual é a cardinalidade $|A \times B|$? Qual a regra geral?

#### Resolução:

* **(a) Elementos de $A \times B$:** Pares ordenados $(a, b)$ com $a \in A$ e $b \in B$:
  $$A \times B = \{ (1, x), \; (1, y), \; (1, z), \; (2, x), \; (2, y), \; (2, z) \}$$

* **(b) Cardinalidade:**
  * Contando os elementos explicitamente: $|A \times B| = 6$.
  * Como $|A| = 2$ e $|B| = 3$, observamos que $6 = 2 \times 3$.
  * **Regra Geral (Princípio Multiplicativo):** Para quaisquer conjuntos finitos $A$ e $B$:
    $$|A \times B| = |A| \cdot |B|$$

---

## 📌 Bloco IV: Prova Direta

---

### Questão 9: Soma de Dois Números Pares

> **Enunciado:** Prove diretamente que a soma de dois números inteiros pares é sempre um número inteiro par.

#### Demonstração Formal:
1. **Hipótese:** Sejam $a$ e $b$ dois números inteiros pares arbitrários.
2. **Uso da Definição:**  
   Pela definição de número par:
   * Existe um inteiro $k_1 \in \mathbb{Z}$ tal que $a = 2k_1$.
   * Existe um inteiro $k_2 \in \mathbb{Z}$ tal que $b = 2k_2$.
3. **Manipulação Algébrica:**  
   Calculamos a soma $a + b$:
   $$a + b = 2k_1 + 2k_2 = 2(k_1 + k_2)$$
4. **Conclusão:**  
   Como $k_1, k_2 \in \mathbb{Z}$, a soma $k_1 + k_2$ é também um número inteiro (denotemos $m = k_1 + k_2 \in \mathbb{Z}$).  
   Logo, $a + b = 2m$.  
   Pela definição de número par, $a + b$ é par. $\blacksquare$

---

### Questão 10: Produto de Dois Números Ímpares

> **Enunciado:** Prove diretamente que o produto de dois números inteiros ímpares é sempre um número inteiro ímpar.

#### Demonstração Formal:
1. **Hipótese:** Sejam $a$ e $b$ dois inteiros ímpares.
2. **Uso da Definição:**  
   Existem inteiros $k_1, k_2 \in \mathbb{Z}$ tais que:
   $$a = 2k_1 + 1 \quad \text{e} \quad b = 2k_2 + 1$$
3. **Manipulação Algébrica:**  
   Multiplicamos $a \cdot b$:
   $$a \cdot b = (2k_1 + 1)(2k_2 + 1) = 4k_1 k_2 + 2k_1 + 2k_2 + 1$$
   Colocando o fator $2$ em evidência nos três primeiros termos:
   $$a \cdot b = 2(2k_1 k_2 + k_1 + k_2) + 1$$
4. **Conclusão:**  
   Defina $m = 2k_1 k_2 + k_1 + k_2$. Como $k_1, k_2 \in \mathbb{Z}$, $m$ é um número inteiro.  
   Portanto, $a \cdot b = 2m + 1$, o que é exatamente a definição de um número ímpar. $\blacksquare$

---

### Questão 11: Transitividade da Divisibilidade

> **Enunciado:** Sejam $a, b, c \in \mathbb{Z}$ com $a \neq 0, b \neq 0$. Prove diretamente que se $a \mid b$ e $b \mid c$, então $a \mid c$.

#### Demonstração Formal:
1. **Hipótese:** $a \mid b$ e $b \mid c$.
2. **Uso da Definição:**
   * $a \mid b \implies$ existe $k_1 \in \mathbb{Z}$ tal que $b = a \cdot k_1$.
   * $b \mid c \implies$ existe $k_2 \in \mathbb{Z}$ tal que $c = b \cdot k_2$.
3. **Substituição e Álgebra:**  
   Substituímos a expressão de $b$ na equação de $c$:
   $$c = (a \cdot k_1) \cdot k_2 = a \cdot (k_1 \cdot k_2)$$
4. **Conclusão:**  
   Como $k_1, k_2 \in \mathbb{Z}$, o produto $k_3 = k_1 \cdot k_2$ é um número inteiro.  
   Logo, $c = a \cdot k_3$, o que satisfaz a definição de divisibilidade: $a \mid c$. $\blacksquare$

---

### Questão 12: Soma de Dois Racionais

> **Enunciado:** Prove diretamente que a soma de dois números racionais é sempre um número racional.

#### Demonstração Formal:
1. **Hipótese:** Sejam $x, y \in \mathbb{Q}$.
2. **Uso da Definição:**  
   Existem inteiros $a, b, c, d \in \mathbb{Z}$ com $b \neq 0$ e $d \neq 0$ tais que:
   $$x = \frac{a}{b} \quad \text{e} \quad y = \frac{c}{d}$$
3. **Manipulação Algébrica:**  
   Somamos as duas frações usando o denominador comum $bd$:
   $$x + y = \frac{a}{b} + \frac{c}{d} = \frac{ad + bc}{bd}$$
4. **Conclusão:**  
   * O numerador $ad + bc$ é um inteiro (soma e produto de inteiros).
   * O denominador $bd$ é um inteiro e $bd \neq 0$ (já que $b \neq 0$ e $d \neq 0$).  
   Como $x + y$ pode ser escrito como a razão de dois inteiros com denominador não nulo, segue que $x + y \in \mathbb{Q}$. $\blacksquare$

---

## 📌 Bloco V: Prova por Contrapositiva

---

### Questão 13: Paridade Quadrática Clássica

> **Enunciado:** Seja $n \in \mathbb{Z}$. Prove por contrapositiva que: se $n^2$ é par, então $n$ é par.

#### Demonstração Formal:
1. **Identificando as Proposições:**
   * $P$: "$n^2$ é par"
   * $Q$: "$n$ é par"
2. **Enunciando a Contrapositiva ($\neg Q \implies \neg P$):**
   * $\neg Q$: "$n$ é ímpar"
   * $\neg P$: "$n^2$ é ímpar"
   * **Declaração a provar:** *"Se $n$ é ímpar, então $n^2$ é ímpar."*
3. **Provando a Contrapositiva:**
   * Assuma que $n$ é ímpar. Pela definição, $n = 2k + 1$ para algum $k \in \mathbb{Z}$.
   * Elevamos ao quadrado:
     $$n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$$
   * Como $2k^2 + 2k \in \mathbb{Z}$, defina $m = 2k^2 + 2k$. Então $n^2 = 2m + 1$, logo $n^2$ é ímpar.
4. **Conclusão:**  
   Como provamos que $\neg Q \implies \neg P$ é verdadeira, pela equivalência lógica da contrapositiva a implicação original $P \implies Q$ é verdadeira: se $n^2$ é par, então $n$ é par. $\blacksquare$

---

### Questão 14: Expressão Linear e Paridade

> **Enunciado:** Seja $n \in \mathbb{Z}$. Prove por contrapositiva que: se $3n + 2$ é ímpar, então $n$ é ímpar.

#### Demonstração Formal:
1. **Identificando as Proposições:**
   * $P$: "$3n + 2$ é ímpar"
   * $Q$: "$n$ é ímpar"
2. **Contrapositiva ($\neg Q \implies \neg P$):**
   * *"Se $n$ é par, então $3n + 2$ é par."*
3. **Provando a Contrapositiva:**
   * Assuma que $n$ é par. Então $n = 2k$ para algum $k \in \mathbb{Z}$.
   * Substituímos na expressão $3n + 2$:
     $$3n + 2 = 3(2k) + 2 = 6k + 2 = 2(3k + 1)$$
   * Como $3k + 1 \in \mathbb{Z}$, a expressão $3n + 2$ é da forma $2m$, logo $3n + 2$ é par.
4. **Conclusão:**  
   Demonstrada a contrapositiva, o teorema original está provado. $\blacksquare$

---

### Questão 15: Desigualdade com Soma

> **Enunciado:** Sejam $x, y \in \mathbb{R}$. Prove por contrapositiva que: se $x + y \ge 10$, então $x \ge 5$ ou $y \ge 5$.

#### Demonstração Formal:
1. **Identificando as Proposições:**
   * Hipótese $P$: $x + y \ge 10$
   * Tese $Q$: $x \ge 5 \lor y \ge 5$
2. **Negando a Tese $\neg Q$ com De Morgan:**
   * $\neg(x \ge 5 \lor y \ge 5) \equiv (x < 5) \land (y < 5)$
3. **Enunciando a Contrapositiva:**
   * *"Se $x < 5$ e $y < 5$, então $x + y < 10$."*
4. **Demonstrando a Contrapositiva:**
   * Assuma que $x < 5$ e $y < 5$.
   * Somando duas desigualdades estritas no mesmo sentido:
     $$x + y < 5 + 5 \implies x + y < 10$$
   * A conclusão obtida $x + y < 10$ é exatamente a negação da hipótese original $\neg P$.
5. **Conclusão:**  
   Como $\neg Q \implies \neg P$ é verdadeira, segue que $P \implies Q$ é verdadeira. $\blacksquare$

---

## 📌 Bloco VI: Prova por Contradição (*Reductio ad Absurdum*)

---

### Questão 16: Não Existência do Maior Inteiro

> **Enunciado:** Prove por contradição que não existe um "maior número inteiro".

#### Demonstração Formal:
1. **Hipótese de Absurdo:**  
   Suponha, por absurdo, que existe um maior número inteiro. Chame esse número de $M \in \mathbb{Z}$.  
   Por ser o maior inteiro, ele satisfaz:
   $$\forall n \in \mathbb{Z}, \; M \ge n$$
2. **Construção do Contraexemplo:**  
   Considere o número $M' = M + 1$.
   * Como $M \in \mathbb{Z}$ e $1 \in \mathbb{Z}$, a soma $M + 1 \in \mathbb{Z}$. Logo, $M'$ é um número inteiro.
   * Por outro lado, como $1 > 0$, somando $M$ aos dois lados temos:
     $$M + 1 > M \iff M' > M$$
3. **A Contradição:**  
   Encontramos um inteiro $M' \in \mathbb{Z}$ tal que $M' > M$, o que contradiz a premissa de que $M \ge n$ para todo $n \in \mathbb{Z}$.
4. **Conclusão:**  
   A suposição inicial é falsa. Portanto, não existe um maior número inteiro. $\blacksquare$

---

### Questão 17: Soma de Racional com Irracional

> **Enunciado:** Prove por contradição que a soma de um número racional com um número irracional é sempre irracional.

#### Demonstração Formal:
1. **Definições e Hipótese:**  
   Sejam $r \in \mathbb{Q}$ e $x \notin \mathbb{Q}$.  
   Seja $s = r + x$ a soma dos dois números.
2. **Hipótese de Absurdo:**  
   Suponha, por absurdo, que $s$ é racional ($s \in \mathbb{Q}$).
3. **Isolando o elemento crítico:**  
   Podemos isolar $x$:
   $$x = s - r$$
4. **Derivação da Contradição:**  
   * Como $s \in \mathbb{Q}$ e $r \in \mathbb{Q}$, existem inteiros $a, b, c, d$ ($b, d \neq 0$) tais que $s = \frac{a}{b}$ e $r = \frac{c}{d}$.
   * Então $x = \frac{a}{b} - \frac{c}{d} = \frac{ad - bc}{bd}$.
   * Como o numerador e o denominador são inteiros (com $bd \neq 0$), decorre que $x \in \mathbb{Q}$.
   * Isso é uma contradição explícita com a premissa de que $x$ é irracional ($x \notin \mathbb{Q}$).
5. **Conclusão:**  
   A suposição de que $s$ é racional gerou um absurdo. Logo, $s = r + x$ é irracional. $\blacksquare$

---

### Questão 18: Irracionalidade de $\sqrt{2}$

> **Enunciado:** Prove por contradição que $\sqrt{2}$ é irracional.

#### Demonstração Formal:
1. **Hipótese de Absurdo:**  
   Suponha, por absurdo, que $\sqrt{2}$ é racional.  
   Então podemos escrevê-lo como uma fração irredutível:
   $$\sqrt{2} = \frac{a}{b}$$
   onde $a, b \in \mathbb{Z}$, $b \neq 0$, e $\operatorname{mdc}(a, b) = 1$ (isto é, $a$ e $b$ não possuem fatores primos em comum).
2. **Elevando ao Quadrado:**
   $$2 = \frac{a^2}{b^2} \implies a^2 = 2b^2$$
3. **Análise de Paridade de $a$:**  
   Como $a^2 = 2(b^2)$, $a^2$ é divisível por 2 (é par).  
   Pelo teorema provado na Questão 13, se $a^2$ é par, então **$a$ é par**.  
   Portanto, podemos escrever $a = 2k$ para algum $k \in \mathbb{Z}$.
4. **Análise de Paridade de $b$:**  
   Substituímos $a = 2k$ de volta na equação $a^2 = 2b^2$:
   $$(2k)^2 = 2b^2 \implies 4k^2 = 2b^2 \implies 2k^2 = b^2 \iff b^2 = 2k^2$$
   Isso mostra que $b^2$ também é par.  
   Novamente, pela Questão 13, se $b^2$ é par, então **$b$ é par**.
5. **A Contradição:**  
   Provamos que $a$ é par e $b$ é par. Logo, ambos são divisíveis por 2.  
   Mas isso contradiz a premissa de que a fração era irredutível ($\operatorname{mdc}(a, b) = 1$).
6. **Conclusão:**  
   A suposição de que $\sqrt{2} \in \mathbb{Q}$ é falsa. Logo, $\sqrt{2}$ é irracional. $\blacksquare$

---

## 📌 Bloco VII: Princípio da Indução Matemática (PIM)

---

### Questão 19: Soma dos Primeiros $n$ Números Naturais

> **Enunciado:** Prove por indução matemática que para todo $n \ge 1$:
> $$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

#### Demonstração Formal:
* **Passo 1: Caso Base ($n = 1$)**
  * Lado Esquerdo (LHS): $\sum_{i=1}^{1} i = 1$.
  * Lado Direito (RHS): $\frac{1(1+1)}{2} = \frac{2}{2} = 1$.
  * Como LHS = RHS = 1, o caso base é **verdadeiro**.

* **Passo 2: Hipótese Indutiva (HI)**
  Assumimos que a fórmula é verdadeira para um $k \ge 1$:
  $$\sum_{i=1}^{k} i = \frac{k(k+1)}{2} \quad \text{(Hipótese Indutiva)}$$

* **Passo 3: Passo Indutivo**
  Queremos provar que a fórmula vale para $k+1$, ou seja:
  $$\sum_{i=1}^{k+1} i = \frac{(k+1)((k+1) + 1)}{2} = \frac{(k+1)(k+2)}{2}$$

  Separando o último termo da soma:
  $$\sum_{i=1}^{k+1} i = \left(\sum_{i=1}^{k} i\right) + (k+1)$$
  Substituindo a Hipótese Indutiva:
  $$\sum_{i=1}^{k+1} i = \frac{k(k+1)}{2} + (k+1)$$
  Colocando $(k+1)$ em evidência:
  $$\sum_{i=1}^{k+1} i = (k+1) \left(\frac{k}{2} + 1\right) = (k+1) \left(\frac{k+2}{2}\right) = \frac{(k+1)(k+2)}{2}$$
  A expressão obtida é idêntica à esperada para $k+1$.

* **Conclusão:**  
  Pelo Princípio da Indução Matemática, a fórmula vale para todo $n \ge 1$. $\blacksquare$

---

### Questão 20: Soma dos Primeiros $n$ Ímpares

> **Enunciado:** Prove por indução matemática que para todo $n \ge 1$:
> $$\sum_{i=1}^{n} (2i - 1) = n^2$$

#### Demonstração Formal:
* **Passo 1: Caso Base ($n = 1$)**
  * LHS: $2(1) - 1 = 1$.
  * RHS: $1^2 = 1$.
  * LHS = RHS, caso base **verdadeiro**.

* **Passo 2: Hipótese Indutiva (HI)**
  Assuma que para um $k \ge 1$:
  $$\sum_{i=1}^{k} (2i - 1) = k^2$$

* **Passo 3: Passo Indutivo**
  Queremos provar que para $k+1$:
  $$\sum_{i=1}^{k+1} (2i - 1) = (k+1)^2$$

  Separando a somatória:
  $$\sum_{i=1}^{k+1} (2i - 1) = \left(\sum_{i=1}^{k} (2i - 1)\right) + (2(k+1) - 1)$$
  Aplicando a Hipótese Indutiva no primeiro bloco:
  $$\sum_{i=1}^{k+1} (2i - 1) = k^2 + (2k + 2 - 1) = k^2 + 2k + 1$$
  Fatorando o trinômio quadrado perfeito:
  $$k^2 + 2k + 1 = (k+1)^2$$
  O resultado é exatamente o esperado para $k+1$.

* **Conclusão:**  
  Pelo PIM, a igualdade é válida para todo $n \ge 1$. $\blacksquare$

---

### Questão 21: Soma de Potências de Base 2

> **Enunciado:** Prove por indução que $\sum_{i=1}^{n} 2^{i-1} = 2^n - 1$ para todo $n \ge 1$.

#### Demonstração Formal:
* **Passo 1: Caso Base ($n = 1$)**
  * LHS: $2^{1-1} = 2^0 = 1$.
  * RHS: $2^1 - 1 = 1$.
  * Caso base **verdadeiro**.

* **Passo 2: Hipótese Indutiva (HI)**
  Assumimos que para $k \ge 1$:
  $$\sum_{i=1}^{k} 2^{i-1} = 2^k - 1$$

* **Passo 3: Passo Indutivo**
  Queremos provar para $k+1$:
  $$\sum_{i=1}^{k+1} 2^{i-1} = 2^{k+1} - 1$$

  Separando o último termo:
  $$\sum_{i=1}^{k+1} 2^{i-1} = \left(\sum_{i=1}^{k} 2^{i-1}\right) + 2^{(k+1)-1} = \left(\sum_{i=1}^{k} 2^{i-1}\right) + 2^k$$
  Pela Hipótese Indutiva:
  $$\sum_{i=1}^{k+1} 2^{i-1} = (2^k - 1) + 2^k = 2 \cdot 2^k - 1 = 2^{k+1} - 1$$
  Chegamos exatamente à expressão para $k+1$.

* **Conclusão:**  
  Pelo PIM, a fórmula vale para todo $n \ge 1$. $\blacksquare$

---

### Questão 22: Desigualdade $2^n > n$

> **Enunciado:** Prove por indução matemática que para todo $n \ge 1$:
> $$2^n > n$$

#### Demonstração Formal:
* **Passo 1: Caso Base ($n = 1$)**
  * LHS: $2^1 = 2$.
  * RHS: $1$.
  * Como $2 > 1$, o caso base é **verdadeiro**.

* **Passo 2: Hipótese Indutiva (HI)**
  Assuma que para um $k \ge 1$:
  $$2^k > k \quad \text{(Hipótese Indutiva)}$$

* **Passo 3: Passo Indutivo**
  Queremos provar que a desigualdade vale para $k+1$, ou seja:
  $$2^{k+1} > k + 1$$

  Partindo do lado esquerdo para $k+1$:
  $$2^{k+1} = 2 \cdot 2^k = 2^k + 2^k$$
  Pela Hipótese Indutiva, sabemos que $2^k > k$.  
  Além disso, como $k \ge 1$, sabemos que $2^k \ge 2^1 = 2 > 1$.  
  Portanto, substituindo essas duas desigualdades:
  $$2^{k+1} = 2^k + 2^k > k + 1$$
  Concluímos que $2^{k+1} > k+1$.

* **Conclusão:**  
  Pelo Princípio da Indução Matemática, $2^n > n$ para todo número natural $n \ge 1$. $\blacksquare$
