# Quolo

Quolo is a powerful integration library designed to facilitate easy and efficient interaction with multiple AI platforms like OpenAI, Anthropic, Google, and Cohere. It supports various AI features such as text generation, function calling, and embeddings.

Our long term goal is to further the integration of Quolo beyond large language models to assist with role-based access control (RBAC) at scale.

## Getting Started

### Installation

Install the package via npm:

```sh
npm install quolo
```

### Setup

Before you can use the Quolo library, you need to configure it with your API keys for the platforms you intend to use.

### Configuring API Keys

Create a `.env` file in your root directory and store your API keys:

```env
OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
GOOGLE_API_KEY=your_google_api_key
COHERE_API_KEY=your_cohere_api_key
```

Ensure your application loads these API keys into the environment variables, preferably using a library like `dovenv`.

```typescript
import 'dotenv/config';
```

### Usage

#### Text Generation

To generate text using OpenAI's GPT model:

```typescript
import { Quolo } from 'quolo';

// Create an instance of Quolo for OpenAI
const quolo = new Quolo('openai', 'your_openai_api_key');

// Use the instance to generate text
quolo.generateText("What is quantum mechanics?", "gpt-3.5-turbo")
    .then(text => console.log("Generated Text:", text))
    .catch(error => console.error("Error:", error));
```

### Supported Platforms

* OpenAI
* Anthropic
* Google
* Cohere

### Capabilities

These are the capabilities of each LLM provider:

| Feature                           | OpenAI | Anthropic | Google | Cohere |
|-----------------------------------|--------|-----------|--------|--------|
| Text Generation                   | Yes    | Yes       | Yes    | Yes    |
| Function Calling                  | Yes    | Yes       | Yes    | Yes    |
| Embeddings                        | Yes    | No        | Yes    | Yes    |
| Fine Tuning                       | Yes    | No        | Yes    | Yes    |
| Retrieval Augmented Generation    | No     | No        | Yes    | Yes    |

### Roadmap

The Quolo roadmap introduces new capabilities for each LLM provider, testing, RBAC integration, and expands support for Hugging Face and Azure platforms.

![Quolo Roadmap](https://github.com/user-attachments/assets/e9512aae-c8e6-480c-a1f6-dc9b6b7ee975)



## Credits

This project was developed with contributions from the following individuals and organizations:

- [Adaca](https://www.adaca.com)

Special thanks to the open-source community and the following projects:

- [Express](https://expressjs.com)
- [TypeScript](https://www.typescriptlang.org)
- [OpenAI](https://www.openai.com)
- [Anthropic](https://www.anthropic.com)
        
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

