# Local LLM Tutorial (Basic)

A simple, containerized local LLM setup using Ollama and Docker Compose.

## Features

- **Fully containerized Ollama LLM server**
- **Automated model (Llama 3) download on startup**
- **Easy-to-use API at `http://localhost:11434`**

## Quick Start

1. **Install Docker and Docker Compose**
   - [Install Docker Desktop for Mac](https://docs.docker.com/desktop/install/mac-install/)
   - [Install Docker Engine and Compose for Linux](https://docs.docker.com/engine/install/)
   - [Install Docker Desktop for Windows](https://docs.docker.com/desktop/install/windows-install/)

2. **Clone this repository**
   ```
   git clone https://github.com/your-username/local-llm-tutorial-basic.git
   cd local-llm-tutorial-basic
   ```

3. **Make the startup script executable**
   ```
   chmod +x startup.sh
   ```

4. **Launch the stack and pull the model**
   ```
   ./startup.sh
   ```

5. **Interact with the LLM**
   - **Chat with the model interactively:**
     ```
     docker compose exec ollama ollama run llama3
     ```
   - **Use the API:**
     ```
     curl http://localhost:11434/api/generate -d '{"model":"llama3","prompt":"Why is the sky blue?"}'
     ```

## Project Structure

```
local-llm-tutorial-basic/
├── docker-compose.yml
├── README.md
└── startup.sh
```

## Resources

- **Ollama Documentation:** [https://ollama.com](https://ollama.com)
- **Docker Documentation:** [https://docs.docker.com](https://docs.docker.com)
- **Docker Compose Documentation:** [https://docs.docker.com/compose/](https://docs.docker.com/compose/)

---

Feel free to open an issue or submit a pull request if you have suggestions!
