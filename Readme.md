# Agent Framework (with Microsoft Foundry) workshop (Python)

The purpose of this repository is to provide step-by-step learning to use fundamental Agent Framework functionalities with Microsoft Foundry (Foundry v2).<br>
More advanced topics - such as, multi-agent design patterns, custom objects, etc - are out of scope in this repository.

1. [Getting started](./01_get_started.ipynb)
2. [Trace Agent](./02_trace.ipynb)
3. [Thread (Conversation)](./03_thread.ipynb)
4. [Hosted Tools](./04_hosted_tools.ipynb)
5. [Foundry Tools](./05_foundry_tools.ipynb)
6. [Memory and personalization (Context Provider)](./06_memory.ipynb)
7. [Workflows](./07_workflow.ipynb)
8. [Human-in-the-loop (HITL)](./08_human_in_the_loop.ipynb)
9. Hosted Agent (coming soon ...)

## Prerequisites

Prepare (create) Microsoft Azure subscription.

Create a new Microsoft Foundry resource and project in [Azure Portal](https://portal.azure.com/). In this workshop, we need new Foundry v2 project, not v1 project.

Open Foundry Portal (new portal) and deploy Azure OpenAI model.  
In this workshop, you need to deploy a model supported in Azure OpenAI Responses API. (See [here](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/how-to/responses?view=foundry&tabs=python-key#model-support) for the supported models.)

Create GitHub Codespace to use Jupyter notebook.  
Run the following steps.

1. Login to [GitHub](https://github.com/).
2. Fork this repository.
3. Create a Codespace as follows.
    - Select "Codespaces" in hamburger-menu icon (in top-left corner).
    - Click "New codespace" button.
    - Select above forked repository and submit.

From now, we work in Codespace.  
First, open notebook (.ipynb) in repository, click "Select Kernel" in top-right corner, and install Jupyter extension. (Also, install Python extension.)

Copy ```.env.example``` as ```.env```.  
Open ```.env```, and set variables according to your environment.

Throughtout this workshop, we'll use Azure CLI credential.  
For this reason, open terminal window, install Azure CLI, and login to Azure by running ```az login``` command.

> Note : You cannot use API key in new ```azure-ai-projects```. (See [here](https://learn.microsoft.com/en-us/answers/questions/5587848/how-to-use-api-key-in-azure-ai-foundry).) Use Entra ID users (or service principal) in production.

In terminal windows, install the required Python modules as follows.

```
# required in all exercises
pip install agent-framework --pre
# required in lesson 2
pip install azure-monitor-opentelemetry
```

> Note : This source code is experimented by using ```agent-framework==1.0.0b260107```. Please install this specified version of ```agent-framework``` module, if it doesn't work. (Sorry, but it might change frequently, because it's in preview now.)

> Note : By installing ```agent-framework```, the required sub-packages in Agent Framework are all installed. See [here](https://github.com/microsoft/agent-framework/tree/main/python/packages) for the list of sub-packages.

## Official samples

The purpose of this repository is to provide step-by-step learning with clear explanation (background) to use fundamental Agent Framework functionalities with Microsoft Foundry (Foundry v2).

In [official GitHub samples](https://github.com/microsoft/agent-framework/tree/main/python/samples/getting_started/agents/azure_ai), you can find more advanced code samples to provide a wide variety of scenarios. (Several examples in this repository are based on this official repository.)
