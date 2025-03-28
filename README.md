Chatbot de Informações sobre Cidades Brasileiras

📖 Sumário

Descrição do Projeto

Memória

Glossário

Instalação

Configuração

Execução

Explicação dos Blocos de Código

Licença

📄 Descrição do Projeto

Este projeto é um chatbot que fornece informações sobre cidades brasileiras utilizando o modelo Groq via integração com a biblioteca LangChain. O chatbot armazena o histórico de mensagens de cada sessão, permitindo um diálogo contínuo e dinâmico.

🧠 Memória

O sistema armazena o histórico de conversas de cada sessão por meio da classe ChatMessageHistory da biblioteca LangChain. Este histórico é gerido e acessado por meio de funções que garantem que cada usuário tenha uma sessão separada e persistente durante a execução.

📚 Glossário

LangChain: Biblioteca que facilita a criação de aplicações que usam modelos de linguagem de maneira encadeada.

Groq: Modelo de linguagem utilizado neste projeto.

Prompt Template: Modelo de prompt que define a estrutura da comunicação entre o usuário e o chatbot.

Histórico de Mensagens: Registro contínuo de interações entre o usuário e o chatbot, armazenado e recuperado durante cada sessão.

Pipeline de Execução: Sequência lógica de execução de funções e modelos.

💻 Instalação

Clonando o Repositório

$ git clone <URL_DO_SEU_REPOSITÓRIO>
$ cd chatbot_cidades_br

Criando o Ambiente Virtual

$ python -m venv venv
$ source venv/bin/activate  # Linux / Mac
$ .\venv\Scripts\activate  # Windows

Instalando as Dependências

$ pip install -r requirements.txt

🔑 Configuração

Crie um arquivo .env na raiz do projeto e adicione sua chave de API do Groq da seguinte maneira:

GROQ_API_KEY=SUACHAVEAQUI

🚀 Execução

Para iniciar o projeto, execute o arquivo principal:

$ python main.py

🔍 Explicação dos Blocos de Código

Importação das Bibliotecas:
As bibliotecas necessárias são importadas, incluindo dotenv para carregar variáveis de ambiente e langchain para integração com o modelo Groq.

Carregamento da API Key:
A chave de API do Groq é carregada através do arquivo .env usando dotenv.

Definição do Modelo:
O modelo ChatGroq é inicializado com a chave de API e o nome do modelo gemma2-9b-it.

Banco de Dados das Cidades:
Um dicionário é usado para armazenar informações relevantes sobre diversas cidades brasileiras.

Função de Histórico de Sessões:
A função get_session_history() gerencia o histórico de mensagens de cada usuário.

Configuração do Pipeline:
O pipeline é configurado usando RunnablePassthrough, prompt e o modelo Groq.

Função de Busca de Informações:
A função get_city_info() retorna informações sobre uma cidade com base no dicionário city_data.

Execução do Pipeline:
O pipeline é executado com um exemplo de entrada de usuário e exibe a resposta fornecida pelo modelo.