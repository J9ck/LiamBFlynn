# LiamBFlynn - Ollama Character Model

From Roommate to LLM - A character-based AI chatbot built with Ollama.

## About

This repository contains an Ollama modelfile for creating an AI chatbot based on the personality of Liam B Flynn, a college student, baseball player, and friend. The model is designed for conversational AI and entertainment purposes.

## Prerequisites

- [Ollama](https://ollama.ai/) installed on your system
- Basic understanding of Ollama modelfiles

## Installation

1. Clone this repository:
```bash
git clone https://github.com/J9ck/LiamBFlynn.git
cd LiamBFlynn
```

2. Create the model using Ollama:
```bash
ollama create liambflynn -f modelfiles/Modelfile
```

## Usage

After creating the model, you can chat with it using:

```bash
ollama run liambflynn
```

### Example Conversations

```bash
# Start a conversation
$ ollama run liambflynn

>>> Who is Noelle?
[LiamBFlynn will respond about Noelle being his best friend...]

>>> Tell me about baseball
[LiamBFlynn will share his passion for baseball...]
```

## Repository Structure

```
LiamBFlynn/
├── modelfiles/          # Ollama modelfiles and configurations
│   ├── Modelfile        # Main Ollama modelfile
│   ├── liam.json        # JSON configuration for web UI
│   └── modelfiles-export-1710351926121.json  # Exported configuration
├── examples/            # Example conversations and use cases
├── docs/                # Additional documentation
├── update               # Update script
└── README.md           # This file
```

## Character Background

Liam Banks Flynn is portrayed as:
- College student at Nichols College, MA
- Division 3 baseball player
- Friend to Jack Doyle, Brodie Burgun, Dan Cascio, Jay Grzysicwicz, Peter Perrotta, and Sean Diaz
- Someone who values friendship, personal growth, and self-improvement
- Enjoys Chipotle and Pokémon Go
- Committed to fitness and wellness

## Customization

You can customize the model by editing the `modelfiles/Modelfile`:

1. Modify the `SYSTEM` prompt to change the personality
2. Adjust the `PARAMETER` settings for different response styles
3. Add or remove context in the "WHAT TO RETAIN" section

After making changes, recreate the model:
```bash
ollama create liambflynn -f modelfiles/Modelfile
```

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests to improve the model or documentation.

### Guidelines
- Keep the character authentic and respectful
- Test changes thoroughly before submitting
- Update documentation for any new features

## License

This project is for educational and entertainment purposes only.

## Disclaimer

This is a fictional AI character created for educational purposes. It does not represent real advice or real interactions with any actual person. Use responsibly and for entertainment only.

## Acknowledgments

- Created by J9ck
- Built with [Ollama](https://ollama.ai/)
- Based on the llama2-uncensored model
- Inspired by real friendships and experiences

## Support

For issues or questions:
- Open an issue on GitHub
- Check the [Ollama documentation](https://ollama.ai/docs)

---

**Note**: This is a character AI model designed for conversational entertainment. Always use AI responsibly and ethically.
