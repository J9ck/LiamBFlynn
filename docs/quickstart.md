# Quick Start Guide

Get up and running with LiamBFlynn in 5 minutes!

## Prerequisites

- Ollama installed ([Download here](https://ollama.ai/))
- Git installed

## Quick Setup

```bash
# 1. Clone the repository
git clone https://github.com/J9ck/LiamBFlynn.git
cd LiamBFlynn

# 2. Create the model
ollama create liambflynn -f modelfiles/Modelfile

# 3. Start chatting!
ollama run liambflynn
```

## Your First Conversation

```
>>> Hey Liam, what's up?

(Liam will respond in his characteristic style)

>>> Tell me about baseball

(Liam will share his passion for the sport)

>>> Who are your best friends?

(Liam will talk about his crew)
```

Type `/bye` to exit the chat.

## What's Next?

- **Learn more**: Check out the [full documentation](setup.md)
- **See examples**: View [example conversations](../examples/conversations.md)
- **Customize**: Edit `modelfiles/Modelfile` and recreate the model
- **Contribute**: Read the [contributing guide](../CONTRIBUTING.md)

## Common Commands

```bash
# List your models
ollama list

# Chat with Liam
ollama run liambflynn

# Delete the model (if needed)
ollama rm liambflynn

# Recreate after changes
ollama create liambflynn -f modelfiles/Modelfile
```

## Troubleshooting

**Model not found?**
```bash
ollama create liambflynn -f modelfiles/Modelfile
```

**Ollama not installed?**
- Visit [ollama.ai](https://ollama.ai/) to download

**Need help?**
- Check the [setup guide](setup.md)
- Open an issue on GitHub

## Have Fun!

Enjoy chatting with LiamBFlynn! Remember, this is an AI character designed for entertainment and educational purposes. Use responsibly! 🎉⚾
