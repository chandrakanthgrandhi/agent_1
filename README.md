# agent_1

## Overview

`agent_1` is a lightweight, modular AI agent framework designed to simplify the creation, orchestration, and deployment of autonomous agents. It provides a clear structure for defining agents, managing their state, and integrating with various tools and APIs.

## Features

- **Modular Architecture**: Easily plug in new capabilities, tools, and memory backends.
- **Simple Agent Definition**: Define agents with minimal boilerplate.
- **Extensible Tooling**: Add custom tools that agents can invoke during execution.
- **State Management**: Built‑in support for short‑term and long‑term memory.
- **Ready for Production**: Designed to be integrated into larger systems and workflows.

## Installation

```bash
# Clone the repository
git clone https://github.com/your-org/agent_1.git
cd agent_1

# Install dependencies (using pip and a virtual environment is recommended)
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```

> **Note**: The project currently requires Python 3.9+.

## Quick Start

Below is a minimal example showing how to create and run an agent that can perform a simple calculation.

```python
from agent_1 import Agent, Tool

# Define a simple tool
class AddTool(Tool):
    name = "add"
    description = "Adds two numbers"

    def run(self, a: float, b: float) -> float:
        return a + b

# Create the agent
my_agent = Agent(
    name="CalculatorAgent",
    role="Performs basic arithmetic operations",
    goals=["Add two numbers when asked"],
    tools=[AddTool()],
)

# Run the agent with a user prompt
result = my_agent.run("What is 7 plus 5?")
print(result)
```

## Documentation

- **API Reference**: See the `docs/` directory for detailed module‑level documentation.
- **Examples**: Additional usage examples are located in the `examples/` folder.
- **Contribution Guide**: To contribute, please read `CONTRIBUTING.md`.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Ensure all tests pass (`pytest`).
4. Open a pull request describing your changes.

## License

This project is licensed under the MIT License – see the `LICENSE` file for details.