# Setup Guide for LiamBFlynn Ollama Model

This guide walks you through setting up and using the LiamBFlynn character model with Ollama.

## Prerequisites

Before you begin, ensure you have:

1. **Ollama installed**: Download from [ollama.ai](https://ollama.ai/)
2. **Git installed**: For cloning the repository
3. **Sufficient disk space**: At least 5GB free for the model

## Step-by-Step Installation

### 1. Install Ollama

#### macOS
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

#### Linux
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

#### Windows
Download the installer from [ollama.ai](https://ollama.ai/download)

### 2. Verify Ollama Installation

```bash
ollama --version
```

You should see the version number printed.

### 3. Clone the Repository

```bash
git clone https://github.com/J9ck/LiamBFlynn.git
cd LiamBFlynn
```

### 4. Create the Model

```bash
ollama create liambflynn -f modelfiles/Modelfile
```

This process will:
- Pull the base llama2-uncensored model (if not already present)
- Apply the custom system prompt and parameters
- Create the liambflynn model

**Note**: The first run may take several minutes as it downloads the base model (~4GB).

### 5. Verify the Model

```bash
ollama list
```

You should see `liambflynn` in the list of available models.

## Usage

### Basic Chat

Start a conversation:
```bash
ollama run liambflynn
```

Type your message and press Enter. Type `/bye` to exit.

### API Usage

You can also interact with the model via the Ollama API:

```bash
curl http://localhost:11434/api/generate -d '{
  "model": "liambflynn",
  "prompt": "Who are your best friends?",
  "stream": false
}'
```

### Python Usage

```python
import requests
import json

def chat_with_liam(prompt):
    response = requests.post('http://localhost:11434/api/generate',
                           json={
                               'model': 'liambflynn',
                               'prompt': prompt,
                               'stream': False
                           })
    return response.json()['response']

# Example
response = chat_with_liam("Tell me about baseball")
print(response)
```

### JavaScript/Node.js Usage

```javascript
const fetch = require('node-fetch');

async function chatWithLiam(prompt) {
  const response = await fetch('http://localhost:11434/api/generate', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      model: 'liambflynn',
      prompt: prompt,
      stream: false
    })
  });
  
  const data = await response.json();
  return data.response;
}

// Example
chatWithLiam("What's your favorite food?")
  .then(response => console.log(response));
```

## Updating the Model

If you make changes to the Modelfile:

1. Edit `modelfiles/Modelfile`
2. Recreate the model:
```bash
ollama create liambflynn -f modelfiles/Modelfile
```

The old version will be replaced with the updated one.

## Troubleshooting

### Model Not Found
If you get "model not found" errors:
```bash
ollama list  # Check if model exists
ollama create liambflynn -f modelfiles/Modelfile  # Recreate if needed
```

### Ollama Not Running
Ensure the Ollama service is running:
```bash
# Check if running
ollama list

# If not, start the service (varies by OS)
ollama serve  # Starts the Ollama server
```

### Slow Responses
- Ensure you have sufficient RAM (8GB+ recommended)
- Close other resource-intensive applications
- Consider using a smaller base model if performance is an issue

### Base Model Download Issues
If the base model fails to download:
```bash
# Manually pull the base model first
ollama pull llama2-uncensored
```

## Advanced Configuration

### Memory Settings

Edit the Modelfile to adjust memory usage:
```
PARAMETER num_ctx 2048  # Context window size
PARAMETER num_gpu 1     # GPU layers to use
```

### Temperature Settings

Adjust response creativity:
```
PARAMETER temperature 0.8  # Higher = more creative, Lower = more focused
```

### Stop Sequences

The model uses custom stop sequences defined in the Modelfile:
```
PARAMETER stop [INST]
PARAMETER stop [/INST]
PARAMETER stop <<SYS>>
PARAMETER stop <</SYS>>
```

## Web UI Integration

The `modelfiles/liam.json` file can be imported into Ollama web UIs for enhanced features:

1. Copy the contents of `modelfiles/liam.json`
2. Import into your preferred Ollama web interface
3. The model will appear with the custom icon and suggested prompts

## Next Steps

- Explore the [example conversations](../examples/conversations.md)
- Customize the Modelfile for your use case
- Build applications using the Ollama API
- Share your experience and contribute improvements

## Resources

- [Ollama Documentation](https://github.com/ollama/ollama/blob/main/docs)
- [Ollama API Reference](https://github.com/ollama/ollama/blob/main/docs/api.md)
- [Modelfile Reference](https://github.com/ollama/ollama/blob/main/docs/modelfile.md)
- [Repository Issues](https://github.com/J9ck/LiamBFlynn/issues)

## Support

If you encounter issues:
1. Check the troubleshooting section above
2. Review the Ollama documentation
3. Open an issue on GitHub with details about your problem
