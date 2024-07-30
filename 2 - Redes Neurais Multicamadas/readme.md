# Documentação do Curso de Redes Neurais Artificiais

Este documento fornece um resumo detalhado dos conceitos e processos aprendidos no curso de Redes Neurais Artificiais da Udemy. Ele cobre desde as diferenças entre redes neurais de uma camada e multicamadas até a implementação completa de uma rede neural.

## Índice

1. [Redes Neurais de Uma Camada vs. Multicamadas](#redes-neurais-de-uma-camada-vs-multicamadas)
2. [Funções de Ativação](#funções-de-ativação)
3. [Processo Completo Feedforward com XOR](#processo-completo-feedforward-com-xor)
4. [Função de Erro](#função-de-erro)
5. [Gradient Descent (Descida do Gradiente)](#gradient-descent-descida-do-gradiente)
6. [Backpropagation (Retropropagação)](#backpropagation-retropropagação)
7. [Implementação Completa Passo a Passo](#implementação-completa-passo-a-passo)

---

## Redes Neurais de Uma Camada vs. Multicamadas

### Uma Camada

Redes neurais de uma camada, também conhecidas como redes neurais de perceptron, possuem apenas uma camada de neurônios (a camada de saída) além da camada de entrada. Elas são adequadas para problemas que são linearmente separáveis. Um exemplo clássico é o problema de classificação linear.

### Multicamadas

Redes neurais multicamadas, ou redes neurais profundas, possuem uma ou mais camadas ocultas entre a camada de entrada e a camada de saída. Essas redes podem modelar relações não lineares e resolver problemas mais complexos que redes de uma camada não conseguem. São usadas em tarefas como reconhecimento de imagem e processamento de linguagem natural.

---

## Funções de Ativação

Funções de ativação introduzem não linearidade na rede neural e ajudam a modelar relações complexas entre os dados. Aqui estão algumas das funções de ativação mais comuns:

- **Função Sigmoide**: 

  `σ(x) = 1 / (1 + e^(-x))`

- **Função Tangente Hiperbólica (tanh)**: 

  `tanh(x) = (e^x - e^(-x)) / (e^x + e^(-x))`

- **Função ReLU (Rectified Linear Unit)**: 

  `ReLU(x) = max(0, x)`

Cada função tem suas próprias vantagens e desvantagens, e a escolha depende do problema específico e da arquitetura da rede.

---

## Processo Completo Feedforward com XOR

O problema XOR é um exemplo clássico usado para ilustrar redes neurais multicamadas. O objetivo é criar uma rede que possa aprender a função XOR, que não é linearmente separável.

### Passos:

1. **Definir a Arquitetura**: Usar uma rede neural com uma camada oculta.
2. **Propagação para Frente**: Calcular a saída da rede aplicando as funções de ativação.
3. **Comparar com o Valor Real**: Avaliar a saída da rede com a saída esperada.
4. **Ajustar Pesos**: Atualizar os pesos para minimizar o erro.

---

## Função de Erro

A função de erro mede a diferença entre a saída prevista pela rede e a saída real. É usada para avaliar a performance do modelo e guiar o processo de treinamento. Algumas funções de erro comuns incluem:

- **Erro Quadrático Médio (MSE)**:

  `MSE = 1/n * Σ(y_i - ŷ_i)^2`

- **Entropia Cruzada** (para problemas de classificação):

  `Cross-Entropy = - Σ(y_i * log(ŷ_i))`

---

## Gradient Descent (Descida do Gradiente)

O Gradient Descent é um método de otimização usado para minimizar a função de erro ajustando os pesos da rede neural. O processo envolve:

1. **Calcular o Gradiente**: Determinar a direção e a taxa de mudança da função de erro em relação aos pesos.
2. **Atualizar os Pesos**: Ajustar os pesos na direção oposta ao gradiente para reduzir o erro.

### Fórmula:

`Peso(n+1) = Peso(n) - Taxa de Aprendizagem * Gradiente do Erro`

---

## Backpropagation (Retropropagação)

Backpropagation é o algoritmo usado para treinar redes neurais, ajustando os pesos com base no erro calculado. O processo inclui:

1. **Propagação para Frente**: Calcular a saída da rede para uma entrada.
2. **Calcular o Erro**: Comparar a saída calculada com a saída esperada.
3. **Retropropagação do Erro**: Calcular o gradiente do erro em relação aos pesos e propagar o erro de volta através da rede.
4. **Atualizar os Pesos**: Ajustar os pesos usando o gradiente calculado para reduzir o erro.

---

## Implementação Completa Passo a Passo

1. **Configuração da Rede**: Definir a arquitetura da rede neural, incluindo o número de camadas e neurônios.
2. **Inicialização dos Pesos**: Atribuir valores iniciais aos pesos.
3. **Propagação para Frente**: Implementar o cálculo da saída da rede.
4. **Cálculo da Função de Erro**: Medir o desempenho da rede usando uma função de erro.
5. **Retropropagação**: Implementar o algoritmo de retropropagação para ajustar os pesos.
6. **Treinamento**: Iterar sobre o conjunto de dados, ajustando os pesos até que o erro seja minimizado.
7. **Avaliação e Teste**: Avaliar o desempenho da rede em dados de teste.

<p align="center">
  <img src="assets/Redes_Neurais_Exemplo.png" alt="Descrição da Imagem" width="300" height="200" />
</p>
