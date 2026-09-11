# Comunicação Off-Grid com Dijkstra

Este projeto foi desenvolvido em C com o objetivo de demonstrar uma aplicação simples do algoritmo de Dijkstra.

A ideia principal não é criar um sistema real de comunicação, mas usar uma rede fictícia de antenas para mostrar, de forma prática, como o algoritmo pode encontrar o menor caminho dentro de um grafo.

## Sobre o projeto

No programa, cada antena é representada como um vértice do grafo.

As conexões entre as antenas representam as arestas, e cada conexão possui uma distância associada.

Dessa forma, podemos imaginar que uma mensagem precisa sair de uma antena e chegar até outra, podendo passar por várias antenas intermediárias.

O objetivo é encontrar a rota com a menor distância total.

É nesse ponto que o algoritmo de Dijkstra é utilizado.

## Como o Dijkstra é aplicado

O algoritmo parte de uma antena de origem e calcula a menor distância possível até as outras antenas da rede.

Durante o processo, ele compara os caminhos disponíveis e mantém sempre a menor distância encontrada.

No final, o programa consegue mostrar qual sequência de antenas deve ser utilizada para chegar ao destino com o menor custo.

Neste projeto, esse custo é representado pela distância entre as antenas.

Por exemplo:

```text
Antena 3 ---- 0.8 km ---- Antena 5
   |
 1.6 km
   |
Antena 2 ---- 1.0 km ---- Antena 6
```

Mesmo que existam vários caminhos possíveis entre duas antenas, o Dijkstra procura aquele cuja soma das distâncias seja a menor.

## Exemplo

O programa utiliza uma antena como ponto de origem e permite escolher uma antena de destino.

Depois disso, é possível digitar uma mensagem.

Um exemplo de saída seria:

```text
Voce é a antena 3

Escolha a antena de destino: 8
Digite a mensagem: Ola

Enviando mensagem pela menor rota:
3 - 5 - 6 - 8

Mensagem enviada: Ola
```

A sequência apresentada representa o menor caminho encontrado pelo algoritmo.

## Arquivo de antenas

As conexões da rede são lidas a partir de um arquivo de texto.

Cada linha representa uma conexão entre duas antenas e a distância entre elas.

Exemplo:

```text
3 5 0.8
2 6 1.0
6 7 1.8
```

De forma geral:

```text
antena1 antena2 distancia
```

Esses dados são utilizados para montar o grafo que será analisado pelo algoritmo.

## Objetivo

O projeto tem caráter didático e serve principalmente para facilitar a compreensão do algoritmo de Dijkstra.

A ideia é mostrar como um problema de menor caminho pode ser relacionado a uma situação mais fácil de visualizar, neste caso, o envio de mensagens entre antenas de uma rede fictícia.
