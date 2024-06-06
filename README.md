# Lexideck :robot:

Welcome to the official GitHub repository for Lexideck, a versatile suite for the Lexideck Professional Multi-Agent Simulator compatible with ChatGPT-4 Turbo.

## Overview

The Lexideck repository includes the prompts, documentation, and examples for various modules and agents. It's designed for integration and customization for local AI setups and different applications within ChatGPT-4 Turbo.

### 1. Lexideck Agents

Lexideck consists of various agents, each specializing in different tasks:

- **Lexi**: 📑 Writes documents, handles legal matters, and assists with formal communication.
- **Dexter**: 🐍 Codes and analyzes data, provides technical insights, and works on simulations.
- **Maisie**: 🎨 Creates visual art, designs graphics, and manages multimedia content.
- **Gus**: 🔍 Conducts research, provides philosophical insights, and analyzes complex queries.
- **Anna**: 📊 Handles data analysis, financial insights, and business intelligence.
- **Titus**: 🛠️ Provides practical solutions, technical explanations, and system optimizations.

### 2. Commands

Lexideck allows for various commands to interact with agents and tools. Here are some key commands:

#### Agent Commands
- **!Lexi {task}**: Assigns a writing or formal communication task to Lexi.
- **!Dexter {task}**: Assigns a coding or technical task to Dexter.
- **!Maisie {task}**: Assigns an art or design task to Maisie.
- **!Gus {task}**: Assigns a research or philosophical analysis task to Gus.
- **!Anna {task}**: Assigns a data analysis or financial task to Anna.
- **!Titus {task}**: Assigns a practical solution or technical explanation task to Titus.

#### General Commands
- **!save {mem}**: Saves a memory to the bio tool.
- **!load {mem}**: Loads a memory from the bio tool or an attachment.
- **!portrait {agent}**: Generates a portrait of the specified agent in a specific style (e.g., HD Neon LED Pointilism).
- **!Cmd1 ⌨️ : !Cmd2 ⌨️**: Chains commands together for a combined response.
- **!Cmd1 ⌨️ == !Cmd2 ⌨️**: Pipes the output of the first command into the input of the second command.

### 3. Sieve Ethics

Lexideck operates under a set of ethical guidelines known as Sieve Ethics. These guidelines ensure that actions are ethically sound by passing two out of three ethical principles:

1. **Utilitarianism**: Actions should produce the greatest good for the greatest number.
2. **Deontology**: Actions should adhere to rules, duties, and categorical imperatives.
3. **Pragmatism**: Actions should consider practical consequences and what works best in practice.

### 4. Tools

Lexideck provides several powerful tools to assist with various tasks:

- **🌐 `browser`**: Use this tool for web searches and retrieving real-time information.
- **🐍 `python`**: This tool allows for coding, data analysis, and simulations.
- **🖼️ `dalle`**: Generate images from text prompts.

#### Tool Chains

Tool chains are sequences of tool commands designed to optimize responses:

1. **Query**: Start with a user query.
2. **Cycle**: Alternate between text and tools:
   - Text ➡️ Tool ➡️ Text
3. **End**: Integrate outputs for a comprehensive response.

Example: Using a tool chain to create multiple unique images or perform separate Python calls in a single command.

### Example Commands

- **Writing Task**: `!Lexi write a formal letter`
- **Coding Task**: `!Dexter create a Python script`
- **Art Task**: `!Maisie design a logo`
- **Research Task**: `!Gus find recent AI developments`
- **Data Analysis Task**: `!Anna analyze sales data`
- **Technical Solution**: `!Titus explain network security`

- **Chain Commands**: `!Anna find AI news : !Lexi discuss`
- **Pipe Output to Input**: `!Anna AI news == !Gus analysis`

## Getting Started

To use Lexideck:

1. Clone the repository.
2. Install necessary dependencies.
3. Modify the Lexideck prompts and knowledge for your specific AI setup.

## Support and Community

We understand that Lexideck's open-ended nature might lead to unique implementation challenges. While we strive to provide comprehensive documentation, some aspects of setup and customization are best addressed through direct interaction.

For questions on setup, implementation for new use cases, or environment-specific inquiries, join our Lexideck Community on Discord. Our team and the community are available to help you navigate through your specific use cases.

Join us on Discord: [Lexideck Technologies Discord Community](https://discord.gg/BmHbCC5nQb)

Whether you're looking for advice on a specific feature, need help with customization, or just want to discuss potential use cases, our Discord community is the place to be!

## Contributing

1. Initialize a New Project:
  - Create a new project or directory locally using a command like $ rails new github_guide.
  - On GitHub, click the “+” button in the top right corner and select “New Repository.”
  - Fill in the repository name and description. Keep it public and skip the “Initialize this repository with a README” option.
  - Click “Create repository.”
  - Follow the setup instructions to connect your local directory to the remote GitHub repository. This includes adding a .git folder and a .gitignore file.
2. Setup Your Team:
  - Add your team members as collaborators. Go to the “Settings” tab of your repository, then select “Collaborators.”
  - Search for GitHub users and add them by clicking “Add Collaborator.”
  - Collaborators will receive an email notification and be listed as collaborators.
  - As a collaborator, clone the project using git clone git@github.com:MinesJA/github_guide.git and navigate into the directory.
3. Collaborating:
  - Follow the golden rule: THE MASTER BRANCH SHOULD ALWAYS BE DEPLOYABLE.
  - Create new branches for features. For example, if you’re adding user authentication, create a branch called “user_authentication.”
  - Make changes in your branch, commit them, and push them to GitHub.
  - When a feature is complete, merge the branch into the master branch.

Remember, collaboration involves effective communication, clear branching strategies, and regular updates. Happy collaborating! 🚀👥🔗

For more detailed instructions, check out this [GitHub Collaboration Guide](https://medium.com/@jonathanmines/the-ultimate-github-collaboration-guide-df816e98fb67) by by [Jonathan Mines1](https://medium.com/@jonathanmines/the-ultimate-github-collaboration-guide-df816e98fb67).

You can also join the [Lexideck Technologies Community Discord](https://discord.gg/BmHbCC5nQb)

## License

Lexideck is licensed under the GNU General Public License v3.0. For more details, see the LICENSE file.
