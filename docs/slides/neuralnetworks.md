---
marp: true
paginate: true
# space mono para titulos
# manrope para corpo 
# 20240208
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

# Matemática para redes neurais (feedforward)

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 8 de fevereiro de 2024

![bg ](#2D253F)

---

![bg left](img/s1_hallison.jpg)

# Sobre mim
### Hallison Paz

- Engenheiro de computação (Instituto Militar de Engenharia)
- Mestre e doutorando em Matemática (IMPA)
- Criador do canal (Youtube)
Programação Dinâmica 
- Trabalhei no Reality Labs Research (Meta)

---
<!-- _class: invert -->
<!-- _paginate: false -->

# "SOMOS A FACULDADE QUE FORMA OS LÍDERES DO FUTURO."

![bg black opacity:.2 saturate](img/s1_inteli.jpg)

<!-- _footer: Fonte: https://www.inteli.edu.br/quem-somos/ -->

---

# Mapeamento de competências da Turma

- Inglês
- Python
- Matemática

#### https://forms.gle/xzbykAzUzAJvxBZX7

![bg right:40% 80%](img/s1_poll_qrcode.jpg)

---


# Por que estudar o que a gente vai estudar?

![bg](styles/bg_inteli_01.png)

<!-- _class: invert -->
---

<!-- _class: invert -->
<!-- _backgroundColor: #2D253F -->
<!-- _paginate: false -->

# O que é uma rede neural?

---

![bg](img/s1_network_cloud.png)

---

# Como isso nos ajuda a resolver problemas?

---

# Forward Propagation

![bg right:56% fit](img/s1_perceptron.png)

---

<!-- combinação, produto escalar, matrizes, linear, não-linear, entrada, saída -->
![bg fit](img/s1_cloud_perceptron.png)

---

<!-- _footer: REPRESENTAÇÃO MATRICIAL. <br/> Imagem: https://www.jeremyjordan.me/intro-to-neural-networks/-->

![bg 80%](img/s1_neural_matrix.png)

---

<!-- _class: invert -->
<!-- _backgroundColor: "#2D253F" -->
<!-- _paginate: false -->

# Função de ativação
## Por quê?

---

# Função de ativação
#### Exemplos
![](img/s1_activation_functions.jpg)

<!-- _footer: Figure on ResearchGate. Available from: https://www.researchgate.net/figure/Fig-3-The-basic-activation-functions-of-the-neural-networksNeural-Networks_fig3_350567223 [accessed 7 Feb, 2024] -->
---

# O que não pode ser uma função de ativação?

---

<!-- _class: invert -->
<!-- _backgroundColor: "#2D253F" -->
<!-- _paginate: false -->

# Perceptron Multicamada
## (Multilayer Perceptron)

---

# Perceptron Multicamadas
## Multilayer Perceptron (MLP)

![bg left:56% fit](img/s1_mlp.png)

<!-- _footer: John Salatas, CC BY-SA 3.0 <https://creativecommons.org/licenses/by-sa/3.0>, <br/> via Wikimedia Commons -->

<!-- _paginate: false -->

---

![bg](img/s1_cloud_mlp.png)

<!-- composição de funções, multiplicação de matrizes, transformações lineares -->

---

# Questão Ponderada - parte 1

Você foi contratado por uma startup de tecnologia de saúde que está desenvolvendo um algoritmo de aprendizado profundo para detectar anomalias em imagens de raios-X. Durante a fase de prototipagem, a equipe decidiu usar a função de ativação ReLU nas camadas ocultas de sua rede neural.

Após algumas iterações, você observa que muitos neurônios na rede estão "morrendo" durante o treinamento, ou seja, eles estão sempre produzindo uma saída zero, independentemente da entrada.

----

# Questão Ponderada - parte 2

a) Explique por que a função ReLU pode causar o "morte" de neurônios durante o treinamento.
b) Sugira uma modificação ou alternativa à função ReLU para mitigar esse problema.
c) Descreva como essa modificação ou alternativa pode beneficiar o treinamento do modelo, especialmente em um contexto de detecção de anomalias em imagens médicas.

---

<!-- _class: invert -->
<!-- _backgroundColor: #2d253f-->
<!-- _paginate: false -->

# Bibliografia complementar

- Goodfellow, Ian, Yoshua Bengio, and Aaron Courville. [Deep Learning](https://www.deeplearningbook.org/). Cambridge, MA: MIT Press, 2016. Chicago (author-date), 17th ed.
    - [Capítulo 6](https://www.deeplearningbook.org/contents/mlp.html).



