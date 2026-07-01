# Aira v1 7B - Custom Trained AI Model

A custom-trained 7B parameter language model optimized for general-purpose AI tasks. This model has been fine-tuned using Ollama and is ready for deployment in various AI applications.

## Model Overview

- **Model Name**: Aira v1 7B
- **Parameters**: 7 Billion
- **Architecture**: Transformer-based
- **Training Framework**: Ollama
- **License**: MIT License

## Features

- Optimized for conversational AI tasks
- Enhanced reasoning capabilities
- Efficient inference with Ollama
- Suitable for various NLP applications including:
  - Text generation
  - Question answering
  - Code generation
  - Summarization
  - Translation

## Installation

### Prerequisites

- Ollama installed on your system
- At least 16GB RAM for inference
- 15GB disk space for model files

### Installation Steps

1. **Clone this repository**
   ```bash
   git clone https://github.com/yourusername/aira-v1-7b-model.git
   cd aira-v1-7b-model
   ```

2. **Build the model with Ollama**
   ```bash
   ollama create aira-v1-7b -f Modelfile
   ```

3. **Run the model**
   ```bash
   ollama run aira-v1-7b
   ```

## Usage

### Basic Usage

```bash
# Start an interactive session
ollama run aira-v1-7b

# Generate text
echo "Write a short story about AI" | ollama run aira-v1-7b
```

### API Usage

```bash
# Start Ollama server
ollama serve

# Make API requests
curl http://localhost:11434/api/generate -d '{
  "model": "aira-v1-7b",
  "prompt": "Explain quantum computing"
}'
```

### Python Integration

```python
import requests

response = requests.post('http://localhost:11434/api/generate', json={
    'model': 'aira-v1-7b',
    'prompt': 'What is machine learning?'
})
print(response.json()['response'])
```

## Model Training Process

See the [TRAINING_FLOWCHART.md](TRAINING_FLOWCHART.md) for a detailed visual guide on how this model was created and how to add it to Ollama.

## Performance

- **Inference Speed**: ~30 tokens/second on modern GPU
- **Memory Usage**: ~8GB VRAM
- **Context Window**: 4096 tokens

## Limitations

- Model may produce inaccurate or biased information
- Not suitable for critical decision-making without human oversight
- Performance depends on hardware specifications

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built using Ollama framework
- Based on transformer architecture
- Fine-tuned for enhanced performance

## Support

For issues and questions, please open an issue on GitHub.
