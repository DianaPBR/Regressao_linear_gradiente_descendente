# Programming 2021
# Data Science and Business Intelligance

### Regressão Linear - Gradiente Descendente

    O trabalho terá em conta a implementação de um algoritmo usando o método de Regressão Linear, através da Gradiente   Descendente. E terá em atenção aos seguintes pontos:
    - Utilização de bibliotecas numpy;
    - Condição de paragem do algoritmo (número de passos, erro mínimo e iterações mínimas);
    - Previsão de valores de output para um conjunto de dados sem resultado;
    - Suporte gráfico ao modelo.
    
    O Projeto será carregado em github.
    
### Regressão Linear

    É uma equação para se estimar o valor de uma variável Y, tendo em conta os valores de uma/mais variável(eis) X.             Caracterizada pela função:
                                                Y = mX + b ou y = b0 + b1x
     Y - Variável Independente
     X - Vairável Dependente
     m - Declive
     b - Ordenada da origem (a interseção em y, (0,b))
 
    Para minimizar os erros, e para obter o valor mais preciso de m e b, terá de ser usado o Método dos mínimos quadrados, sendo que a Gradiente Descendente converge para o valor mínimo tendo em conta o learning_rate.
    
\\[ mx = \sum_{i=0}^n (x_i - \bar x_i)(y_i - \bar y_i) / \sum_{i=0}^n (x_i - \bar x_i)^2 \\]  

\\[ b = \bar y - m* \bar x \\]  

isto é 

1. Diferença entre o valor real de y e o valor esperado de y
    
    \\[ (yi - \bar yi) \\] 
    
2. Diferença dos quadrados 

    \\[ (yi - \bar yi)^2 \\] 

3. Média dos quadrados

    \\[ E = \frac{1}{n} \sum_{i=0}^n (y_i - \bar y_i)^2\\]
    
4. Erro médio dos quadrados

    \\[ E = \frac{1}{n} \sum_{i=0}^n (y_i - (mx_i + b))^2\\]
    
###  Gradiente Descendente

A gradiente descendente procura assim o valor mínimo da função:

- m = 0
- b = 0
- L (Learning rate) (Muito alta pode levar a passar do valor mínimo, e um learning rate demasiado baixo irá tornar o algoritmo muito lento até à convergência para o valor mínimo)

Desta forma será necessário calcular a derivada da função erro com respeito a m e a b.

- Dm
    \\[ Dm = \frac{-2}{n} \sum_{i=0}^n x_i(y_i - \bar y_i) \\]  
    
- Db
    \\[ Db= \frac{-2}{n} \sum_{i=0}^n (y_i - \bar y_i) \\]
    
Resumindo, o valor de m e b será:

\\[ m = m + (error * X) * LR\\]

\\[ b = b + (error) * LR\\]

![Gradient_descent_2.jpg.png](attachment:Gradient_descent_2.jpg.png)
hi
