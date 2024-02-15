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

<!-- _class: invert -->
<!-- _paginate: false -->
# Choros e lamentações

![bg opacity:.2](https://upload.wikimedia.org/wikipedia/commons/8/86/Edvard_Munch_-_The_Scream_-_Google_Art_Project.jpg)

---

<!-- _class: invert -->
<!-- _paginate: false -->

<style scoped>
h1 {
  /* text-align: center; */
  color: #1e1e1f
}
</style>

# Como definir o problema de multi-armed bandits?

![bg 210%](styles/bg_inteli_01.png)


---

# Que tipos de problemas seguem esta modelagem?


---

<!-- _class: invert -->
<!-- _backgroundColor: #2D253F -->

<!-- _paginate: false -->

# Investigação $\times$ Exploração

## (Exploration vs Exploitation)

---

# Faz sentido só investigar?

---

# Lei dos grandes números

---

# Faz sentido só explorar?

---

<!-- _class: invert -->

## "SE EU TIVESSE 8 HORAS PARA CORTAR UMA ÁRVORE, GASTARIA SEIS AFIANDO MEU MACHADO"

<br/>

-- Abraham Lincoln? Gimli, filho de Glóin? Desconhecido?

---

<style scoped>
h1 {
  /* text-align: center; */
  color: #1e1e1f
}
</style>


# Como solucionar razoavelmente o problema de multi-armed bandits?

![bg 210%](styles/bg_inteli_01.png)

---

# Greedy vs $\epsilon$-greedy

## valor-ação

---

# Exemplo: 
# 10-armed bandits

![bg right:69% 95%](img/s2_reward_distribution.png)

---

# Greedy vs $\epsilon$-greedy

![](img/s2_greedy_epsilon_comparison.png)

<!-- _footer: Sutton, R.S. and Barto, A.G. (2018) Reinforcement Learning: An Introduction. 2nd Edition, A Bradford Book, Cambridge. Capítulo 2  -->

----

# Greedy vs $\epsilon$-greedy

![](img/s2_actions_steps.png)

<!-- _footer: Sutton, R.S. and Barto, A.G. (2018) Reinforcement Learning: An Introduction. 2nd Edition, A Bradford Book, Cambridge. Capítulo 2  -->

---

# Algoritmo

![](img/s2_bandit_algorithm.png)

<!-- _footer: Sutton, R.S. and Barto, A.G. (2018) Reinforcement Learning: An Introduction. 2nd Edition, A Bradford Book, Cambridge. Capítulo 2  -->

---

<style scoped>
h1 {
  /* text-align: center; */
  color: #1e1e1f
}
</style>

![bg 210%](styles/bg_inteli_01.png)

# Como fazer um algoritmo greedy investigar mais?

---

# Escolhas iniciais otimistas


![](img/s2_optimistic_init.png)


---

# E se as distribuições não forem estacionárias?

---

# Cálculo do valor de uma ação

---

# Como se relaciona com aprendizado por reforço?

---

# Contextual Armed Bandits
## <<< Próxima semana >>>

---

<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style>

# TROCA DE CONTEXTO

![bg ](styles/bg_inteli_01.png)


---

# Problema do Cartpole

<video width="480" height="320" controls>
  <source src="video/cartpole.mp4" type="video/mp4">
</video>

<!-- _footer: Cartpole no [OpenAI Gym](https://www.gymlibrary.dev/environments/classic_control/cart_pole/) -->


---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- Sutton, R.S. and Barto, A.G. (2018) [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html). 2nd Edition, A Bradford Book, Cambridge. **Capítulo 2**.

##### Para ir mais além

- A. G. Barto, R. S. Sutton and C. W. Anderson, ["Neuronlike adaptive elements that can solve difficult learning control problems,"](http://incompleteideas.net/papers/barto-sutton-anderson-83.pdf) in IEEE Transactions on Systems, Man, and Cybernetics, vol. SMC-13, no. 5, pp. 834-846, Sept.-Oct. 1983, doi: 10.1109/TSMC.1983.6313077.