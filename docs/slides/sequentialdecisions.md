---
marp: true
paginate: true
# space mono para titulos
# manrope para corpo 
---

<style>
    section {
        font-family: "Manrope", Arial;
    }
    h1, h2 {
        font-family: "Space Mono", monospace;
    }
</style>


<!-- _class: invert -->
<!-- _paginate: false -->

# Introdução a decisões sequenciais

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 21 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)


---

<!-- _paginate: false -->
<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style>

# O que esperar da aula de hoje?

![bg](styles/bg_inteli_01.png)

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Revisão de Probabilidade

---

# Revisão de Probabilidade

- Espaço Amostral
- Evento
- Probabilidade
- Variável aleatória

---

# Probabilidade Condicional

$P(B\mid A)={\frac {P(B \cap A)}{P(A)}}$

---

# Eventos Independentes

∀x ∈ x, y ∈ y, p(x = x, y = y) = p(x = x)p(y = y).


---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Variável aleatória

---

# Variável aleatória

### Valor esperado

$$E[X] = \sum\limits_x xp(x)$$

<br/>

$$E[X]=\int _{-\infty }^{\infty }xf(x)dx$$
---

# Variável aleatória

### Variância

$$Var(X) = E[(X - \mu)^2]$$

<br/>

$$Var(X) = E[X^2] - E[X]^2$$

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Exemplos de Distribuições Notáveis

---

# Distribuição Binomial ou de Bernouli

$p(1) = P[X = 1] = p$

$p(0) = P[X = 0] = 1 - p$


---

# Distribuição Normal



---

# Teorema do Limite Central

![](img/s3_limite_central.png)

<!-- _footer: ROSS, S. [Probabilidade um curso moderno com aplicações](https://integrada.minhabiblioteca.com.br/books/9788577806881). 8. ed. Porto Alegre: Bookman, 2010. Capítulo 8. -->

---

# Distribuição Conjunta e Probabilidade marginal

![h:420](img/s3_joint_prob.png)

<!-- _footer: Fonte: [MathExchange](https://math.stackexchange.com/questions/1497879/understanding-how-to-obtain-this-table-for-the-joint-probability) -->

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Problemas de Decisão Sequencial

---

![bg](img/s3_modeling_sequential_decisions.png)


----
# Notação

- Tempo $t$
- Estados $S_t \in \mathcal{S}$
- Ações $A_t \in \mathcal{A}(s)$
- Recompensas $R_{t+1} \in \mathcal{R} \subset \mathbb{R}$ 

#### Sequência ou trajetória
<br/>

$$S_0,A_0,R_1, S_1,A_1,R_2, S_2,A_2,R_3, . . .$$

---

If the random variables $R_t$ and $S_t$ have well defined discrete probability distributions dependent only on the preceding state and action, then we have a **Markov Decision Process**. *(adapted from [1])*


<!-- _footer: - [1] Sutton, 2018 -->

---

<!-- _backgroundColor: #F2F2F2 -->
<!-- _paginate: false -->

![bg 80%](img/s3_robot_state.png)

---

# Dinâmica de um processo de decisão de Markov

<br/>

$p(s', r|s, a) = Pr\{S_t=s',R_t=r | S_{t−1}=s,A_{t−1}=a\}$

<br/>

$\sum_\limits{s' \in \mathcal{S}}\sum\limits_{r \in \mathcal{R}}p(s', r|s, a)$ para todo $s \in \mathcal{S}, a \in \mathcal{A}(s)$


---

![bg 85%](img/s3_probabilities_mdp.png)

<!-- _footer: Sutton, 2018 -->

---

# Retorno, objetivo

$$G_t = R_{t+1} + \gamma R_{t+2} + \gamma^2R_{t+3} + ... = \sum_{k=0}^\infty \gamma^kR_{t+k+1}$$


---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Políticas e funções de valor

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Bibliografia complementar


- Goodfellow, Ian, Yoshua Bengio, and Aaron Courville. [Deep Learning](https://www.deeplearningbook.org/). Cambridge, MA: MIT Press, 2016. Chicago (author-date), 17th ed.
    - [Capítulo 3](https://www.deeplearningbook.org/contents/prob.html) até a seção 3.9.3.

- Sutton, R.S. and Barto, A.G. (2018) [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html). 2nd Edition, A Bradford Book, Cambridge. **Capítulo 3** até a seção 3.4.

- 
