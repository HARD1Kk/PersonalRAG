# AI Code Commenter 

A professional AI-powered tool that automatically adds comprehensive comments to your code using multiple AI models including GPT, Claude, Gemini, and Perplexity.

## Features

- 🤖 **Multiple AI Models**: Support for GPT, Claude, Gemini, and Perplexity
- 🌐 **20+ Programming Languages**: C++, Python, JavaScript, Java, and more
- 💼 **Professional Styling**: Clean, modern interface with dark theme
- 📝 **Smart Commenting**: Context-aware, professional-quality comments
- 🔄 **Real-time Processing**: Stream results as they're generated
- 📋 **Easy Copy**: One-click copy functionality for generated code

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/HARD1Kk/AI_code_commenter.git
   cd AI_code_commenter
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   Create a `.env` file in the project root and add your API keys:
   ```env
   OPENAI_API_KEY=your_openai_key_here
   ANTHROPIC_API_KEY=your_anthropic_key_here
   GEMINI_API_KEY=your_gemini_key_here
   PERPLEXITY_API_KEY=your_perplexity_key_here
   ```

## Usage

### Run the Jupyter Notebook
```bash
jupyter notebook code_generator.ipynb
```

Then run all cells in the notebook to launch the application.

## API Keys Required

- **OpenAI API Key**: For GPT model access
- **Anthropic API Key**: For Claude model access
- **Google API Key**: For Gemini model access
- **Perplexity API Key**: For Perplexity model access

Get your API keys from:
- [OpenAI](https://platform.openai.com/api-keys)
- [Anthropic](https://console.anthropic.com/)
- [Google AI Studio](https://makersuite.google.com/app/apikey)
- [Perplexity](https://www.perplexity.ai/settings/api)

## Supported Languages

- C/C++
- Python
- JavaScript/TypeScript
- Java
- C#
- Go
- Rust
- Swift
- Kotlin
- PHP
- Ruby
- And many more...

## Project Structure

```
AI_code_commenter/
├── code_generator.ipynb    # Main Jupyter notebook
├── requirements.txt        # Python dependencies
├── env.example            # Environment variables template
├── .gitignore             # Git ignore rules
└── README.md              # This file
```

## Contributingu

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

If you encounter any issues or have questions, please open an issue on GitHub.
