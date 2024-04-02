# How to run locally

### Create a `.env` file in the root folder. Add the variables listed below. Populate the values by going to the `environment variables` section of the `spur-chatbot-test` resource in Azure.

#### Variables for .env file:
```
# Chat
DEBUG=True
AZURE_OPENAI_RESOURCE=
AZURE_OPENAI_MODEL=
AZURE_OPENAI_KEY=
AZURE_OPENAI_MODEL_NAME=gpt-35-turbo-16k
AZURE_OPENAI_TEMPERATURE=0
AZURE_OPENAI_TOP_P=1.0
AZURE_OPENAI_MAX_TOKENS=1000
AZURE_OPENAI_SYSTEM_MESSAGE=You are an AI assistant that helps people find information.
AZURE_OPENAI_PREVIEW_API_VERSION=2024-02-15-preview
AZURE_OPENAI_STREAM=True
AZURE_OPENAI_ENDPOINT=
# User Interface
UI_TITLE=
UI_LOGO=
UI_CHAT_DESCRIPTION=
UI_FAVICON=
# Chat history
AZURE_COSMOSDB_ACCOUNT=
AZURE_COSMOSDB_DATABASE=
AZURE_COSMOSDB_CONVERSATIONS_CONTAINER=
AZURE_COSMOSDB_ACCOUNT_KEY=
# Chat with data: common settings
SEARCH_TOP_K=5
SEARCH_STRICTNESS=3
SEARCH_ENABLE_IN_DOMAIN=True
# Chat with data: Azure AI Search
AZURE_SEARCH_SERVICE=
AZURE_SEARCH_INDEX=
AZURE_SEARCH_KEY=
AZURE_SEARCH_SEMANTIC_SEARCH_CONFIG=default
AZURE_SEARCH_INDEX_IS_PRECHUNKED=False
AZURE_SEARCH_TOP_K=20
AZURE_SEARCH_ENABLE_IN_DOMAIN=False
AZURE_SEARCH_QUERY_TYPE=simple
AZURE_SEARCH_STRICTNESS=3
```

### From the root folder run:
`./start.cmd`


### Troubleshooting

- If you see an error similar to the error below run `'npm i --save-dev @types/react-syntax-highlighter` from the `frontend` folder:
```
src/components/Answer/Answer.tsx:15:42 - error TS7016: Could not find a declaration file for module 'react-syntax-highlighter'.
```

- Python 3 is required to build and run the project.