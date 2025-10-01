# n8n Multi-Agent Handoff Templates

Two n8n workflow templates demonstrating different patterns for implementing multi-agent AI systems with handoff capabilities.

## Blog Post

Read the full article explaining these templates: **[YOUR BLOG POST LINK HERE]**

## Overview

These templates showcase how to build conversational AI systems where multiple specialized AI agents can collaborate and pass control between each other. Both workflows use OpenAI's language models and n8n's langchain nodes.

### Template 1: Demonstrate Agent Pass Off

A simple two-agent system where Agent 1 receives user input, processes it, and passes its output to Agent 2 for further processing. This demonstrates the basic pattern of sequential agent communication.

**Key Features:**
- Sequential agent handoff (Agent 1 → Agent 2)
- Shared memory for conversation context
- Separate response nodes for each agent

**Use Cases:**
- Simple two-step workflows
- Processing that requires distinct expertise areas
- Sequential refinement of outputs

### Template 2: Example Agent Handoff Switch

A more sophisticated system with a Master Agent that routes user requests to one of three specialized agents (Agent 1, 2, or 3) based on the request content. Each agent maintains its own memory and can continue the conversation.

**Key Features:**
- Master Agent routing logic
- Three specialized sub-agents
- Switch-based conditional routing
- Independent memory for each agent
- JSON-based inter-agent communication

**Use Cases:**
- Multi-specialist AI systems
- Triaging and routing user requests
- Maintaining separate conversation contexts per specialty

## Prerequisites

Before using these templates, ensure you have:

1. **n8n instance** - Either cloud or self-hosted (version 1.0+)
2. **OpenAI API account** - You'll need API credentials configured in n8n
3. **n8n langchain nodes** - These come standard with recent n8n versions

## How to Import

### Step 1: Download the Templates

Download the JSON files from this repository:
- `Demonstrate Agent Pass Off.json`
- `Example Agent Handoff Switch.json`

### Step 2: Import into n8n

1. Open your n8n instance
2. Click on **Workflows** in the left sidebar
3. Click the **Import** button (or use the **+** button and select **Import from File**)
4. Select one of the downloaded JSON files
5. Click **Import**

### Step 3: Configure Credentials

After importing, you'll need to set up your OpenAI credentials:

1. In the imported workflow, locate the **OpenAI: gpt-4.1-mini** node
2. Click on the node to open its settings
3. Click on the **Credential to connect with** dropdown
4. Select an existing OpenAI credential or create a new one:
   - Click **Create New**
   - Enter your OpenAI API key
   - Give it a name and save

### Step 4: Activate and Test

1. Click the **Activate** toggle in the top-right corner
2. Use the **Test Workflow** button or the chat interface to interact with your agents
3. Watch the execution flow to see how agents communicate

## Customization Tips

- **Modify System Messages**: Update the `systemMessage` parameter in each agent node to customize agent behavior
- **Change Models**: Switch between different OpenAI models (GPT-4, GPT-3.5, etc.) based on your needs
- **Adjust Memory**: Modify the `contextWindowLength` in memory nodes to control conversation history
- **Add More Agents**: Extend the switch template by adding additional agents and routing rules

## Screenshots

See `Workflow-1.JPG` and `Workflow-2.JPG` for visual examples of how these workflows appear in the n8n interface.

## License

Feel free to use, modify, and distribute these templates for your projects.

## Feedback

If you have questions or suggestions, please reach out via [your preferred contact method].
