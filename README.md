# LightRAG-Implementation-AzureOpenAI
Implementing LightRAG (Simple and Fast Retrieval-Augmented Generation) using Azure OpenAI 

## Pre-requirements:
We will be using `https://github.com/HKUDS/LightRAG` repository, We will clone and execute.

### Steps:

1. **Open VSCode > Terminal (command prompt) and continue the below commands:**

    ```sh
    # Clone the Repository
    git clone https://github.com/HKUDS/LightRAG.git

    #Create Virtual Environment
    conda create -n LightRAG python=3.10

    #
    
    # Change Directory to LightRAG
    cd LightRAG
    
    # Install from source (Recommend)
    pip install -e .

    #--------OR--------

    # Install from PyPI
    pip install lightrag-hku
    ```
2. **Adding the text file**
    - Now need to add the `.txt` file of your own OR Download the demo text "A Christmas Carol by Charles Dickens":
    ```sh
    curl https://raw.githubusercontent.com/gusye1234/nano-graphrag/main/tests/mock_data.txt > ./book.txt
    ```
3. **Creating the Deployments of LLM Model and Embedding Model in Azure OpenAI:**

    - For embedding, the model is `text-embedding-3-small`
    - For LLM model, recommended is `GPT-4o`.
    

4. **Configure AZURE_OPENAI_API_KEY:**

    After creating the deployments, you need to add these to `.env` file or add secret key if using colab.
   - AZURE_OPENAI_API_VERSION = your_api_version
   - AZURE_OPENAI_DEPLOYMENT = your_deployment_name
   - AZURE_OPENAI_API_KEY = your_api_key
   - AZURE_OPENAI_ENDPOINT = your_endpoint
   - AZURE_EMBEDDING_DEPLOYMENT = your_deployment_name
   - AZURE_EMBEDDING_API_VERSION = your_api_version

5. **Implement the LightRAG and Set AzureOpen AI Code**
   - Use the code from if using colab `lightRAG.ipynb`
   - Use the code from `lightrag_azure_openai_demo.py`
