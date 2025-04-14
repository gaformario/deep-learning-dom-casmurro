**Recuperação de Trechos Literários Usando RAG Contexto**

Este projeto implementa um sistema RAG (Retrieval-Augmented Generation) que utiliza técnicas de Processamento de Linguagem Natural (NLP) para responder perguntas sobre o livro Dom Casmurro, de Machado de Assis. O sistema combina busca semântica e modelos de Question Answering (QA) para fornecer respostas baseadas no conteúdo do livro.

O sistema realiza as seguintes etapas:
- Pré-processa o texto do livro, dividindo-o em blocos (capítulos).
- Gera embeddings semânticos para os blocos usando o modelo all-MiniLM-L6-v2.
- Indexa os embeddings em um índice vetorial utilizando a biblioteca hnswlib.
- Recebe perguntas do usuário, recupera o bloco mais relevante e utiliza dois modelos de QA (distilbert-base-uncased-distilled-squad e deepset/roberta-base-squad2) para gerar respostas.
- Compara as respostas e scores dos dois modelos para identificar o melhor desempenho.

