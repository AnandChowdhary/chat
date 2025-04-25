# 💬 Chat

A GitHub Actions workflow that enables chat conversations with AI models directly in GitHub Issues. This workflow uses GitHub's AI models API to provide intelligent responses to your questions and discussions.

Source:

- Workflow: [`.github/workflows/chat.yml`](./.github/workflows/chat.yml)
- System prompt: [`system-prompt.md`](./system-prompt.md)

## Features

- 🤖 Chat with all available AI models from GitHub Marketplace
- 🎤 Natural conversation flow with GitHub issue comments
- 🏷️ Model selection through issue labels

## How to use

![Screenshot of isssues](https://github.com/user-attachments/assets/0af2a80f-20ce-4a81-a5a9-e4f6d6a8ef6e)

1. **Create a new issue**

   - Open a new issue in this repository
   - Write your question or message in the issue title
   - The workflow will automatically respond using the default model (GPT-4.1)

2. **Continue the conversation**

   - Reply to the AI's response in the issue comments
   - The AI will maintain context of the entire conversation
   - Each response will be from the same AI model

3. **Change the AI model**

   - Add a label with the model ID you want to use (e.g., `openai/gpt-4o`)
   - The next response will use the selected model
   - Available models are listed as labels in the repository

4. **Update available models**
   - Comment "update labels" in any issue
   - The workflow will refresh the available model labels
   - You'll get a confirmation with the list of current models

## Available models

The workflow supports all models available in the GitHub AI catalog, including:

- `openai/gpt-4.1` (default) - Latest GPT-4 model with improved performance
- `openai/gpt-4o` - OpenAI's multimodal model
- `openai/o1` - Advanced reasoning model
- `openai/o3` - Enhanced quality and safety model
- And many more...

To see all available models, see the [repository labels](https://github.com/AnandChowdhary/chat/labels) or the [official API endpoint](https://models.github.ai/catalog/models).

## How it works

1. When you create an issue or comment, the workflow:

   - Checks for a model label
   - Uses the default model if no label is found
   - Maintains conversation history
   - Generates a response using the selected model

2. The workflow automatically:
   - Creates labels for all available models
   - Maintains consistent label styling
   - Handles errors gracefully
   - Provides helpful error messages

## License

MIT &copy; [Anand Chowdhary](https://anandchowdhary.com)
