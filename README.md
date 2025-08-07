# Lista Estática com Cursor

Este projeto implementa uma **lista duplamente encadeada com cursor** em C++, utilizando **alocação estática com vetor e união de estruturas**. Ele simula operações de inserção, remoção, pesquisa e visualização dos elementos da lista, mantendo o controle de memória manualmente, sem uso de ponteiros dinâmicos convencionais.

---

## 🧠 Conceito

- A posição `0` do vetor é reservada para o **cabeçalho** da lista.
- As demais posições representam células que podem estar **ocupadas** ou **livres**, com controle feito por índices.
- Utiliza uma `union` com duas visões:
  - **Cabeçalho**: armazena metadados (quantidade, início, fim e posição livre).
  - **Lista**: representa os nós com campos `next`, `prev` e o dado `chave`.

---

## ✨ Funcionalidades

- Inserção no final da lista (`insere`)
- Inserção ordenada pela chave (`insereOrdenado`)
- Remoção de elementos por chave (`remove`)
- Pesquisa de elementos (`pesquisa`)
- Impressão dos registros ativos (`imprimeRegistros`)
- Visualização da estrutura completa (`imprimeEstrutura`)

---

## ▶️ Como usar

1. Compile o código:

```
g++ -o lista lista.cpp
```

2. Execute o programa:

```
./lista
```

3. Interaja com o menu:

```
Menu:
1 - Inserir
2 - Remover
3 - Pesquisar
4 - Imprimir registros
5 - Imprimir estrutura
6 - Inserir ordenado
0 - Sair
```

---

## 🧪 Exemplo de uso

```
Tamanho da lista: 10

Menu:
1 - Inserir
Chave: 5

1 - Inserir
Chave: 8

5 - Imprimir estrutura
...
```

---

## 🛠️ Requisitos

- Compilador C++ (ex: `g++`)
- Terminal para execução interativa

---

## 📚 Aprendizado

Este projeto é ideal para estudantes de **estrutura de dados**, pois demonstra:

- Implementação de listas sem ponteiros reais (usando índices)
- Gerenciamento manual de memória simulada
- Uso avançado de `union` para múltiplas interpretações de dados

---

## 👨‍💻 Autor

**Bernardo Carvalho Guerra**

