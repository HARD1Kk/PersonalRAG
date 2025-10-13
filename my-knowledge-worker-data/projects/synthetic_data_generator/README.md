# 🧠 Business Scenario → Synthetic Dataset Generator

This project provides a web-based interface built with Gradio to generate synthetic datasets based on a defined schema. It leverages large language models to create realistic and structured data for various business scenarios.

## Features

*   Generate synthetic data based on a user-defined schema.
*   Specify the number of data samples to generate.
*   Uses powerful Large Language Models (LLMs) for data creation.
*   Interactive interface powered by Gradio.
*   Supports multiple LLM providers: OpenAI, Anthropic, Google, and HuggingFace.
*   Download generated datasets in various formats (JSON, CSV, TXT, Markdown).

## Requirements

To run this project, you need to have Python 3.6+ installed, along with the following libraries:

*   bitsandbytes==0.46.0
*   gradio
*   pandas
*   numpy
*   datasets
*   torch
*   transformers
*   openai
*   huggingface_hub
*   requests
*   anthropic

You can install all the required libraries using pip:

```bash
pip install --quiet --upgrade bitsandbytes==0.46.0 gradio pandas numpy datasets torch transformers openai huggingface_hub requests anthropic
```

## Running in Google Colab (Recommended)

This project is designed to be run in Google Colab, which provides a free and convenient environment with GPU access.

1.  **Open in Colab:**

    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HARD1Kk/synthetic_data_generator/blob/main/dataset_generator.ipynb)

2.  **Set up your API keys:**

    This project requires API keys for HuggingFace, OpenAI, Anthropic, and Google. To keep your keys secure, use Colab's secrets management:

    *   In the Colab notebook, click on the **key icon** in the left sidebar to open the **Secrets** tab.
    *   Add the following secrets:
        *   `HF_TOKEN`: Your Hugging Face API token.
        *   `OPENAI_API_KEY`: Your OpenAI API key.
        *   `ANTHROPIC_API_KEY`: Your Anthropic API key.
        *   `GOOGLE_API_KEY`: Your Google API key.

3.  **Run the notebook:**

    *   Run the cells in the notebook sequentially.
    *   The Gradio interface will launch at the end, providing you with a public URL to access the application.

## Running Locally (Alternative)

While not the recommended method, you can also run this project on your local machine.


## HuggingFace, OpenAI, Anthropic and Google API Keys Setup

To use the different models, you need to provide your API keys. The notebook is configured to use Google Colab's `userdata` to access these keys. If you are running the notebook locally, you will need to modify the code to load your keys from a different source (e.g., environment variables, a configuration file).

## Models Supported

The application supports a variety of models from different providers:

*   **GPT:** `gpt-4o-mini`, `gpt-4o`, `gpt-3.5-turbo`
*   **Claude:** `claude-3-7-sonnet-latest`, `claude-3-5-haiku-latest`, `claude-3-opus-latest`
*   **Gemini:** `gemini-2.0-flash`, `gemini-1.5-pro`
*   **HuggingFace:**
    *   `meta-llama/Llama-3.1-3B-Instruct`
    *   `microsoft/bitnet-b1.58-2B-4T`
    *   `ByteDance-Seed/Seed-Coder-8B-Instruct`
    *   `tiiuae/Falcon-E-3B-Instruct`
    *   `Qwen/Qwen2.5-7B-Instruct`

## Gradio Interface

The Gradio interface allows you to:

*   **Enter the number of data samples to generate.**
*   **Select the format for the dataset** (json, csv, txt, markdown).
*   **Describe your business scenario** in a textbox.
*   **Select the model type and model name** you want to use.
*   **Enter the maximum number of output tokens** to generate.
*   **View the generated dataset** in a chatbot interface.
*   **Extract and save the dataset** to a file.

## Future Development

*   Add support for more LLM providers and models.
*   Improve the error handling and user feedback.
*   Add more options for customizing the generated data.
*   Create a standalone Python application instead of a Jupyter notebook.
