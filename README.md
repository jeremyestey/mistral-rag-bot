# Mistral RAG Bot

A Retrieval-Augmented Generation (RAG) chatbot built with Flask and Mistral AI.

Originally created by [Halim Madi](https://www.halimmadi.com) as a sample project designed for students, workshops, and educational purposes.

## 🎯 Purpose

This project demonstrates how to build a simple but effective RAG system using:
- **Flask** for the web framework
- **Mistral AI** for language generation
- **Text-based knowledge base** for document retrieval

Perfect for learning RAG concepts, educational workshops, and as a foundation for more complex implementations.

## 🚀 Features

- Simple Flask web interface
- Mistral AI integration for intelligent responses
- Text file ingestion for knowledge base
- Real-time chat functionality
- Easy deployment to Vercel
- Educational code structure for learning

## 📋 Prerequisites

- Python 3.7+
- Mistral AI API key
- Basic knowledge of Flask and Python

## 🔧 Quick Setup

### 1. Clone the Repository
```bash
git clone https://github.com/jeremyestey/mistral-rag-bot.git
cd mistral-rag-bot
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Environment Configuration
Create a `.env` file in the project root:
```env
MISTRAL_API_KEY=your_api_key_here
```

### 5. Add Your Content
Add your text file as `essay.txt` in the project root directory. This will serve as your knowledge base.

### 6. Run the Application
```bash
python app.py
```

The application will be available at `http://localhost:5001`

## 📁 Project Structure

```
mistral-rag-bot/
├── app.py                 # Main Flask application
├── requirements.txt       # Python dependencies
├── .env                  # Environment variables (create this)
├── essay.txt            # Source text for RAG system
├── vercel.json          # Vercel deployment configuration
├── templates/           # HTML templates
└── static/             # Static files (CSS, JS)
```

## 🌐 Deployment to Vercel

### Step 1: Prepare Your Repository
- Push your code to GitHub
- Ensure your `.env` file is not committed (it should be in `.gitignore`)

### Step 2: Connect to Vercel
- Connect your GitHub repository to Vercel
- Import the project

### Step 3: Configure Environment Variables
In the Vercel dashboard, add:
- `MISTRAL_API_KEY`: Your Mistral AI API key

### Step 4: Deploy
Click deploy and your bot will be live!

## 🛠️ How It Works

1. **Document Processing**: The system reads your `essay.txt` file and processes it for retrieval
2. **User Query**: When a user asks a question through the web interface
3. **Retrieval**: The system finds relevant passages from your text
4. **Generation**: Mistral AI generates a response based on the retrieved context
5. **Response**: The answer is displayed in the chat interface

## 🎓 Educational Use

This project is perfect for:
- **Learning RAG concepts**: Understand how retrieval-augmented generation works
- **Workshop demonstrations**: Simple enough to explain in workshops
- **Student projects**: Great starting point for more complex implementations
- **Prototyping**: Quick way to test RAG with your own documents

## 🔧 Customization Ideas

### Different Document Types
Replace `essay.txt` with your own content:
- Research papers
- Documentation
- FAQ content
- Product manuals

### Enhanced Features You Could Add
- Multiple document support
- PDF file processing
- User authentication
- Conversation history
- Better UI/UX
- Vector database integration

### Code Modifications
The simple structure makes it easy to:
- Add new routes
- Modify the chat interface
- Implement different retrieval strategies
- Experiment with different Mistral models

## 🐛 Troubleshooting

### Common Issues

**API Key Errors**
- Ensure your Mistral API key is correctly set in `.env`
- Check that the API key has proper permissions

**File Not Found**
- Make sure `essay.txt` exists in the project root
- Verify the file has content and is readable

**Port Issues**
- The app runs on port 5001 by default
- Change the port in `app.py` if needed

**Deployment Issues**
- Ensure environment variables are set in Vercel
- Check the Vercel build logs for errors

## 🤝 Contributing

This is an educational project, and contributions are welcome! Ideas for improvements:

- Better error handling
- Support for multiple file formats
- Enhanced UI design
- Additional deployment options
- More robust text processing
- Performance optimizations

## 📚 Learning Resources

To better understand this project, learn about:
- **Flask**: Web framework basics
- **RAG Systems**: Retrieval-augmented generation concepts
- **Mistral AI**: API usage and capabilities
- **Text Processing**: Document chunking and retrieval strategies

## 📄 License

This project is provided as a learning resource. You are free to:
- Use this code for educational purposes
- Modify and adapt it for your own projects
- Share it with others for learning
- Use it in workshops and tutorials

## 🙏 Acknowledgments

- Original creator: [Halim Madi](https://www.halimmadi.com) - [Instagram: @yalla_halim](https://www.instagram.com/yalla_halim/)
- [Mistral AI](https://mistral.ai/) for the language model API
- [Flask](https://flask.palletsprojects.com/) for the web framework
- [Vercel](https://vercel.com/) for easy deployment

## 📞 Support

For questions about this educational project:
- Create an issue in this repository
- Visit [Halim Madi's website](https://www.halimmadi.com) for more resources
- Check the original creator's other educational content

---

**Perfect for learning RAG concepts and building your first intelligent chatbot! 🤖**
