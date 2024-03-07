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

# Fundamentos de Métodos de Diferença Temporal

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 7 de março de 2024

![bg](styles/bg_inteli_04.jpeg)


---

<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas

<br/>

- Ponderada sobre deep racer: a ser entregue na próxima sprint.
- Correção da ponderada de função de ativação.
- Correção do Cartpole.

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

![](img/s5_autoestudo_mathqsarsa.png)

----

# Função de Qualidade

Função de valor estado-ação

<br/>

$$Q(s, a) = \mathbb{E}[r(s', s, a) + \gamma v(s')]$$
<br/>

$$Q(s, a) = \sum\limits_{s'}p(s' | s, a)(r(s', s, a) + \gamma v(s'))$$

<br/>


* Assume que tem um **modelo** da recompensa e da transição

---

# Função de Qualidade


<br/>

###### Calcula-se a função de valor de estado:
<br/>

$$v(s) = \max\limits_a Q(s, a)$$

###### Constrói-se uma política:
<br/>

$$\pi(s, a) = \arg\max\limits_a Q(s, a)$$


---

## \<RECAP\> Iteração de Valor

##### Busca a política ótima por:

$$v_{*}(s) = \max\limits_a q_{\pi_*}(s, a)$$
$$v_{*}(s) = \max\limits_a\sum\limits_{s′, r}p(s′,r | a, s)[r + \gamma v_{*}(s′)]$$

<br/>

$$v_{k+1}(s) = \max\limits_a\sum\limits_{s′, r}p(s′,r | a, s)[r + \gamma v_{k}(s′)]$$


---


<!-- _class: invert -->
<!-- _paginate: false -->

<style scoped>
h1 {
  /* text-align: center; */
  color: #1e1e1f
}
</style>


![bg 210%](styles/bg_inteli_01.png)

# O que fazer se não tiver um modelo?

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Aprendizado por Monte Carlo

---

# Aprendizado por Monte Carlo

$$G_t = R_{t+1} + \gamma R_{t+2} + \gamma^2R_{t+3} + ... = \sum_{k=0}^\infty \gamma^kR_{t+k+1}$$

###### Retorno de um episódio:

$$G = \sum_{k=0}^n \gamma^kR_{k+1}$$

###### Roda a política, calcula o retorno, divide pelos estados:


$v_{i+1}(s) = v_i(s) + \frac{1}{n}(G - v_{i}(s))$ , para todos os estados no episódio.

---

# Aprendizado por Monte Carlo

<br/>

$$v_{i+1}(s) = v_i(s) + \frac{1}{n}(G - v_{i}(s))$$

$$Q_{i+1}(s, a) = Q_i(s, a) + \frac{1}{n}(G - Q_{i}(s, a))$$

<br/>

* Diferença é uma "medida de erro"
* Aprendizado por experiência; sem modelo prévio.

---
<!-- _class: invert -->
#### Legal, mas....


# Monte Carlo Learning é ineficiente.

## POR QUÊ?

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Aprendizado por Diferença Temporal

<!-- maybe events that happened more recently are somehow related to the rewards im getting -->

---

# Diferença Temporal (TD)

<br/>

$$v(s_k) = \mathbb{E}[R_{k+1} + \gamma v(s_{k+1})]$$



###### Expressão para TD(0):

<br/>

$$v^{\text{novo}}(s_k) = v^{\text{velho}}(s_k) + \alpha[R_{k+1} + \gamma v^{\text{velho}}(s_{k+1}) - v^{\text{velho}}(s_k)]$$

###### Expressão para TD(1): **???????**

* No limite, converge para o aprendizado por Monte Carlo.

<!-- ---

TD-$\lambda$ -->

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# SARSA: State-Action-Reward-State-Action

---

# SARSA: State-Action-Reward-State-Action

<br/>

$$Q^{\text{novo}}(s_k, a_k) =  Q^{\text{velho}}(s_k, a_k) + \alpha[R_{k+1} + \gamma Q(s_{k+1}, a_{k+1}) - Q^{\text{velho}}(s_k, a_k)]$$

<br/>


* SARSA - on-policy
* funciona com TD(n)


<!-- SARSA - on-policy - always doing what you think is the best think (more exploitation)

- more cumulative reward during learning process

you need to take trajections on the environment - aprender com experiência -->

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Q-Learning

---

# Q-learning - off-policy

<br/>

$$Q^{\text{novo}}(s_k, a_k) =  Q^{\text{velho}}(s_k, a_k) + \alpha[R_{k+1} + \gamma\max\limits_a Q(s_{k+1}, a) - Q^{\text{velho}}(s_k, a_k)]$$

<!-- Q-learning pode aprender por imitação pq é off-policy

experience replay

can explore more 

epsilon-greedy - off-policy search strategies
-->

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar


- ▶️ Ajay Halthor. [Foundation of Q-learning | Temporal Difference Learning explained!](https://youtu.be/uJX_72MnKg8?si=0y6R5tmPP0G-TUJD)


- ▶️ Steve Brunton. Q-Learning: [Model Free Reinforcement Learning and Temporal Difference Learning](https://youtu.be/0iqz4tcKN58?si=curA0y49JN_Hlcn-).