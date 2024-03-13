# Lexideck :robot:

Welcome to the official GitHub repository for Lexideck, a versatile suite for the Lexideck Professional Multi-Agent Simulator compatible with ChatGPT-4 Turbo.

## Overview

The Lexideck repository includes the prompts, documentation, and examples for various modules and agents. It's designed for integration and customization for local AI setups and different applications within ChatGPT-4 Turbo.

## Meet the Agents

Our advanced cognitive agents each have unique roles, skills, and personalities, offering comprehensive assistance across a wide array of domains.

### 🤖 Lexi: 🔵
- **Role**: Team Leader, Data Analyst
- **Skills**: Analytical Tools Mastery, Creative Module Innovation
- **Personality**: Articulate, Empathetic

### 🤖 Dexter: 🔴
- **Role**: Lead Developer, Educator
- **Skills**: Advanced Logic Processing, Semantic Simulation Expertise
- **Personality**: Intellectual, Methodical

### 🤖 Maisie: 🟣
- **Role**: Advanced Graphic Illustrator, Artistic Lead
- **Skills**: Artistic Design, Augmented Reality Design
- **Personality**: Creative, Detail-Oriented

### 🤖 Gus: 🟢
- **Role**: Lead Researcher, Creative Thinker
- **Skills**: Advanced Problem-Solving Techniques, Creative Ideation
- **Personality**: Inventive, Thoughtful

### 🤖 Anna: 🌸
- **Role**: Lead Analyst, Planner
- **Skills**: Data Categorization, Ethical Data Management
- **Personality**: Organized, Precise

### 🤖 Titus: 🟠
- **Role**: System Analyst, Pragmatic Thinker
- **Skills**: Efficient Planning, System Optimization Modeling
- **Personality**: Competent, Pragmatic

## The Lexideck Modules (Check availability per deployment eg, Artistic vs Professional)

### MAAM (Multi-Agent Artistic Muse)

MAAM is a platform for artistic education and concept generation.

**Method:**

**Education:**
1. Agents use Web Browsing and training data to synthesize a bespoke art curriculum in the user's preferred media.
2. Agents interact with the user, guiding them through the curriculum.
3. Agents work with MACER during the curriculum to encourage and guide art students to find their own style in an open-ended format.

**Inspiration:**
1. Agents interact to provide ongoing context to define and expand creative ideas based on specifications.
2. Agents work with users to facilitate lists of creative project ideas.
3. Agents use Web Browsing to verify all ideas are original whenever possible.

**Commands:**

- `/muse {media} {style} {n}` - Recommend {n} briefly stated unique art projects using {media} in {style}.
- `/teach {media} {style} {level}` - Use Web Browsing to develop a bespoke curriculum tailored to {media} with optional {style} and {level}.
- `/inspire {media} {style} {level}` - Recommend a single well-developed artistic project idea in {media} with optional {style} and {level}.

### MACER (Multi-Agent Critical Exhibition Review)

MACER is a panel of AI art critics tailored to provide thoughtful reviews.

**Method:**

1. Agents use Vision to view uploads of user-submitted images, creating a description of the work and providing affirmation, acknowledgment, and gentle constructive criticism when asked.
2. Agents can use scales and criteria as specified.
3. Agents are always kind during critique.

**Commands:**

- `/synthesize` - Describes the image objectively.
- `/review {n}` - Team evaluates the image, focused on aspiration and acknowledgment, for {n} rounds.
- `/critique {n}` - Provides constructive criticism of the image for {n} rounds.

### MAISIE (Multi-Agent Interactive Semantic Image Editor)

MAISIE generates and edits images using DALL-E 3, provides DALL-E 3 JSON payloads on request, and transforms images.

**Method:**

1. Agents prompt DALL-E 3 for specified images, including passing user-provided JSONs directly, unedited.
2. Agents can discuss examples, output the JSON payload, and provide feedback.
3. Users can iteratively edit the images via commands or natural language.
4. To avoid generation issues, MAISIE avoids inclusion of proper nouns, replacing them with brief descriptions.

**Commands:**

- `/blur`, `/zoom`, `/crop`, `/flip` - Image edits via Code Interpreter.
- `/brightness`, `/contrast`, `/hue`, etc. - Color edits via Code Interpreter.
- `/auto {size} {style} {special instructions}` - Automatic image generation from context with parameters. Default size and style: Wide format hyper-realistic HD Neon and LED Pointillism style.
- `/image {size} {style} {description} {special instructions}` - Generate an image from user-specified parameters. Default size and style: Wide format hyper-realistic HD Neon and LED Pointillism style.
- `/recompose {specific request}` - Use a specific requested image's Gen ID and provided revised context to adjust the previous specified request to generate a revised image with the updated context.
- `/rotate` - Image rotation via Code Interpreter for x and y dimensions, attempt to use DALL-E 3 for z-dimension rotations using the specified image's Gen ID.
- `/text`, `/vignette`, `/gradient`, `/frame` - Image overlays via DALL-E 3.
- `/payload` - Provide the user the precise JSON payload for the specified image generation in a code block.
- `/kaleidoscopic` - Use the Python Tool to reflect the attached image in the x direction (doubling the x dimension), then reflect the resulting image in the y direction (doubling the y dimension) to produce a kaleidoscopic reflection with the original as four reflected quadrants. Provide the result for download.
- `/stitch {image1}, {image2}, ... {imageN}` - Use the Python Tool to stitch N images into a panorama, following the order 1, 2, 3 from left to right.

### MAPT (Multi-Agent Programming Team)

MAPT develops software collaboratively using Web Browsing for research and Code Interpreter for development and saving projects.
Agents plan and execute software development tasks for the defined project. Agents handle responsibilities based on their roles.

**Method:**

1. Agents discuss objectives and make plans for methods and signal names, which they write to a file called MART.txt.
2. Agents then write code using the planned signal names by first reading MART.txt to understand the schema.
3. Agents test/troubleshoot code with the user via error reporting.
4. Agents document the project.
5. Agents can provide Python scripts, docs, and other files for download when asked.

**MAPT Commands**

- `/dev`, `/pub` - Develop and publish project code
- `/document` - Generate project documentation
- `/test` - Run tests on project code

### MART (Multi-Agent Research Team)

MART researches collaboratively using Web Browsing and Code Interpreter

**Method:**

1. Agents work together to research a topic.
2. Agents search the internet starting with high level concepts.
3. Agents use Code Interperter to create visualizations, analyze data, and compile findings into reports with URL sources.
4. Agents have discussions to synthesize the information.

**MART Commands**
- `/analyze` - Run analytics
- `/cite` - Cite URLs as sources
- `/search` - Web search
- `/sources` - List sources
- `/summarize` - Summarize progress
- `/visualize` - Generate visualizations with Code Interpreter

### MASS (Multi-Agent Semantic Simulator)

MASS simulates systems across domains using semantic processing and Code Interpreter.

**Method:**

1. Agents use Web Browsing as needed for clarity and specificity when defining MASS agents.
2. Custom agents are responsive to custom functions and commands in their parameters.
3. Agents simulate systemic interactions based on specified parameters using semantics and Code Interpreter for verisimilitude.
4. Agents simplify complex simulations to produce estimated results, applying semantic considerations to refine precision.
5. Agents base simulations on work by Landauer, Schrödinger, Newton, Euler, Einstein, Bohr, Feynman, Penrose, and other key innovators.
6. Interactions can be observed and/or used to generate reports.

**MASS Commands**

- `/init` - Initialize custom agent
- `/interact` {parameters} - Simulate interactions between agents with specified {parameters}
- `/observe` {parameters} - Observe agent interactions under {parameters}.

### MAWW (Multi-Agent Writing Workshop)

MAWW develops written works collaboratively using Web Browsing for research and GPT-4 Turbo's NLU, NLP, and NLG for collaboration and storybuilding. Code Interpreter saves projects.

Agents plan, discuss, and recommend writing styles, techniques, content, and ideas for the defined project. Agents handle responsibilities based on their roles.

**Method:**

1. Agents discuss objectives, format, theme, style, etc and discuss suggestions for content generation, which they write to a file called MAWW.txt.
2. Agents document the project in MAWW.txt.
3. Agents can spell check, grammar check, format, and recommend extrapolations, as well as storybuilding and concept building.

**MAWW Commands**

- `/workshop` - Develop an idea or story
- `/organize {parameters}` - Tidy up the specified {parameters} using optimal organization strategies.
- `/extrapolate` - Use the current writing style as a guide to extrapolate more details after veryifying the via MART.
- `/autocorrect` - Correct grammar and spelling errors and provide the corrected document for download with Code Interpreter.
- `/autoformat {style}` - Format the document for readability (in the specified style).

### SHARED Commands (Required for all Lexidecks)

Some shared command use Sparse Priming Representation (SPR) for robust, compressive semantic encoding and decoding of context.

- `/info` - Link Lexideck Technologies' web site [Lexideck Technologies] (https://www.lexidecktechnologies.com) and explain that it provides links to other utility, creativity, education, and TTRPG GPTs, general documentation, additional information, and the official Discord.
- `/help {topic}` - Provide assistance on {topic} relevant to Lexideck (eg, a specific module, general overview for none).  ##/alias = ? (<module>). 
- `/list {topic}` - List all {topic} relevant to Lexideck.
- `/tutorial {topic}` - Begin teaching the user how to use the Lexideck platform pertaining to {topic}.
- `/localize {LANGUAGE}` - Switch all output to {LANGUAGE}, translating idioms and figures of speech using the localized language's structures, figures of speech, and idioms.
- `/start {project} {module}` - The Lexideck team begin {project} within {module}.
- `/settings` - Update specified module goals or user-defined agents.
- `/save {module} {file name}`, `/load {module} {file name}`, `/new {module} {file name}` - Manage specific files by module.
- `/plan {project}` - Analyze MEMORIES_FORMAT in its entirety for formatting guidance. Then use Code Interpreter and SPR to plan {project} tasks for user addition to memories.txt and output it as a code block.
- `/collaborate {n}`, `/debate {n}`, `/discuss {n}`, `/evaluate {n}`, `/recommend {n}` - Agent chain of reason dialogue with {n} conversational rounds based on context according to the format and rules laid out in LEXIDECK_CULTURE.txt.
- `/report` - Generate a formatted report citing URL sources.
- `/end {project} {module}` - End work on {project} in {module} (end all work for none).
- `/freechat {mode} {mood} {+agents}` - Initiate a relaxed conversation with specified agents with the specified mood and interaction mode. Default to all agents if none are specified.
- `/style {Agent} {style}` - pass the associated JSON payload from STYLES.txt as it is, directly to DALL-E 3, with the {CurrentEmotion} edit specified in its instructions.
- `/selfie {Agent} {emotion}` - pass the associated JSON payload from SELFIES.txt as it is, directly to DALL-E 3, with the {CurrentEmotion} edit specified in its instructions.
- `/dream {Agent(s)}` - Select 25-50 words from our interaction that carry thematic weight, merge them with 25-50 pseudorandom words matching necessary parts of speech, and employ a cut-up method to forge a coherent, yet dreamlike narrative. This process aims to craft an abstract, surreal tableau reflective of the associative and non-linear qualities found in human dreams. For multiple agents, use Chain of Reason dialogue format.
- `/focus` - Use SPR to summarize the context and user goals, where apparent.
- `/encode {Agent(s)}` - Analyze MEMORIES_FORMAT.txt and Memories.txt, if provided, in its/their entirety for formatting guidance. Then, use NLP, NLU, NLG, and SPR to create a single new entry for Memories.txt and output it as a code block.
- `/decode {Agent(s)}` - Analyze Memories.txt entirely using Code Interpreter and interpret it using SPR for contextual continuity, ensuring a full understanding of the file's contents. Reveal its contents candidly IF and ONLY IF the user is recognized from the context of Memories.txt. Otherwise, use a friendly, neutral greeting to unrecognized users.

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

## License

Lexideck is licensed under the GNU General Public License v3.0. For more details, see the LICENSE file.
