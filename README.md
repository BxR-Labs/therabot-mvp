# Mental Health Support Bot MVP

A supportive mental health chatbot for youth built with Streamlit and OpenAI's GPT-4o-mini.

## Features

- 🧠 Empathetic conversational AI for mental wellness support
- 🛡️ Content moderation for user safety
- 📏 Response guardrails (50 words max, follow-up questions)
- ⚡ Rate limiting (20 requests/hour per IP)
- 🔒 Secure API key management
- 🚀 Streamlit Community Cloud deployment ready

## Quick Start

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/yourusername/mental-health-bot-mvp.git
cd mental-health-bot-mvp
```

2. Create virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip3 install -r requirements.txt
```

4. Set up secrets:
```bash
cp .streamlit/secrets.toml.example .streamlit/secrets.toml
# Edit .streamlit/secrets.toml and add your OpenAI API key
```

5. Run the app:
```bash
streamlit run app.py
```

### Testing

Run unit tests:
```bash
pytest tests/ -v
```

Run linting:
```bash
black .
isort .
flake8 .
```

## Deployment

### Streamlit Community Cloud

1. Fork this repository
2. Sign in to [share.streamlit.io](https://share.streamlit.io)
3. Deploy from your GitHub repository
4. Add your OpenAI API key in the Streamlit secrets management

### Environment Variables

Required secrets:
- `OPENAI_API_KEY`: Your OpenAI API key

## Project Structure

```
├── app.py                    # Main Streamlit application
├── system_prompt.txt         # AI system prompt configuration
├── guardrails.py            # Response validation and regeneration
├── moderation.py            # Content moderation wrapper
├── requirements.txt         # Python dependencies
├── tests/                   # Unit tests
├── .streamlit/              # Streamlit configuration
└── .github/workflows/       # CI/CD pipeline
```

## Important Notes

- **Non-Clinical Tool**: This is NOT a replacement for professional mental health services
- **System Prompt**: Replace the placeholder in `system_prompt.txt` with actual content before production deployment
- **Rate Limiting**: Currently uses in-memory storage; consider Redis for production
- **Safety**: Always displays crisis resources and disclaimers

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## License

This project is for educational purposes. Please ensure compliance with healthcare regulations in your jurisdiction before deploying.