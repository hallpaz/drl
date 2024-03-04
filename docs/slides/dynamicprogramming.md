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

# Programação Dinâmica para Aprendizado por Reforço

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 5 de março de 2024

![bg](styles/bg_inteli_04.jpeg)


---

<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas

<br/>

- Ponderada sobre deep racer: a ser entregue na próxima sprint.
- Correção da ponderada de função de ativação.
- 1ª Prova.

<!-- ---

<!-- _paginate: false -->
<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style> -->

<!-- ---

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
# Os juros do conhecimento -->

---
<!-- _paginate: false -->
#### Autoestudos na AdaLove
![](img/s5_autoestudo_dp.png)

----

# Equação de Bellman

<br/>

$$v_\pi(s) = \mathbb{E}_\pi[G_t | S_t=s] = \sum\limits_{a \in A}\pi(a|s)\sum\limits_{s′\in \mathcal{S}}\sum\limits_{r \in \mathcal{R}}p(s′,r | a, s)[r + \gamma v\pi(s′)]$$

<br/> 

$$v_\pi(s)  = \sum\limits_{a \in A}\pi(a|s)\sum\limits_{s′, r}p(s′,r | a, s)[r + \gamma v\pi(s′)]$$

<br/>

* Sistema de $|S|$ equações! 😱

---

# Iterative Policy Evaluation

<br/>


$$v_{k+1}(s) = \mathbb{E}_\pi[R_{t+1} + \gamma v_k(S_{t+1}) | S_t=s] = \sum\limits_{a \in A}\pi(a|s)\sum\limits_{s′, r}p(s′,r | a, s)[r + \gamma v_{k}(s′)]$$

* expected updates

---

## Iterative Policy Evaluation

![](img/s5_policiy_evaluation_algorithm.png)

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Gridworld

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Melhorando uma política

---

# Iteração de Valor

##### Busca a política ótima por:

$$v_{*}(s) = \max\limits_a q_{\pi_*}(s, a)$$
$$v_{*}(s) = \max\limits_a\sum\limits_{s′, r}p(s′,r | a, s)[r + \gamma v_{*}(s′)]$$

<br/>

$$v_{k+1}(s) = \max\limits_a\sum\limits_{s′, r}p(s′,r | a, s)[r + \gamma v_{k}(s′)]$$

---

## Iteração de Valor

![](img/s5_value_iteration_algorithm.png)

---

# Teorema da melhoria de Política

<br/>

Sejam $\pi$ e $\pi'$ duas políticas tais que


$$v_{\pi'}(s) \geq v_{\pi}(s) \text{ para todo } s \in S - \{s_c\}$$

e

$$q_{\pi'}(s_c) \ge v_{\pi}(s_c)$$


então $\pi' \ge \pi$.

<!-- _footer: Adaptado de ([Sutton](http://www.incompleteideas.net/book/RLbook2020.pdf), 2018) -->

---

# Melhorando uma Política

<br/>

Construa $\pi'$ de modo que:

$$\pi' = \arg\max\limits_a q_{\pi}(s, a)$$

<br/>

* Pelo teorema da melhoria, $\pi'$ tem que ser pelo menos tão boa quanto $\pi$

---

# Iteração de Política

![](img/s5_policy_iteration_scheme.png)

<!-- _footer: Esquema de ([Sutton](http://www.incompleteideas.net/book/RLbook2020.pdf), 2018) -->

---

## Iteração de Política

![bg right:68% 94%](img/s5_policy_iteration_algorithm.png)



<!-- ---
<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style>

![bg](styles/bg_inteli_01.png)

# E quando não dá pra calcular o valor diretamente? -->

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

-  Bellman, Richard. “[The theory of Dynamic Programming](https://www.rand.org/content/dam/rand/pubs/papers/2008/P550.pdf)” Bulletin of the American Mathematical Society 60 (1954): 503-515.

- ▶️ Steve Brunton. Model Based Reinforcement Learning: [Policy Iteration, Value Iteration, and Dynamic Programming](https://youtu.be/sJIFUTITfBc?si=iCHZYo4KV9C007OU). 