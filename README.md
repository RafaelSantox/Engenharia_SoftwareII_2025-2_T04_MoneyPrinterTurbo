# Introdução

---

O projeto em questão tem como objetivo identificar os padrões arquiteturais presentes no repositório [MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo), utilizando de LLMs para tal. A realização do projeto ocorreu mediante a etapa de análise manual, seguida da análise com LLMs.

## Análise manual

Inicialmente, foi feita uma análise manual do projeto através da exploração do arquivo README e uma investigação do próprio código em busca de padrões arquiteturais que as LLMs deveriam identificar.

## Análise com LLMs

Utilizamos algumas LLMs do [HuggingFace](https://huggingface.co/models) que tinham como tag as tarefas code search, semantic search ou text classification. Para trabalhar com as LLMs, foram criados 3 notebooks no [GoogleColab](https://colab.google/), que possui um ambiente de execução com GPU <i>Python 3 Google Compute Engine backend</i>, 12.67GB de RAM e 112.64GB de armazenamento.

A seguir, uma relação da escolha das LLMs e justificativa para escolha:

|Task|Modelo(s)|Justificativa|
|:--------:|:---------:|:------------:|
|Code Search|[<i>microsoft/graphcodebert-base</i>](https://huggingface.co/microsoft/graphcodebert-base) e [<i>mistralai/Mistral-7B-Instruct-v0.2</i>](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.2) (auxiliar)|A justificativa para uso do graphcodebert-base foi a sua capacidade de entender as relações sintáticas entre os tokens gerados com o uso de grafos. O uso da Mistral-7B-Instruct-v0.2 como auxiliar se deu principalmente por ser um modelo leve e conversacional, resumindo assim a análise feita pelo graphcodebert-base.|
|Semantic Search|[<i>sentence-transformers/all-MiniLM-L6-v2</i>](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)|Este modelo é notável por ser extremamente leve e gerar resultados precisos com um processamento rápido, o que é ideal para ambientes com recursos limitados, como o Google Colab. Sua facilidade de uso o torna particularmente adequado para equipes que não possuem familiaridade avançada com LLMs, garantindo a geração eficaz de embeddings vetoriais de alta qualidade sem a necessidade de infraestrutura de hardware dedicada.|
|Text Classification|[<i>google/flan-t5-xl</i>](https://huggingface.co/google/flan-t5-xl) e [<i>BART-Large-MNLI</i>](https://huggingface.co/facebook/bart-large-mnli)|O Flan-T5-XL foi selecionado devido sua flexibilidade em seguir prompts mais complexos, além de possuir um equilíbrio entre desempenho e performance se comparado a modelos maiores, também é um modelo open-source facilitando seu uso para pequenos projetos. O modelo BART-Large-MNLI BART combina um encoder (como BERT) e um decoder (semelhante ao GPT), o que dá a ele bastante flexibilidade de geração, permite usar a inferência textual para classificar textos, é uma  boa escolha para sistemas de classificação onde você não tem muitos dados rotulados.|

# Como executar

---

Para executar, basta baixar os arquivos da pasta colab_notebooks e fazer upload no [GoogleColab](https://colab.google/). Cada arquivo representa um notebook diferente no colab e deve ser executado separadamente. As dependências necessárias serão baixadas automaticamente ao executar. Um tutorial mais detalhado se encontra no relatório, localizado na pasta docs deste repositório ou através do link abaixo.

# Links úteis

---

Relatório da atividade, contendo uma análise e explicação mais aprofundada do projeto: [Relatório](https://docs.google.com/document/d/13JeSUXYwiZQ4xPF2bBD3F7DLP3tkuZYV6Az2UTz_q3k/edit?usp=sharing)


Vídeo explicando o trabalho realizado: [Vídeo](https://drive.google.com/file/d/13TOlqN0ehvGoFXwxhYfdF4glymIugiKd/view?usp=sharing)

# Relação dos participantes

---

|Nome|Matrícula|Contribuição|
|:--------:|:---------:|:------------:|
|Fernanda da Silva Santos|202300061581|Escolha do projeto alvo de análise, uso da LLM  sentence-transformers/all-MiniLM-L6-v2 para análise do código-fonte, escrita do relatório, gravação do vídeo|
|Gustavo Rodrigues dos Santos|202300061939|Escolha do projeto alvo de análise, uso da LLM FLAN-T5-XL para análise do código fonte do repositório e a LLM BART-Large-MNLI para classificar o padrão da arquitetura, escrita e revisão do relatório, gravação do vídeo.|
|Joao Santos Rocha|202300061948|Escolha do projeto alvo de análise, uso das LLMs GraphCodeBERT para detecção de padrões de código e Mistral-7B-Instruct para análise semântica, escrita do relatório, gravação do vídeo.|
|Jose Henrique Souza Santana|202300061699|Escolha do projeto alvo de análise, uso das LLMs GraphCodeBERT para detecção de padrões de código e Mistral-7B-Instruct para análise semântica, escrita do relatório, gravação do vídeo.|
|Jose Luiz de Jesus Souza|201800138910|O integrante não contribuiu com a atividade.|
|Lais Santos de Sousa|202100115364|Escolha do projeto alvo de análise, uso da LLM sentence-transformers/all-MiniLM-L6-v2 por meio de script para análise do código fonte, escrita do relatório, gravação do vídeo.|
|Rafael de Jesus Santos|202300114489|Escolha do projeto alvo de análise, uso da  LLM FLAN-T5-XL para gerar um resumo técnico do projeto e a LLM BART-Large-MNLI para classificar o padrão arquitetural, escrita do relatório e gravação do vídeo.|
|Tasso Marcel de Oliveira|202300061984|Escolha do projeto alvo de análise, identificação manual dos padrões arquiteturais, uso da  LLM FLAN-T5-XL para gerar um resumo técnico do projeto e a LLM BART-Large-MNLI para classificar o padrão arquitetural, escrita do relatório e gravação do vídeo.|
