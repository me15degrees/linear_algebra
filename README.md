## O que é Álgebra Linear?
É uma ramificação da matemática que estuda vetores, espaços vetoriais (ou espaços lineares), matrizes e sistemas de equações lineares. Ela se concentra na análise de como essas entidades interagem e podem ser manipuladas para resolver problemas em diversas áreas.
O foco deste repositório está em codificar a parte de soluções de sistemas de equações lineares. Alguns métodos existentes são a Redução Gaussiana, Método da Matriz Inversa, entre outros.

### 1. Redução de Gauss (ou Eliminação de Gauss)

*Objetivo*: Transformar um sistema de equações lineares em uma forma mais simples para resolver as variáveis, geralmente usando a forma triangular superior.

*Passos do método*:

- Formação da Matriz Aumentada:
  - Comece formando a matriz aumentada do sistema, que é uma matriz que combina a matriz dos coeficientes A e o vetor dos termos constantes b.
  - Para um sistema de equações Ax=b, a matriz aumentada é [A∣b].

- Transformação para a Forma Escalonada:
  - Use operações elementares de linha para transformar a matriz aumentada em uma forma triangular superior. As operações elementares são:
  - Trocar duas linhas.
  - Multiplicar uma linha por um escalar não zero.
  - Adicionar ou subtrair múltiplos de uma linha a outra.
  - O objetivo é criar zeros abaixo da diagonal principal da matriz dos coeficientes.

- Substituição Retroativa:
  - Após transformar a matriz em uma forma triangular superior, resolva o sistema começando pela última equação e substitua as variáveis para cima.
  - Esse processo é chamado de substituição retroativa e é usado para encontrar os valores das variáveis.

#### Exemplo:

Para o sistema de equações:
```
⎨x+2y+3z=9
⎨2x+3y+4z=18
⎨3x+4y+5z=27
```

Forme a matriz aumentada:

```
[123∣ 9]
[234∣ 18]
[345∣ 27]
```

### 2. Método da Matriz Inversa

*Objetivo*: Encontrar a solução para um sistema de equações lineares usando a inversa da matriz dos coeficientes, se ela existir.

*Passos do Método*:

- Formação da Matriz Aumentada:
    - Para o sistema Ax=b, você precisa apenas da matriz dos coeficientes A e do vetor dos termos constantes b.

- Verificação da Inversibilidade:
   -  Verifique se a matriz dos coeficientes A é invertível. Uma matriz é invertível se seu determinante é não zero.
    - Se o determinante de A for zero, o sistema pode ser singular ou ter infinitas soluções.

- Cálculo da Matriz Inversa:
    - Se A for invertível, calcule sua inversa A⁻¹.
    - Há métodos para encontrar a inversa, como a fórmula de adjunta, eliminação de Gauss-Jordan ou decomposição LU.

- Encontrar a Solução:
    Use a inversa da matriz AA para encontrar a solução do sistema: x=A⁻¹b.

#### Exemplo:

Para o sistema:
Ax=b

- Calcule a inversa de A, denotada por A⁻¹.

- Multiplique A⁻¹ por b para encontrar x: x=A⁻¹b

Exemplo Numérico:

Para o sistema:
```
{x+y=2
{2x+3y=5
```
A matriz dos coeficientes A é:
```
A=[11]
  [​23​]
```
O vetor dos termos constantes b é:
```
b=[2]
  [​5​]
```
