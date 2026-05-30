# Atividade Hugging Face - RAG em Python

## Tema escolhido

RAG (Retrieval-Augmented Generation)

## Descricao do problema

Modelos de linguagem podem gerar respostas corretas, mas tambem podem responder de forma vaga ou inventar informacoes quando nao recebem contexto suficiente. O problema abordado nesta atividade foi mostrar como um sistema de RAG pode recuperar trechos relevantes antes da geracao da resposta.

## Solucao desenvolvida

Foi criada uma mini aplicacao em Python com bibliotecas do ecossistema Hugging Face. A aplicacao:

1. define uma pequena base de documentos;
2. gera embeddings com `sentence-transformers/all-MiniLM-L6-v2`;
3. calcula similaridade cosseno para recuperar os textos mais relevantes;
4. envia o contexto recuperado para o modelo `google/flan-t5-base`;
5. gera a resposta final em linguagem natural.

## Estrutura do repositorio

- `rag_huggingface_demo.ipynb`: notebook principal da atividade
- `slides_apresentacao.pdf`: apresentacao em 3 slides
- `slides_apresentacao.md`: roteiro da apresentacao
- `requirements.txt`: dependencias do projeto

## Como executar

Recomendado: Google Colab ou ambiente local com Python 3.10+.

Abra o notebook `rag_huggingface_demo.ipynb` e execute as celulas em ordem.

A primeira celula pode ser usada para instalar as dependencias no mesmo Python do notebook.

Se preferir instalar manualmente:

```bash
pip install -r requirements.txt
```

## Resultado obtido

O notebook foi executado com sucesso e gerou:

- os documentos recuperados com seus scores de similaridade;
- o contexto enviado ao modelo;
- uma resposta final gerada pelo `flan-t5-base`.

Exemplo de pergunta testada:

`Como o RAG ajuda a reduzir alucinacoes em modelos de linguagem?`

## Integrantes

Preencha com o(s) nome(s) do grupo, se houver:

- Seu nome

## Referencias

- Hugging Face. https://huggingface.co/
- Transformers documentation. https://huggingface.co/docs/transformers/index
- Sentence Transformers documentation. https://www.sbert.net/
- Lewis, Patrick et al. Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks. https://arxiv.org/abs/2005.11401
