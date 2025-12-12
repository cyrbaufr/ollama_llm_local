# ollama_llm_local

This repo was created to test local versions on LLM running with a CPU using ollama

## Linux installation process
In a terminal, run the following command: "curl -fsSL https://ollama.com/install.sh | sh"
This will install Ollama on the PC

## Run a model locally
Type "ollama run" + name of the model
e.g. ollama run llama3.2:1b
Test can be performed in a terminal using command lines:  

```python 
curl http://127.0.0.1:11434/api/generate -d '{
  "model": "llama3.2:1b",
  "prompt":"Why is the sky blue?"
}'
``` 

To avoid individual tokens generation:  

```python
curl http://127.0.0.1:11434/api/generate -d '{
  "model": "llama3.2:1b",
  "prompt":"Create a python function to add two integers?", 
  "stream": false
}'
```
