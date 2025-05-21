---
uni-module: "LNS"

alias:
  [
    "Hauptminorenkriterium",
    "definit",
    "positiv definit",
    "negativ definit",
    "semidefinit",
    "positiv semidefinit",
    "negativ semidefinit",
  ]
---

# Definitheit

| Matrix A ist        | für alle $x\in\mathbb{R}^n$ mit $x\neq0$ | alle $n$ [[Eigenwert\|Eigenwerte]] $\lambda_i$ sind | für alle $n$ [[Hauptunterdeterminanten]] $D_i$ gilt |
| ------------------- | ---------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| positiv semidefinit | $x^TAx\geq0$                             | reel und $\geq0$                                    |                                                     |
| positiv definit     | $x^TAx>0$                                | reel und $>0$                                       | $D_i>0$                                             |
| negativ semidefinit | $x^TAx\leq0$                             | reel und $\leq0$                                    |                                                     |
| negativ definit     | $x^TAx<0$                                | reel und $<0$                                       | $(-1)^{i+1}D_i<0$                                   |

Kriterium 3 heißt auch Hauptminorenkriterium.
