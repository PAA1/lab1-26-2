# Laboratório Avaliado 1 — Projeto e Análise de Algoritmos I

**Tópicos:** Análise Assintótica · Representações de Grafos · Graus

---

## Instruções

1. Faça o clone deste repositório:
   ```bash
   git clone <URL_DO_REPOSITÓRIO>
   cd lab1-26-2
   ```

2. Abra o arquivo `lab1.py` e complete as funções indicadas com `# TODO`.

3. Em cada função, **preencha também a linha de complexidade**:
   ```python
   # Complexidade: O( )
   ```
   Use $n$ para o número de vértices e $m$ para o número de arestas.

4. Teste sua solução rodando:
   ```bash
   python3 lab1.py
   ```
   Um `✓ OK` indica que o teste passou. Um `✗ FALHOU` indica erro.

5. Ao terminar, **entregue o arquivo `lab1.py`** pela tarefa no Moodle.

---

## Visão Geral das Partes

| Parte | Funções | Conceito |
|-------|---------|----------|
| 1 | `adj_list_to_matrix`, `adj_matrix_to_list` | Conversão entre representações |
| 2 | `grau_lista`, `grau_matriz`, `sequencia_de_graus` | Graus de vértices |
| 3 | `eh_regular`, `conta_arestas`, `vertices_isolados`, `vertice_de_grau_maximo` | Propriedades básicas |
| 4 | `verifica_handshaking` | Lema do Aperto de Mãos |

---

## Representações Usadas

**Lista de adjacência** — `dict[int, list[int]]`

```python
# Grafo  0 — 1 — 2 — 3
adj_list = {0: [1], 1: [0, 2], 2: [1, 3], 3: [2]}
```

**Matriz de adjacência** — `list[list[int]]`

```python
# Mesma grafo; M[i][j] = 1 se existe aresta {i,j}
matrix = [
    [0, 1, 0, 0],
    [1, 0, 1, 0],
    [0, 1, 0, 1],
    [0, 0, 1, 0],
]
```

---

## Observações

- Os grafos neste lab são **simples** e **não-dirigidos**.
- Não use bibliotecas externas (NetworkX, numpy, etc.).
- Não altere as assinaturas das funções nem os testes.
- As complexidades devem ser justificadas em termos de $n$ (vértices) e $m$ (arestas).