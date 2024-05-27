<h1 align="center"> 🧮 Sistemas de Numeração 🧮 <br>
  <a href="../[  1 ] Sinais Analógicos x Sinais Digitais/"><img src="https://img.shields.io/badge/Anterior-Sinais Analógicos x Sinais Digitais-215a36" alt="Anterior"></a>
  <a href="../[  3 ] Descrição de Circuitos Lógicos/"><img src="https://img.shields.io/badge/Próximo-Descrição de Circuitos Lógicos-215a36" alt="Próximo"></a>
</h1>

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

# Conversão entre Bases:
- Para converter qualquer número de uma base b para a base 10, podemos utilizar a definição de base genérica.
  - $\sum_{i=0}^{n} A_i * b^i$
  - $A_i$ é o i-ésimo dígito do número e n é o número de dígitos.
    - $A_n * b^n + A_{n-1} * b^{n-1} + ... + A_1 * b^1 + A_0 * b^0$
- Para converter um número de base 10 para uma base b, utilizamos o método das divisões sucessivas.
  - Dividimos o número por b e guardamos o resto da divisão.
  - O resto da divisão é o dígito menos significativo.
  - Dividimos o resultado da divisão inteira por b e guardamos o resto da divisão.
  - Repetimos o processo até que o resultado da divisão inteira seja 0.
  - O número convertido é formado pelos restos das divisões, do último para o primeiro.
  - Por exemplo, para converter o número 123 para binário:
    - $123 / 2 = 61$ resto 1
    - $61 / 2 = 30$ resto 1
    - $30 / 2 = 15$ resto 0
    - $15 / 2 = 7$ resto 1
    - $7 / 2 = 3$ resto 1
    - $3 / 2 = 1$ resto 1
    - $1 / 2 = 0$ resto 1
    - Logo, $123_{10} = 1111011_2$
- Conversões entre bases diferentes de 10 podem ser feitas utilizando a base 10 como intermediária.
  - Por exemplo, para converter o número $123_8$ para binário:
    - $123_8 = 1 * 8^2 + 2 * 8^1 + 3 * 8^0 = 64 + 16 + 3 = 83_{10}$
    - $83_{10} = 1010011_2$
    - Logo, $123_8 = 1010011_2$
  - Nesse caso em específico, a conversão pode ser feita diretamente, pois 8 é uma potência de 2.
    - Podemos fazer isso convertendo blocos de 1 dígito octal para 3 dígitos binários (pois $2^3 = 8$).
-   | Octal | Binário |
    | --- | ----- |
    | 0   | 000   |
    | 1   | 001   |
    | 2   | 010   |
    | 3   | 011   |
    | 4   | 100   |
    | 5   | 101   |
    | 6   | 110   |
    | 7   | 111   |
    - Basta substituir cada dígito octal pelo seu equivalente em binário (sempre com 3 dígitos, mesmo que contenha zeros a esquerda).
    - $1 = 001, 2 = 010, 3 = 011$ então $123_8 = 001010011_2 = 1010011_2$
  - O mesmo pode ser feito para converter de hexadecimal para binário, pois 16 é uma potência de 2.
    - Nesse caso, cada dígito hexadecimal é substituído por 4 dígitos binários. Muito cuidado para não esquecer de manter os zeros a esquerda.
  - Um uso muito comum para esses sistemas de numeração é justamente esse, condensar números binários (facilitando a leitura) de forma rápida.

# Contagem em Sistemas de Numeração Posicional:
- Como fazemos para contar em decimal? 
  - Utilizamos os dígitos de 0 a 9 e, quando chegamos no 9, voltamos para 0 e incrementamos o dígito à esquerda.
- Podemos utilizar a mesma lógica para contar em qualquer base. Contamos de 0 até b-1 e, quando chegamos no b-1, voltamos para 0 e incrementamos o dígito à esquerda.

| Decimal | Binário | Octal | Hexadecimal |
| ------- | ------- | ----- | ----------- |
| 0       | 0       | 0     | 0           |
| 1       | 1       | 1     | 1           |
| 2       | `10`    | 2     | 2           |
| 3       | 11      | 3     | 3           |
| 4       | `100`   | 4     | 4           |
| 5       | 101     | 5     | 5           |
| 6       | 110     | 6     | 6           |
| 7       | 111     | 7     | 7           |
| 8       | `1000`  | `10`  | 8           |
| 9       | 1001    | 11    | 9           |
| `10`    | 1010    | 12    | A           |
| 11      | 1011    | 13    | B           |
| 12      | 1100    | 14    | C           |
| 13      | 1101    | 15    | D           |
| 14      | 1110    | 16    | E           |
| 15      | 1111    | 17    | F           |
| 16      | `10000` | 20    | `10`        |





# Binary Coded Decimal (BCD)
- O BCD é uma outra forma de representar números decimais em binário.
- Nela, cada dígito decimal é representado por um número binário de 4 bits. 
  - A conversão utiliza a mesma lógica da conversão entre hexadecimal e binário.
  
- Vantagem: Facilidade de conversão entre decimal e binário.
- Desvantagem: Ineficiência de espaço, pois cada dígito decimal é representado por 4 bits. Existem 16 combinações possíveis, mas apenas 10 são utilizadas.
  - $730_{10}$ em BCD é 0111 0011 0000
  - 0001 0010 0011 em BCD é $123_{10}$

---

<p align="center">
    <a href="../[  1 ] Sinais Analógicos x Sinais Digitais/"><img src="https://img.shields.io/badge/Anterior-Sinais Analógicos x Sinais Digitais-215a36" alt="Anterior"></a>
    <a href="../[  3 ] Descrição de Circuitos Lógicos/"><img src="https://img.shields.io/badge/Próximo-Descrição de Circuitos Lógicos-215a36" alt="Próximo"></a>
</p>