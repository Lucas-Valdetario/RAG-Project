Chat com PDF (RAG)
Este projeto utiliza LangChain, OpenAI e ChromaDB para permitir que você faça perguntas a um arquivo PDF e receba respostas baseadas no conteúdo do documento (técnica de Retrieval-Augmented Generation).

🚀 Como funciona
Carregamento: O PDF é lido e dividido em páginas.

Processamento: O texto é quebrado em chunks (pedaços) menores para facilitar a busca.

Vetorização: O código gera embeddings das informações e as salva em um banco de dados local (Chroma).

Consulta: Ao fazer uma pergunta, o sistema busca os trechos mais relevantes e os envia para o GPT da OpenAI gerar uma resposta precisa.

🛠️ Tecnologias utilizadas
LangChain: Framework para orquestração da lógica de IA.

OpenAI (GPT-3.5-Turbo): Modelo de linguagem para geração de respostas.

ChromaDB: Banco de dados vetorial para armazenamento dos documentos.

Python Decouple: Para gerenciamento de variáveis de ambiente.

📋 Pré-requisitos
Antes de rodar o notebook, você precisará de:

Uma chave de API da OpenAI (OPENAI_API_KEY).

Python instalado (recomenda-se criar um ambiente virtual).

Instalar as dependências:

Bash
pip install langchain langchain-openai langchain-community chromadb pypdf python-decouple
⚙️ Configuração
Crie um arquivo .env na raiz do projeto e adicione sua chave:

Snippet de código
OPENAI_KEY=sua_chave_aqui
📖 Como usar
Basta abrir o arquivo rag.ipynb em seu ambiente Jupyter e executar as células em ordem. Na última célula, o programa abrirá um campo de input para você digitar sua pergunta sobre o PDF configurado.
