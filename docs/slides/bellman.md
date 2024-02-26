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
## Função de valor de um estado $s$ sob a política $\pi$

<br/>

$v_\pi(s) = \mathbb{E}_\pi[G_t | S_t = s] = \mathbb{E}_\pi[\sum\limits_{k=0}^\infty \gamma^kR_{t+k+1} | S_t = s]$, para todo $s \in S$

---

## Função de ação-valor sob a política $\pi$

<br/>

$q_\pi(s, a) = \mathbb{E}_\pi[G_t | S_t=s, A_t = a] = \mathbb{E}_\pi[\sum\limits_{k=0}^\infty \gamma^kR_{t+k+1} | S_t=s, A_t=a]$

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->
# Políticas e funções de valor

---

E quando a gente não sabe calcular?

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- Sutton, R.S. and Barto, A.G. (2018) [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html). 2nd Edition, A Bradford Book, Cambridge. **Capítulo 3** seções 3.4 a 3.6.

- dsd https://aleksandarhaber.com/deconstructing-the-meaning-of-the-value-function-and-its-bellman-equation-reinforcement-learning-tutorial/ 
