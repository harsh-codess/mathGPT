# MathsGPT - Text to Math Problem Solver

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Try_Now-blue?style=for-the-badge)](https://mathgpt-harshcodess.streamlit.app/)

> **🌐 [Try the Live Demo Here!](https://mathgpt-harshcodess.streamlit.app/)**

A powerful AI-powered Streamlit application that solves mathematical problems and provides data search capabilities using Google Gemma 2 model via Groq API.

## 🌟 Features

- **Mathematical Problem Solving**: Solves complex math problems with step-by-step explanations
- **Wikipedia Integration**: Searches for relevant information to provide context
- **Reasoning Engine**: Logic-based problem solving with detailed explanations
- **Interactive Chat Interface**: User-friendly chat-based interaction
- **Real-time Processing**: Instant responses with streaming callbacks
- **Multi-tool Agent**: Combines calculator, Wikipedia search, and reasoning tools

## 🚀 Live Demo

**[🌐 Access the Live Application](https://mathgpt-harshcodess.streamlit.app/)**

The application is deployed and ready to use! Simply visit the link above to:
- Input mathematical word problems
- Get step-by-step solutions
- Access Wikipedia information for context
- Receive detailed explanations in a conversational format

*Note: You'll need to provide your own Groq API key when using the live demo.*

## 📋 Prerequisites

- Python 3.8 or higher
- Groq API key (free tier available)
- Internet connection for Wikipedia searches

## 🛠️ Installation

1. **Clone the repository:**
```bash
git clone https://github.com/harsh-codess/MathsGPT.git
cd MathsGPT
```

2. **Create a virtual environment:**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install required dependencies:**
```bash
pip install streamlit langchain-groq langchain langchain-community wikipedia
```

4. **Set up your Groq API key:**
   - Visit [Groq Console](https://console.groq.com/)
   - Sign up for a free account
   - Generate an API key
   - Keep it ready for the application

## 🏃‍♂️ Running the Application

1. **Start the Streamlit app:**
```bash
streamlit run app.py
```

2. **Open your browser** and navigate to `http://localhost:8501`

3. **Enter your Groq API key** in the sidebar

4. **Start solving math problems!**

## 💡 Usage Examples

### Example 1: Word Problem
**Input:**
```
I have 5 bananas and 7 grapes. I eat 2 bananas and give away 3 grapes. 
Then I buy a dozen apples and 2 packs of blueberries. Each pack of 
blueberries contains 25 berries. How many total pieces of fruit do I have?
```

**Output:** Step-by-step calculation with reasoning

### Example 2: Mathematical Calculation  
**Input:**
```
Calculate the area of a circle with radius 7.5 cm
```

**Output:** Formula explanation and numerical result

### Example 3: Complex Problem
**Input:**
```
A train travels 120 km in 2 hours. If it increases its speed by 20 km/h, 
how long will it take to travel 200 km?
```

**Output:** Detailed solution with speed calculations

## 🔧 Technical Architecture

### Core Components

1. **Language Model**: Google Gemma 2-9B-IT via Groq API
2. **Agent Framework**: LangChain with ZERO_SHOT_REACT_DESCRIPTION
3. **Tools Integration**:
   - Calculator tool for mathematical computations
   - Wikipedia tool for information retrieval
   - Reasoning tool for logical problem solving

### Application Flow

```
User Input → Agent Decision → Tool Selection → Processing → Response
```

## 📁 Project Structure

```
MathsGPT/
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
├── .env               # Environment variables (not tracked)
├── .gitignore         # Git ignore rules
└── README.md          # Project documentation
```

## 🔑 API Keys Setup

### Groq API Key
1. Visit [Groq Console](https://console.groq.com/)
2. Create an account (free tier available)
3. Navigate to API Keys section
4. Generate a new API key
5. Copy and paste into the Streamlit sidebar

**Note:** Keep your API keys secure and never share them publicly.

## 🎯 Supported Problem Types

- **Arithmetic**: Basic calculations, percentages, ratios
- **Algebra**: Equation solving, polynomial operations
- **Geometry**: Area, perimeter, volume calculations
- **Word Problems**: Real-world mathematical scenarios
- **Statistics**: Basic statistical calculations
- **Logic Problems**: Step-by-step reasoning

## 🔧 Customization

### Adding New Tools
```python
# Example: Adding a new tool
custom_tool = Tool(
    name="Custom Tool",
    func=your_function,
    description="Description of what the tool does"
)

# Add to agent initialization
assistant_agent = initialize_agent(
    tools=[wikipedia_tool, calculator, reasoning_tool, custom_tool],
    llm=llm,
    agent=AgentType.ZERO_SHOT_REACT_DESCRIPTION
)
```

### Modifying the Prompt
Edit the `prompt` variable in `app.py` to customize the agent's behavior:
```python
prompt = """
Your custom prompt here...
Question: {question}
Answer:
"""
```

## 🐛 Troubleshooting

### Common Issues

1. **API Key Error**
   - Ensure your Groq API key is valid
   - Check if you have sufficient API credits

2. **Import Errors**
   - Install all required packages: `pip install -r requirements.txt`
   - Ensure you're using the correct Python version

3. **Streamlit Issues**
   - Clear cache: `streamlit cache clear`
   - Restart the application

4. **Wikipedia Search Failures**
   - Check internet connection
   - Some queries might not return results

### Performance Tips

- Use specific mathematical terms for better results
- Break down complex problems into smaller parts
- Provide clear context for word problems

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 Requirements

Create a `requirements.txt` file with:
```txt
streamlit>=1.28.0
langchain>=0.1.0
langchain-groq>=0.1.0
langchain-community>=0.0.20
wikipedia>=1.4.0
```

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Groq** for providing fast AI inference
- **Google** for the Gemma 2 model
- **LangChain** for the agent framework
- **Streamlit** for the web application framework
- **Wikipedia** for knowledge base integration

## 📞 Support

For support and questions:
- Open an issue on GitHub
- Check existing issues for solutions
- Review the troubleshooting section

## 🔄 Version History

- **v1.0.0**: Initial release with basic math solving capabilities
- Features: Calculator, Wikipedia search, reasoning engine
- Streamlit interface with chat functionality

---

**Happy Problem Solving! 🧮✨**