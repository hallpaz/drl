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

# Visão Geral de Deep Reinforcement Learning

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 14 de março de 2024

![bg](styles/bg_inteli_04.jpeg)


---

<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas

<br/>

- Ponderadas: até domingo (17/03/2024)!
- Correção das provas: até segunda-feira (18/03/2024)
- Ponderada de Deep Racer: ?????



---

# Recapitulando

## Q-learning

<br/>

$$Q^{\text{novo}}(s_k, a_k) =  Q^{\text{velho}}(s_k, a_k) + \alpha[R_{k+1} + \gamma\max\limits_a Q(s_{k+1}, a) - Q^{\text{velho}}(s_k, a_k)]$$

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Deep Q-Network (DQN)

---

![bg fit 72%](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/04/Screenshot-2019-04-16-at-5.46.01-PM.png)

<!-- _footer: https://colab.research.google.com/drive/1KCvsI2ATucEuQadbUxsJf67s2e-wQ3Fd?usp=sharing -->

---
<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Policy Gradients

---

# Policy Network

<br/>

![h:380](https://karpathy.github.io/assets/rl/policy.png)

<!-- _footer: https://karpathy.github.io/2016/05/31/rl/ -->

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- S. L. Brunton (2022, January 21), Overview of Deep Reinforcement Learning Methods. Disponível em: https://doi.org/10.52843/cassyni.kfnzpy. Acesso em 14 de março de 2024.

- Andrej Karpathy. [Deep Reinforcement Learning: Pong from Pixels](https://karpathy.github.io/2016/05/31/rl/). Andrej Karpathy blog, 2016.

- Sanyam Kapoor. [Police Gradients in a Nutshell](https://towardsdatascience.com/policy-gradients-in-a-nutshell-8b72f9743c5d). Towards Data Science, 2018.