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

# Introdução aos Métodos de Monte Carlo

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 29 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)


---

<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas

- Ponderada sobre equação de Bellman: 03/03/2024
- Ponderada sobre deep racer: a definir
- Correção da ponderada de Backpropagation 

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
![](img/s4_autoestudo_montecarlo.png)

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Métodos de Monte Carlo


---

# Métodos de Monte Carlo

- Qual a ideia por trás desta estratégia?
- Por que ela funciona?
- Como ela irá nos ajudar?

![bg right:38%](img/s4_montecarlo_ville.jpg)
<!-- Repeated Random Sampling

estimate values directly from experience

estimate value function without prior knowledge of environment dynamics -->

---

<!-- _class: invert -->
<!-- _paginate: false -->

<style scoped>
h1 {
  /* text-align: center; */
  color: #1e1e1f
}

footer {
    color: #ffffff
}

a {
    color: #1d1d1d
}

</style>

![bg 210%](styles/bg_inteli_01.png)
# Prática no Google Colab

<a href="https://colab.research.google.com/github/hallpaz/drl/blob/main/notebooks/intro_montecarlo.ipynb\" target="_parent\"><img src="https://colab.research.google.com/assets/colab-badge.svg\" alt="Open In Colab"/></a>

<!-- _footer: Link por extenso: https://colab.research.google.com/github/hallpaz/drl/blob/main/notebooks/intro_montecarlo.ipynb -->

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- Timothy Budd. NWI-NM042B Monte Carlo Techniques. Physics & Astronomy master program at Radboud University, Nijmegen, The Netherlands. Chapter 3: [Direct-sampling Monte Carlo integration](https://hef.ru.nl/~tbudd/mct/lectures/monte_carlo_integration.html)

- [Monte Carlo Methods in Practice](https://www.scratchapixel.com/lessons/mathematics-physics-for-computer-graphics/monte-carlo-methods-in-practice/monte-carlo-methods.html). Scratch that Pixel.