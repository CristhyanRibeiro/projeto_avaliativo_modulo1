# Projeto Final — Módulo 1
## Manutenção Preditiva de Máquinas

Projeto desenvolvido no curso de Desenvolvimento de IA para Análise Preditiva, do programa SCTEC.

### Objetivo

Analisar dados operacionais de máquinas e comparar algoritmos de classificação para identificar possíveis falhas.

### Base de dados

A base contém 10.000 registros e 14 colunas. A variável alvo é `falha_maquina`, sendo 0 para operação normal e 1 para falha.

Foram identificados 339 registros com falha, correspondentes a 3,39% da base.

### Etapas desenvolvidas

1. Análise exploratória e visualização dos dados.
2. Verificação de duplicatas, valores ausentes e outliers.
3. Tratamento dos valores ausentes.
4. Engenharia de atributos.
5. Separação dos dados e balanceamento com Random Under Sampling.
6. Padronização com StandardScaler.
7. Treinamento e avaliação de KNN e Árvore de Decisão.

### Resultados

| Modelo | Acurácia de teste |
|---|---:|
| KNN — K=3 | 84,25% |
| KNN — K=5 | 85,35% |
| KNN — K=7 | 84,80% |
| Árvore — Profundidade 3 | 88,85% |
| Árvore — Profundidade 5 | 88,75% |
| Árvore — Profundidade 7 | 88,80% |
| Árvore — Sem limite | 87,70% |

A Árvore de Decisão com profundidade 3 apresentou a maior acurácia no conjunto de teste. A árvore sem limite mostrou sinais de overfitting, alcançando 100% no treinamento e 87,70% no teste.

A acurácia deve ser interpretada com cautela devido ao desbalanceamento original das classes.

### Como executar

Utilizar Python e instalar as dependências:

```bash
pip install -r requirements.txt
```

Abrir `manutencao_preditiva.ipynb` no VS Code ou Jupyter Notebook e executar as células na sequência.

O arquivo CSV deve permanecer dentro da pasta `data`.

### Estrutura

```text
Projeto Final Modulo 1/
├── data/
│   └── manutencao_preditiva.csv
├── manutencao_preditiva.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```
