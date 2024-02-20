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

# Aprendizado por Reforço no Deep Racer

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 19 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)

---

<!-- _class: invert -->
<!-- _paginate: false -->
# From bandits to "bandits cars"

![bg opacity:.3](https://live.staticflickr.com/8541/8676282757_f18db38cb9_b.jpg)

---

# Multi-Armed Bands com distribuição não-estacionária

---

# Cálculo do valor de uma ação

<br/>

$$Q_{n+1} = Q_n + \alpha[R_n - Q_n]$$

<br/>

Quando $\alpha_n(a) = \frac{1}{n}$ para todo $n$, temos o caso anterior (média simples).

<br/>

##### Qualquer sequência $\{\alpha_n(a)\}$ pode ser utilizada para solucionar o problema?

---

<!-- _backgroundColor: #2D253F -->
<!-- _class: invert -->

---

# Contextual Armed Bandits

https://hackernoon.com/contextual-multi-armed-bandit-problems-in-reinforcement-learning

---

# Como se relaciona com aprendizado por reforço?

---
<style scoped>
h1 {
  /* text-align: center; */
  color: #ffffff
}
</style>

# Deep Racer

![bg ](styles/bg_inteli_01.png)

---

<!-- _paginate: false -->
<!-- _backgroundColor: #2D253F -->
<!-- _class: invert -->


# O que é aprendizado por reforço?

---

# Agente

---

# Ambiente

---

# Ação

---

# Recompensa


---

# Estado

---


---

# Função de Valor ou Função de Recompensa

---

![](img/s3_maze.png)


---

# Função de recompensa

Position on track
Heading
Waypoints
Track width
Distance from center line
All wheels on track
Speed
Steering angle

<!-- _footer: Documentação do [Deep Racer](https://docs.aws.amazon.com/deepracer/latest/developerguide/deepracer-console-train-evaluate-models.html#deepracer-reward-function-signature) -->

---

PPO algorithm

---

# Parâmetros e Hiperparâmetros

---

# Ajuste de funções de recompensa

---

# Competição


- Competição individual por aluno. 
- Inscrições a partir de 5 de março.
- Haverá 3 workshops virtuais.
- Corrida virtual classificatória.
- 5 modelos selecionados por região geográfica
- 25 finalistas no Congresso da SBC em Brasília.