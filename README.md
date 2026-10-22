# Ciclo LevelUp UCB 2026.2 — Desafio RAG com *Os Sertões*

## Sobre o desafio

Este repositório reúne a implementação de técnicas de Retrieval-Augmented Generation (RAG), utilizando a obra *Os Sertões*, de Euclides da Cunha, como fonte de consulta.

O objetivo é explorar diferentes estratégias de recuperação de informações e geração de respostas fundamentadas no conteúdo do livro, observando suas características, resultados e limitações.

**Curso:** Ciclo LevelUp UCB 2026.2  
**Projeto:** Desafio de implementação de RAG

## Métodos implementados

- **Naive RAG:** recuperação de trechos por similaridade semântica.
- **Parent RAG:** recuperação de trechos menores com utilização de blocos maiores como contexto.
- **Rerank RAG:** reordenação dos trechos candidatos por meio de um segundo modelo de relevância.

## Perguntas do desafio

O experimento considera cinco questões relacionadas à obra:

1. Como o ambiente natural do sertão influencia a vida de seus habitantes?
2. Quais características dos sertanejos são apresentadas e como se relacionam com o ambiente?
3. Qual contexto histórico e político contribuiu para a Guerra de Canudos?
4. Qual foi o papel de Antônio Conselheiro no movimento de Canudos?
5. Quais críticas sociais e políticas aparecem na obra e que visão do Brasil Euclides da Cunha apresenta?

## Tecnologias utilizadas

- Python
- Google Colab
- PyMuPDF
- Sentence Transformers
- FAISS
- Transformers
- PyTorch

## Organização do repositório

```text
os-sertoes-rag/
├── README.md
├── naive-rag.ipynb
├── parent-rag.ipynb
└── rerank-rag.ipynb
```

Cada notebook deve conter a implementação do método correspondente, a recuperação de informações e os resultados das perguntas do desafio.

## Resultados e limitações

Nos testes preliminares, foram recuperados trechos relacionados à seca e às condições naturais do sertão. A abordagem Parent RAG permitiu ampliar o contexto, enquanto o Rerank RAG reordenou os resultados sem apresentar melhoria clara na relevância para a pergunta testada.

O modelo de linguagem também apresentou respostas com informações não sustentadas pelos trechos recuperados. Por isso, a fidelidade ao texto original deve ser considerada na avaliação dos resultados.

Essas observações são preliminares e não permitem concluir qual método apresenta melhor desempenho em todas as perguntas.

## Como executar

1. Abra o notebook desejado no Google Colab.
2. Execute as células em ordem.
3. Aguarde a instalação das dependências e o processamento do PDF.
4. Execute a recuperação de trechos e analise os resultados.

A execução depende de acesso à internet para baixar o documento e os modelos utilizados.

## Fonte

Euclides da Cunha — *Os Sertões*. O documento utilizado como fonte é baixado pelo notebook, não sendo necessário incluir o PDF no repositório.

## Objetivo acadêmico

Este projeto foi desenvolvido no contexto do Ciclo LevelUp UCB 2026.2, com foco na experimentação prática de técnicas de recuperação aumentada por geração.
