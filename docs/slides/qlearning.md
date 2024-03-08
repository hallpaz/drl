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

# Q-Learning e Aprendizagem por Diferença Temporal

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 8 de março de 2024

![bg](styles/bg_inteli_04.jpeg)

---

<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas

<br/>

- Ponderada sobre deep racer: olhar mensagem do prof Raphael no Slack.
- Prazo da ponderada Gridworld: 11/03/2024?? 

---

### Ponderada Eq de Bellman

![h:550](img/s5_bellman_exercise.png)

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

# Artefatos desta Sprint

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


- Algoritmo *on-policy*
- Funciona com TD(n)


<!-- SARSA - on-policy - always doing what you think is the best think (more exploitation)

- more cumulative reward during learning process

you need to take trajections on the environment - aprender com experiência -->

---

## SARSA

![](img/s5_sarsa_algorithm.png)

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Q-Learning

---

# Q-learning

<br/>

$$Q^{\text{novo}}(s_k, a_k) =  Q^{\text{velho}}(s_k, a_k) + \alpha[R_{k+1} + \gamma\max\limits_a Q(s_{k+1}, a) - Q^{\text{velho}}(s_k, a_k)]$$

- Algoritmo *off-policy*

---

## Q-Learning

![](img/s5_qlearning_algorithm.png)

---

# SARSA vs Q-Learning

![](img/s5_cliffwalk.png)


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

# Onde entra redes neurais nisso tudo?

---

<!-- _class: invert -->
<!-- _paginate: false -->

# Intuição do Deep Q-Learning

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar


- ▶️ Steve Brunton. Q-Learning: [Model Free Reinforcement Learning and Temporal Difference Learning](https://youtu.be/0iqz4tcKN58?si=curA0y49JN_Hlcn-).

- Volodymyr Mnih, Koray Kavukcuoglu, David Silver, Alex Graves, Ioannis Antonoglou, Daan Wierstra, Martin Riedmiller. [Playing Atari with Deep Reinforcement Learning](https://arxiv.org/abs/1312.5602). ArXiv preprint arXiv:1312.5602 (2013)
