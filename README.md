# Chatbot com LangChain e Groq

Este repositório contém um chatbot desenvolvido com LangChain e a API da Groq, capaz de analisar sites, PDFs, vídeos do YouTube e planilhas Excel, além de permitir interações diretas com o usuário.

## Instalação

Este código foi projetado para ser executado no Google Colab. Antes de rodá-lo, instale as dependências necessárias:

```bash
!pip install langchain==0.3.0
!pip install langchain.groq==0.2.0
!pip install langchain-community==0.3.0
!pip install youtube-transcript-api==0.6.2
!pip install pypdf==5.0.0
!pip install pandas
!pip install numpy==1.23.5
```

## Como usar

1. Clone o repositório ou copie o código para o Google Colab.
2. Insira sua chave de API da Groq na variável `api_key`.
3. Execute o código e siga as instruções no terminal.
4. Escolha entre as opções disponíveis:
   - **1**: Analisar um site
   - **2**: Analisar um PDF
   - **3**: Analisar um vídeo do YouTube
   - **4**: Analisar uma planilha Excel
   - **5**: Conversar com o chatbot
   - **x**: Finalizar o chatbot

## Funcionalidades

- **Análise de diferentes fontes de dados**: O chatbot pode extrair e processar informações de sites, PDFs, vídeos do YouTube (legendas) e planilhas Excel.
- **Interação dinâmica**: O usuário pode fazer perguntas diretamente ao chatbot.
- **Integração com Groq**: O modelo de IA é baseado no `llama-3.3-70b-versatile`.

## Estrutura do Código

- **Carga de documentos**:
  - `carrega_site()`: Obtém o conteúdo textual de um site.
  - `carrega_pdf()`: Extrai o texto de um arquivo PDF.
  - `carrega_youtube()`: Obtém as legendas de um vídeo do YouTube.
  - `carrega_planilha()`: Converte os dados de uma planilha Excel em texto.
- **Chatbot**:
  - `respostas_bot_chat()`: Gera respostas sem contexto adicional.
  - `respostas_bot()`: Gera respostas baseadas em um documento fornecido.
  - `iniciar_chat_simples()`: Permite conversas diretas.
  - `iniciar_chat_com_atribuicoes()`: Responde com base nos documentos analisados.

## Observações

- Certifique-se de que a chave de API da Groq esteja configurada corretamente.
- O código foi desenvolvido para ser usado no Google Colab, mas pode ser adaptado para rodar localmente com pequenas modificações.

## Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para usá-lo e modificá-lo!

