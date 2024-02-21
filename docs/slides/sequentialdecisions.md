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

# Introdução a decisões sequenciais

### Aprendizado por reforço para aplicações em redes neurais

### Prof. Hallison Paz

##### 21 de fevereiro de 2024

![bg](styles/bg_inteli_04.jpeg)

---
<!-- _class: invert -->
<!-- _paginate: false -->
# Dúvidas e Dívidas


---

# Valor esperado

$$E[X] = \sum xp(x)$$

<br/>

$$E[X]=\int _{-\infty }^{\infty }xf(x)dx$$
---

# Variância

$$Var(X) = E[(X - \mu)^2]$$

$$Var(X) = E[X^2] - E[X]^2$$

---

# Distribuição Binomial ou de Bernouli

$$p(0) = P[X = 0] = 1 - p$$
$$p(0) = P[X = 1] = p$$

---

# Distribuição Normal

prova pagina 249
---

# Teorema do Limite Central

---

Binomial converge para normal

---

S0,A0,R1, S1,A1,R2, S2,A2,R3, . . .

---


p(s0, r|s, a) = Pr{St=s0,Rt=r | St−1=s,At−1=a},


----

X
s02S
X
r2R
p(s0, r|s, a) = 1, for all s 2 S, a 2 A(s). (


eq 3.2 sutton

----
p(s0 |s, a)
.
= Pr{St=s0 | St−1=s,At−1=a} =
X
r2R
p(s0, r|s, a).

eq 3.4 sutton

----


r(s, a)
.=
E[Rt | St−1=s,At−1=a] =
X
r2R
r
X
s02S
p(s0, r|s, a), (3.5

eq 3.5 sutton

---

# Retorno, objetivo

$$G_t = R_{t+1} + \gamma R_{t+2} + \gamma^2R_{t+3} + ... = \sum_{k=0}^\infty \gamma^kR_{t+k+1}$$


---

# Políticas e funções de valor

---

# Bibliografia complementar

- Sutton, R.S. and Barto, A.G. (2018) [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html). 2nd Edition, A Bradford Book, Cambridge. **Capítulo 3** até a seção 3.4.
