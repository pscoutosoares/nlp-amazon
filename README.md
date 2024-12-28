# Análise de Sentimentos em Reviews da Amazon

## [Slide da apresentação](/pln-amazon.pdf)
## [Video da apresentação](/)
## [ipynb](/nlp_amazon.ipynb)


## Contexto do Problema

No e-commerce, dois problemas críticos afetam diretamente a experiência de compra e as vendas:
1. **Cálculo correto das pontuações de produtos após a venda**:
   - Garante maior satisfação do cliente.
   - Melhora a visibilidade de produtos bem avaliados.
   - Oferece uma experiência de compra confiável para os clientes.

2. **Ordenação correta dos comentários sobre os produtos**:
   - Evita o destaque de comentários enganosos.
   - Previne perdas financeiras e de clientes.

A solução desses problemas beneficia:
- **Clientes**: Jornada de compra mais segura e satisfatória.
- **Vendedores**: Maior destaque para produtos de qualidade.
- **E-commerce**: Aumento da confiança e das vendas na plataforma.

## Abordagem Estudada

Este repositório explora diferentes abordagens para realizar a **análise de sentimentos** em reviews de produtos da Amazon, utilizando o dataset [Amazon Product Data](https://www.kaggle.com/datasets/tarkkaanko/amazon?resource=download). 

### Etapas do Estudo

1. **Pré-processamento dos Dados**:
   - Remoção de pontuações e palavras irrelevantes (stopwords).
   - Conversão de textos para minúsculas.
   - Mapeamento das notas em sentimentos: `positivo`, `negativo` e `neutro`.

2. **Análise Exploratória e Visualização**:
   - Geração de **nuvens de palavras** para identificar termos mais frequentes.
   - Análise da distribuição de sentimentos.
   - Comparação do tamanho médio de reviews entre diferentes sentimentos.

3. **Modelagem**:
   - **SVM com Bag of Words**: Captura a frequência de palavras nos textos.
   - **SVM com Embeddings (spaCy)**: Representa os textos de forma vetorial, considerando semântica.
   - **BERT (Fine-tuning)**: Modelo avançado de linguagem pré-treinado ajustado para a tarefa.

4. **Avaliação**:
   - Métricas usadas: **Acurácia** e **F1-Score**.
   - Comparação de desempenho entre os modelos.

## Resultados

Os resultados indicaram que o modelo **BERT** apresentou o melhor desempenho geral, seguido pelo **SVM com Bag of Words**. O **SVM com Embeddings** teve resultados satisfatórios, mas limitados devido à simplicidade da abordagem.

### Métricas de Desempenho

| Modelo                  | Acurácia | F1-Score |
|-------------------------|----------|----------|
| SVM + Bag of Words      | 0.81     | 0.76     |
| SVM + Embeddings (spaCy)| 0.80     | 0.70     |
| BERT (Fine-tuning)      | 0.82     | 0.77     |

### Dataset

Os dados utilizados neste estudo podem ser encontrados em:
[Amazon Product Data](https://www.kaggle.com/datasets/tarkkaanko/amazon?resource=download)


