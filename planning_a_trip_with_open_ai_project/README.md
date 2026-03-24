# Planning a Trip with OpenAI

## Descrição do Projeto
Este projeto foi desenvolvido como parte de um desafio prático onde o objetivo é criar um guia de turismo virtual com inteligência artificial para a cidade de Paris, utilizando a API da OpenAI de forma a atuar como uma agência de turismo (Peterman Reality Tours).

O assistente fornece respostas inteligentes e contextualizadas sobre dicas de viagens, distâncias e pontos turísticos icônicos de Paris (como o Museu do Louvre, Torre Eiffel e Arco do Triunfo), auxiliando no planejamento da viagem de forma interativa.

## Tecnologias Utilizadas
- Python
- Jupyter Notebook
- API da OpenAI (modelo `gpt-4o-mini`)

## Estrutura do Projeto
- `notebook_project_planning_a_trip_with_open_ai.ipynb`: O arquivo principal do projeto, contendo todo o código Python para interagir com a API da OpenAI, configurar o papel do assistente e processar as perguntas do usuário.

## Pré-requisitos
Para executar e reproduzir este projeto, você precisará ter em sua máquina:
- [Python 3.8+](https://www.python.org/downloads/)
- [Jupyter Notebook](https://jupyter.org/install) (ou trabalhar em um ambiente como o VS Code com extensão Jupyter)
- Uma chave de API válida da [OpenAI](https://platform.openai.com/api-keys)

## Orientações para Reprodução

1. **Abra o terminal** na pasta do projeto:
   ```bash
   cd caminho/para/planning_a_trip_with_open_ai_project
   ```

2. **Crie um ambiente virtual** (opcional, mas altamente recomendado):
   ```bash
   python -m venv venv
   
   # Ativação no Windows:
   venv\Scripts\activate
   
   # Ativação no Mac/Linux:
   source venv/bin/activate
   ```

3. **Instale as bibliotecas necessárias**:
   ```bash
   pip install openai jupyter
   ```

4. **Configuração da Chave da API**:
   O código utiliza a biblioteca da OpenAI que busca automaticamente a variável de ambiente `OPENAI_API_KEY`. Configure-a no seu terminal antes de rodar o notebook.
   
   *No Windows (CMD):*
   ```cmd
   set OPENAI_API_KEY=sua_chave_aqui
   ```
   
   *No Windows (PowerShell):*
   ```powershell
   $env:OPENAI_API_KEY="sua_chave_aqui"
   ```
   
   *No Mac/Linux:*
   ```bash
   export OPENAI_API_KEY="sua_chave_aqui"
   ```
   *(Alternativamente, você pode criar um arquivo `.env` e usar a biblioteca `python-dotenv` dentro do notebook para carregar a chave, adicionando `load_dotenv()` no início do código).*

5. **Inicie o Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

6. **Execução**:
   No navegador, abra o arquivo `notebook_project_planning_a_trip_with_open_ai.ipynb`. Execute as células em ordem. A última célula irá processar as perguntas pré-definidas através de um loop, manter o histórico da conversa vivo no array de mensagens e imprimir as respostas detalhadas dadas pela IA sobre Paris.

## Como Personalizar
Se quiser usar o assistente para outras cidades ou outras dinâmicas, basta alterar o conteúdo (o prompt do sistema) da variável `conversation` na primeira interação para refletir o novo comportamento desejado e mudar as perguntas na lista `questions`.
