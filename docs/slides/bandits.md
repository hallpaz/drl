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

# Multi-Armed Bandits

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 15 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)

---


# Como definir o problema de multi-armed bandits?

---

# Proxy para...

---


"... afiando o meu machado"

---


# Investigação $\times$ Exploração
## (Exploration vs Exploitation)

---

# Faz sentido só investigar?

---

# lei dos grandes números

---

# Faz sentido só explorar?

---

## "SE EU TIVESSE 8 HORAS PARA CORTAR UMA ÁRVORE, GASTARIA SEIS AFIANDO MEU MACHADO"

<br/>

-- Abraham Lincoln? Gimli, filho de Glóin? Desconhecido?

---

# Como solucionar razoavelmente o problema de multi-armed bandits?

---

# greedy vs $\epsilon$-greedy

## valor-ação

---

# greedy vs $\epsilon$-greedy

![](img/s2_greedy_epsilon_comparison.png)

----

# greedy vs $\epsilon$-greedy

![](img/s2_actions_steps.png)

---

# Algoritmo

---

# Como fazer um algoritmo greedy investigar mais?

---

# Escolhas iniciais otimistas


![](img/s2_optimistic_init.png)


---

# E se asdistribuições não forem estacionárias?

---

Cálculo do valor de uma ação

---

# Como se relaciona com aprendizado por reforço?

---

Como extender para o problema associativo?

This is an example of an associative search task, so called because it involves both
trial-and-error learning to search for the best actions, and association of these actions
with the situations in which they are best. Associative search tasks are often now called
contextual bandits in the literature. Associative search tasks are intermediate between
the k-armed bandit problem and the full reinforcement learning problem. They are like
the full reinforcement learning problem in that they involve learning a policy, but they
are also like our version of the k-armed bandit problem in that each action a↵ects only
the immediate reward. If actions are allowed to a↵ect the next situation as well as the
reward, then we have the full reinforcement learning problem. We present this problem
in the next chapter and consider its ramifications throughout the rest of the book.

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- Sutton, R.S. and Barto, A.G. (2018) [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html). 2nd Edition, A Bradford Book, Cambridge. **Capítulo 2**.