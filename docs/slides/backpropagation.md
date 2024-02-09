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

# Matemática para redes neurais (backpropagation)

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 9 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)

---

<!-- ## Redes Neurais são aproximadores universais -->

![bg fit](img/s1_hornik_paper.png)

<!-- https://doi.org/10.1016/0893-6080(89)90020-8 -->

---

# Como você faria para um perceptron aproximar uma reta específica?

---
## Como se computa a saída de um MLP? 

![bg right:60% 80%](img/s1_mlp.png)

---

# Composição de funções

<!-- _class: invert -->
<!-- _backgroundColor: #2D253F -->
<!-- _paginate: false -->

---

# Sabemos calcular a saída (resposta) de uma rede. E agora?

---

<!-- _class: invert -->
<!-- _backgroundColor: #2D253F -->

# Função de custo ou função de perda

---

# Métricas

##### Uma métrica ou função de distância é qualquer função que atende às 3 propriedades a seguir:

- Não negativa
- Simétrica
- Respeita desigualdade triangular


---

# Regra da Cadeia

Se $h(x) = f(g(x))$, então:

<br/>

$$\frac{dh}{dx} = \frac{df}{dg} \cdot \frac{dg}{dx}$$

<!-- ![bg](styles/bg_inteli_03.png) -->

---

Método de Newton

---

# Funções de várias variáveis
<br/>

#### Exemplo 1:

$$f: \mathbb{R}^2 \rightarrow \mathbb{R}, f(x, y) = x^2 + xy - cos(y)$$

<br/>

#### Exemplo 2:

$$g: [0, \pi] \times [0, 2\pi] \rightarrow \mathbb{R}^3, g(x) = (sen(x)cos(y), sen(x)sen(y), cos(x)) $$

---

<!-- _class: invert -->
<!-- _backgroundColor: #2D253F -->

<!-- _paginate: false -->

# $\partial$ Derivadas Parciais

---

<!-- _class: invert -->
<!-- _backgroundColor: #2D253F -->
<!-- _paginate: false -->

# $\nabla$ Gradiente 



---

# Gradiente Descendente

<br/><br/>

$$\theta_{j+1} = \theta_j - \gamma \nabla C(\theta_j)$$

![bg right:40% fit](img/s1_gradient_descent.gif)

<!-- _footer: Para experimentar: https://www.geogebra.org/m/sWsGNs86 -->

---
# Backpropagation

![bg left:54% fit](img/s1_backprop_paper.png)

---

# Deu pra entender que a **função de ativação** tem um papel nesse processo?

---



