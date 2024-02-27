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

# Funções de Valor e a Equação de Bellman

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 27 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)


---

<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas

<!-- ---

<!-- _paginate: false -->
<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style> -->

---

<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}

h3 {
  /* text-align: center; */
  color: #dddddd
}
</style>

![bg](styles/bg_inteli_01.png)

### Reflexão
# Os juros do conhecimento

---
<!-- _paginate: false -->
#### Autoestudos na AdaLove
![](img/s4_bellman_autoestudo.png)

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Funções de Valor

---

# Retorno, objetivo

$$G_t = R_{t+1} + \gamma R_{t+2} + \gamma^2R_{t+3} + ... = \sum_{k=0}^\infty \gamma^kR_{t+k+1}$$

---

# Estado Final

<br/>

![](img/s4_absorbing_state.png)

---

## Política como distribuição de probabilidade

<br/>

Uma política é um mapeamento (função) que diz qual a probabilidade de escolher a ação $A_t=a$ no estado $S_t=s$.

<br/>

$$\pi(a | s) = P[A_t=a | S_t=s]$$

---

# Exercício: especificação de uma política

![bg left:60%](img/s4_autoestudo_grid.png)

---
## Função de valor de um estado $s$ sob a política $\pi$

<br/>

$v_\pi(s) = \mathbb{E}_\pi[G_t | S_t = s] = \mathbb{E}_\pi[\sum\limits_{k=0}^\infty \gamma^kR_{t+k+1} | S_t = s]$, para todo $s \in S$

---

## Função de valor de uma ação sob a política $\pi$

<br/>

$q_\pi(s, a) = \mathbb{E}_\pi[G_t | S_t=s, A_t = a] = \mathbb{E}_\pi[\sum\limits_{k=0}^\infty \gamma^kR_{t+k+1} | S_t=s, A_t=a]$

---

## Derivando a equação de Bellman



<!-- _footer: Fonte: https://stats.stackexchange.com/questions/243384/deriving-bellmans-equation-in-reinforcement-learning -->

---

## A equação de Bellman

<br/>

$v_\pi(s) = \mathbb{E}_\pi[G_t | S_t=s] = \sum\limits_{a \in A}\pi(a|s)\sum\limits_{s′\in \mathcal{S}}\sum\limits_{r \in \mathcal{R}}p(s′,r | a, s)[r + \gamma v\pi(s′)]$

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
## Entendendo a ~~cabulosa💀~~ equação de Bellman


---
# "Backup Diagram"

#### Foco no estado

<br/>

* $v_\pi(s) = \sum\limits_{a \in \mathcal{A}}\pi(a | s)q_\pi(s, a)$

![bg right 90% fit](img/s4_backup_state.jpg)

---

# "Backup Diagram"

#### Foco na ação

![h:300](img/s4_backup_action.jpg)

* $q_\pi(s, a) = r(s, a, s') + \sum\limits_{s' \in \mathcal{S}}p(s' | s, a) v_\pi(s')$

---

# Tudo junto...

![h:360](img/s4_backup_full.jpg)

$$v_\pi(s) = \sum\limits_{a \in \mathcal{A}}\pi(a | s)(r(s, a, s') + \gamma\sum\limits_{s' \in \mathcal{S}}p(s' | a, s)v_\pi(s'))$$

---

## Exercício: Qual o valor de cada estado colorido?

- Considere: $\gamma=0.9$; $r_A=10$; $r_B=5$; $r_{fora}=-1$; $r_{outros}=0$.
- $\pi(a | s) = \frac{1}{4}, \forall a \in \mathcal{A}$

![](img/s4_gridworld_exercise.png)

---
# Resposta
<!-- ![bg fit](img/s4_gridworld_equip.png) -->

<!-- _foote: EXEMPLO: Sutton, 2018 -->


---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Políticas ótimas

---

# Políticas ótimas

<br/>

- $\pi \gt \pi' \leftrightarrow v_\pi(s) \ge v_{\pi'}(s)$  para todo $s \in \mathcal{S}$

- A cada política ótima há uma função de valor de estado $v_*(s)$ e uma função de valor de ação ótimos $q_*(s, a)$.

---

![](img/s4_optimal_statevalue.png)

Se a recompensa for determinística, tem-se:
$$v_*(s) = \max\limits_a r(s, a, s') + \gamma\sum\limits_{s' \in \mathcal{S}}p(s' | a, s)v_*(s')$$


<!-- _footer: Sutton, 2018 -->

---

![](img/s4_optimal_actionvalue.png)

No caso de recompensa determinística:
$$q_*(s, a) = r(s, a, s') + \gamma\sum\limits_{s' \in \mathcal{S}}p(s' | a, s)\max\limits_aq_*(s', a')$$

<!-- _footer: Sutton, 2018 -->

---

![bg fit](img/s4_gridworld_optimal.png)

<!-- _footer: Sutton, 2018 -->

---

## Exercício: calcule o valor ótimo no grid do autoestudo

![bg right:60% 90%](img/s4_autoestudo_grid.png)

<!-- _paginate: false -->
---
<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style>

![bg](styles/bg_inteli_01.png)

# E quando não dá pra calcular o valor diretamente?

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- Sutton, R.S. and Barto, A.G. (2018) [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html). 2nd Edition, A Bradford Book, Cambridge. **Capítulo 3** seções 3.4 a 3.6.

- Aleksandar Haber. [Clear Explanation of the Value Function and Its Bellman Equation](https://aleksandarhaber.com/deconstructing-the-meaning-of-the-value-function-and-its-bellman-equation-reinforcement-learning-tutorial/) – Reinforcement Learning Tutorial.

- Luc Gendrot. Not Another RL Tutorial! [Part 2: Chains, Rewards, and Decision Processes, Oh My!](https://medium.com/@lgendrot/teaching-myself-rl-eef155ef5e4a)