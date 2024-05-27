# O que é um Sistema de Numeração?
- Um sistema de numeração é um conjunto de símbolos e regras que permitem representar quantidades de forma consistente.
- Contar é uma atividade que faz parte do nosso dia a dia, desde a antiguidade o homem sentiu a necessidade de contar. Isso levou à criação de sistemas de numeração por diversas civilizações.
- Um mesmo número pode ser representado de diferentes formas, dependendo do sistema de numeração utilizado. Por exemplo, o número 10 pode ser representado como:
  - $10_{10}$ (decimal)
  - $A_{16}$ (hexadecimal)
  - $1010_2$ (binário)
  - $X$ (romano)
  
# O que é um Sistema de Numeração Posicional?
- Em um sistema de numeração posicional, o valor de cada símbolo depende da sua posição na representação do número.
- O sistema de numeração decimal é um exemplo de sistema de numeração posicional. No número 123, o 1 representa 100, o 2 representa 20 e o 3 representa 3.
- Números romanos, por exemplo, não são um sistema de numeração posicional.
  - Isso significa que o valor de um dígito não depende da sua posição na representação do número.
  - O número 123 em romano é CXXIII, onde C representa 100, X representa 10 e III representa 3. Observe que o X é 10 em qualquer posição.
- Um conjunto de símbolos é chamado de base.
  
# Base Decimal:
- O sistema de numeração decimal é o mais utilizado no dia a dia.
- Ele é composto por 10 símbolos: { $0, 1, 2, 3, 4, 5, 6, 7, 8, 9$ }
- Cada posição de um número decimal representa uma potência de 10.
  - Por exemplo, o número $123_{10}$ é representado por:
    - $1 * 10^2 + 2 * 10^1 + 3 * 10^0 = 100 + 20 + 3 = 123_{10}$
  - Para representar um número fracionário, como $12$,$34_{10}$, podemos utilizar potências negativas de 10.
    - $1 * 10^1 + 2 * 10^0 + 3 * 10^{-1} + 4 * 10^{-2} = 10 + 2 + 0.3 + 0.04 =$$12$,$34_{10}$
- Podemos utilizar a mesma lógica para representar números com outras bases.
  
# Base Genérica b:
- Um sistema de numeração genérico é composto por b símbolos, onde b é chamada de base.
- Os símbolos são { $0, 1, 2, ..., b-1$ }
- Da mesma forma que no sistema decimal, cada posição de um número genérico representa uma potência de b. Por exemplo, o número $123_b$ representa o número abaixo em base 10:
  - $1 * b^2 + 2 * b^1 + 3 * b^0$
- Para representar um número fracionário, como $12$,$34_b$, podemos utilizar potências negativas de b.
  - $1 * b^1 + 2 * b^0 + 3 * b^{-1} + 4 * b^{-2}$
- O dígito mais a esquerda é o mais significativo (MSD) e o dígito mais a direita é o menos significativo (LSD). 
  - Isso significa que o dígito mais a esquerda tem um peso maior que o dígito mais a direita.
  - Podemos concluir isso dado que o dígito mais a esquerda é multiplicado por uma potência maior que o dígito mais a direita.
  

# Base Binária:
- Como vimos anteriormente, circuitos digitais possuem dois estados: ligado e desligado.
- Essa base é composta por apenas 2 símbolos: { $0, 1$ }
- Por isso, o sistema de numeração binário é muito utilizado em computação. Com ele podemos utilizar circuitos lógicos para realizar operações.
- Cada simbolo é chamado de bit (binary digit).
- Podemos representar números fracionários utilizando a definição, mas essa não é uma prática comum.
- Um conjunto de 8 bits é chamado de byte.

# Base Octal:
- O sistema de numeração octal é composto por 8 símbolos: { $0, 1, 2, 3, 4, 5, 6, 7$ }
- Cada posição de um número octal representa uma potência de 8 (que é $2^3$, isso será importante mais tarde).
- Cuidado para não confundir números octais com números decimais. Por exemplo, o número $10_8$ é diferente de $10_{10}$.
  - $10_8 = 1 * 8^1 + 0 * 8^0 = 8 + 0 = 8_{10}$
  - $10_{10} = 1 * 10^1 + 0 * 10^0 = 10 + 0 = 10_{10}$

# Base Hexadecimal:
- O sistema de numeração hexadecimal é composto por 16 símbolos: { $0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F$ }
- | Decimal | Hexadecimal |
  | --- | ------- |
  | 10  | A       |
  | 11  | B       |
  | 12  | C       |
  | 13  | D       |
  | 14  | E       |
  | 15  | F       |
- Cada posição de um número hexadecimal representa uma potência de 16 (que é $2^4$, isso será importante mais tarde).
- A palavra $FACE_{16}$ é um exemplo de número hexadecimal. Ele representa o número abaixo em base 10:
  - $15 * 16^3 + 10 * 16^2 + 12 * 16^1 + 14 * 16^0 = 15 * 4096 + 10 * 256 + 12 * 16 + 14 = 64206_{10}$

