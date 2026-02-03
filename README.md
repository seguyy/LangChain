# LangChain

This repository demonstrates how to design and implement multi-step Large Language Model (LLM) workflows using LangChain. The project focuses on the use of chains as a core abstraction for composing prompts, managing intermediate outputs, and routing tasks dynamically.

The notebook illustrates practical patterns that are commonly used in production-grade LLM systems.

## Project Overview
Modern LLM applications often require more than a single prompt. This project explores how to structure complex reasoning and text transformation pipelines using LangChain’s chaining mechanisms.

The notebook covers:

- Prompt templating and LLM configuration

- Sequential reasoning pipelines

- Explicit variable management across steps

- Dynamic routing of user inputs to specialized prompts


## Concepts Demonstrated
### LLMChain

- Defines a single prompt-to-LLM execution unit
- Uses prompt templates with input variables
- Controls model behavior through parameters such as temperature

### SimpleSequentialChain
- Passes output from one chain directly into the next
- Useful for linear transformations and multi-step generation

### SequentialChain
- Supports multiple inputs and named outputs
- Enables modular and reusable pipeline components
- Better suited for production-style workflows

### Router Chain
- Classifies inputs and routes them to appropriate downstream chains
- Demonstrates task-aware prompt routing
- Lays the foundation for scalable multi-capability LLM systems

## How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/seguyy/LangChain.git
   cd LangChain
   
2. Install dependencies
   ```bash
   pip install langchain openai jupyter
   
3. Set your OpenAI API key (macOS / Linux)
   ```bash
   export OPENAI_API_KEY="your-api-key"

4. Launch the notebook
   ```bash
   jupyter notebook Chains.ipynb
