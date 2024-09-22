## Where Does Ollama Store Models on My Mac? 

in the following location: 

```
/home/$USER/.ollama/models/
```

to run ollama use the following command based on yoru model: 

```
ollama run llama3.1
ollama run gemma2:2b
ollama run phi3
```

this will install and run the 8b llama3.1 model

to exit ollama type: 

```
/bye
```

to clear the session context type: 

```
/clear
```

for help type: 

```
/?, /help
```

to list all the installed models use the command: 

```
ollama list
```



## How Can We Move the Models to External Hard Drive? 

❖ First of All We Will Copy The `blob` and `mainfest` Folders From `/home/$USER/.ollama/models/` To the New Models Folder We Will Create on Our Hard Drive. 

❖ Now We Will Delete the Models Folder From the Home Directory 

❖ And Finally We Will Create the Symbolic Link Like This: 

```
❯ ln -s "/Volumes/Samsung T5/Ollama/models/" ~/.ollama/
```

❖ All Set! 👍 

## How to Delete a Model?

Use the Following Command: 

```
ollama rm llama3.1
```

## Best GUI App to Run the LLMS

https://github.com/AugustDev/enchanted

## How to Fix the Error Max Retries Exceeded when Pulling a Model?

Use the Following: 

```
while ! ollama run mistral; do
	echo "Command Failed.Retrying..."
	sleep 1
	done
```

the way to do it in zsh without creating sh file is to use each line and after the each line press Control ⌃ + Enter or Enter, and after done press enter. 

## Raycast Extension

https://www.raycast.com/massimiliano_pasquini/raycast-ollama

## Advanced Stuff

to show the default info about a specific model type: 

```
ollama show mistral
```

**Batch Size**: Batch size is like cooking multiple meals at once instead of one at a time. In machine learning, it's the number of examples (data points) that the model processes in one go before updating its internal understanding. A larger batch size can make training faster but might require more memory.

**Quantization**: Quantization is like compressing a high-quality image to make it smaller. In machine learning, it's a technique to reduce the size of a model by using fewer bits to represent its numbers. This makes the model smaller and often faster, but there might be a small trade-off in accuracy. It's particularly useful for running large language models on devices with limited resources.



## Github Reference

https://github.com/ollama/ollama

