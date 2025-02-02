

# Deploying and Serving Llama 2 Models on AWS SageMaker

This repository demonstrates how to deploy and serve large language models (LLMs), specifically the Llama 2 family of models from Hugging Face, on Amazon SageMaker.  It provides a complete workflow, from model deployment to inference and cleanup, utilizing Boto3 and the SageMaker Python SDK.  This setup allows you to easily scale your LLM inference and integrate it into real-world applications.  The repository includes scripts for deploying the model, invoking the deployed endpoint for inference, and cleaning up all created resources (endpoints, models, and configurations) to manage costs effectively.

## Setting Up Your Environment

Before running the code, you'll need to set up your local development environment.  We recommend using Conda to manage your Python environment and dependencies. Follow these steps:

1. **Install Conda:** If you don't have Conda installed, download and install it from [https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html).

2. **Create a Virtual Environment:** Open your terminal or command prompt and navigate to the root directory of this repository.  Then, create a new Conda environment:

   ```bash
   conda create -n llama2-sagemaker python=3.9  # Or your preferred Python version
   ```

3. **Activate the Environment:** Activate the newly created environment:

   ```bash
   conda activate llama2-sagemaker
   ```

4. **Install Requirements:** Install the required Python packages using pip:

   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` file lists all the necessary libraries, including Boto3, the SageMaker SDK, and other dependencies.  Ensure that you have the correct versions specified in this file for compatibility.

   **Note:**  If you encounter issues with specific library installations (especially those related to CUDA or GPU support), consult the documentation for those libraries for guidance on your operating system and hardware setup.  You might need to install additional system-level dependencies.

