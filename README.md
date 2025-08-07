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

## 📦 Estrutura de Dados

```cpp
struct dados {
    int chave;
};

union celula {
    struct { int quant, first, last, free; } cabecalho;
    struct { int next, prev; dados reg; } lista;
};
