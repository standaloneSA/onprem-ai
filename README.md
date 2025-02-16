# OnPrem AI 

Make sure to add the OpenAI_API_KEY and GROQ_API_KEY to .env before running 'docker compose up -d' 



## Services

- OpenWebUI: port 3000
- SearXNG: port 8090
- LiteLLM Proxy: port 4000

## Setup

OpenWebUI will launch on port 3000. Once you login and set up an account, go to the Admin Portal, then Settings, then Connections

0. Before running 'docker compose up', modify litellm-config.yaml to add or remove any models you want to be able to select 

1. Set the OpenAI connection to enabled, make the URL http://litellm:4000 with any key and no prefix

2. Disable Ollama API (we're using Ollama through the LiteLLM proxy)

3. Make sure your models are populated under Models

4. Under web search, enable Web Search, and for Web Search Engine, select "searxng", with the query url of: http://searxng:8080/search?q=<query>

