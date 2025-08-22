# CrewAI Blog Generator

A collaborative AI content creation system using the CrewAI framework with Groq API integration. This project generates high-quality blog posts through a three-agent workflow: Content Planner, Writer, and Editor.

---

## Features

- **Multi-Agent Collaboration**: Three specialized AI agents working sequentially
- **Token Management**: Built-in limits to prevent API token exhaustion
- **Rate Limiting**: Automatic delays to avoid API rate limits
- **Error Recovery**: Automatic retry mechanism for failed requests
- **Groq API Integration**: Fast inference with multiple model support
- **Markdown Output**: Ready-to-publish blog posts in markdown format

---

## Prerequisites

- Python 3.8+
- Groq API key
- Required Python packages (see Installation)

---

## Installation

1. Clone or download the project files

2. Install required packages:
    ```bash
    pip install crewai python-dotenv groq
    ```

3. Create a `.env` file in the project root:
    ```
    GROQ_API_KEY=your_groq_api_key_here
    GROQ_MODEL=openai/gpt-oss-120b
    ```

---

## Supported Models

- `openai/gpt-oss-120b` (recommended)
- `llama-3.1-8b-instant`
- `mixtral-8x7b-32768`
- `gemma-7b-it`
- `qwen2-72b-instruct`

---

## Usage

1. Set your desired topic in the code:
    ```python
    result = crew.kickoff(inputs={"topic": "Your Topic Here"})
    ```

2. Run the script:
    ```bash
    python your_script_name.ipynb
    ```

3. The system will generate a complete blog post through three stages:
    - **Planning**: Research and outline creation
    - **Writing**: Full blog post composition
    - **Editing**: Final review and polish

---

## System Architecture

### Agents

**Content Planner**
- Researches latest trends and key players
- Identifies target audience
- Creates detailed content outline
- Provides SEO keywords and sources

**Content Writer**
- Crafts compelling blog posts based on planner's work
- Incorporates SEO keywords naturally
- Structures content with engaging sections
- Maintains factual accuracy and balanced viewpoints

**Editor**
- Reviews and polishes the written content
- Ensures journalistic best practices
- Aligns content with brand voice
- Avoids controversial topics

### Workflow

```
Input Topic → Planner → Content Plan → Writer → Blog Post → Editor → Final Output
```

---

## Configuration

### Token Limits
- **Max Tokens per Request**: 400 (configurable)
- **Plan Output**: Under 250 words
- **Final Blog Post**: Under 600 words
- **Paragraphs per Section**: 1-2 paragraphs

### API Settings
- **Temperature**: 0.7 (creativity vs consistency balance)
- **Timeout**: 60 seconds
- **Max Retries**: 3 attempts
- **Rate Limiting**: 2-second delay between requests

---

## Error Handling

- **Token Limit Errors**: Automatic retry after 30-second delay
- **Rate Limit Errors**: Exponential backoff strategy
- **API Timeout**: Configurable timeout with retry logic
- **Connection Issues**: Graceful error messages

---

## Output Format

Generated blog posts include:
- Engaging title and introduction
- Well-structured body sections with subheadings
- Balanced viewpoints and factual information
- SEO-optimized content
- Professional conclusion
- Markdown formatting ready for publication

---

## Customization

### Changing Topics
Modify the topic in the `crew.kickoff()` call:
```python
result = crew.kickoff(inputs={"topic": "Machine Learning"})
```

### Adjusting Output Length
Modify the `expected_output` parameters in task definitions to change word limits.

### Model Selection
Change the `GROQ_MODEL` in your `.env` file to use different models.

---

## Troubleshooting

### Common Issues

**"Token limit exceeded"**
- The system automatically handles this with retries
- Consider reducing `max_tokens` if persistent

**"Rate limit reached"**
- Built-in delays should prevent this
- Increase `time.sleep()` values if needed

**"API key not found"**
- Ensure `.env` file is in the correct location
- Verify `GROQ_API_KEY` is set correctly



---

## Performance Tips

1. **Model Selection**: Use `openai/gpt-oss-120b` for faster generation
2. **Token Optimization**: Keep agent backstories concise
3. **Caching**: The system automatically caches responses
4. **Batch Processing**: Process multiple topics in separate script runs

---

## API Costs

- Monitor your usage through the Groq console
- Adjust `max_tokens` to control costs
- Use smaller models for development/testing

---

## Contributing

To improve this system:
1. Test with different model combinations
2. Experiment with agent backstories
3. Adjust token limits for your use case
4. Add additional agents for specialized tasks

---

## License

This project is for educational and development purposes. Please ensure compliance with Groq's terms of service and API usage policies.

---

## Support

- **CrewAI Framework**: [CrewAI Documentation](https://docs.crewai.com/)
- **Groq API**: [Groq Documentation](https://console.groq.com/docs)
- **Code Issues**: Review error messages and adjust