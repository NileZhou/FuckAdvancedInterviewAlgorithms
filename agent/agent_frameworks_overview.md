# Logic of survey

1. Establish a knowledge system and index to gain a general understanding of the field, so that related information can be added to our knowledge structure tree in the future.
2. Identify the key issues in each subfield, and determine the key benchmarks / metrics.
3. Understand the key details that we need to focus on (read the readme, code, and papers with questions in mind).


# Befor Read


**C1m** : the number of **C**ommits for recent **1** **m**onth, measure the activity of a repository

We do not account for projects that have not been updated for more than one month, or those projects that C1m less than 5.

The date of survey is July 4, 2024

# Agent

> An "agent" is anything that perceives and takes actions in the world -- wikipedia

The typical minimal operation process of an agent:

Perception -> Planning -> Action

The full operation process of an agent:


# key features of agent

- autonomous
- continual learning
- persistent
- multimodal
- multi-agent cooperation
- complex task solving (divide and conquer)
- **driving method (code, dsl, prompt, etc.)**

# key features of frameworks

- human-in-the-loop
- high-scalability
- app develop platform
- asnyc (和persistent)
- **duplex**
- local-friendly
- cloud-friendly (云端多台实例，得加锁，机制 关闭)
- multi-agent
- **rich-patterns**
- self-host language (驱动方式, dsl, )
- no-handcraft prompt
- include devops
- **support multi-task**  (是否支持多任务)
- **specific stream protocol (用的什么流式协议)**

# agent build frameworks

| framework                                                       | TAG                                                                     | driven method            | supported by                                    | recommend reason                                                                                                               | C1m/Contributors | Star(k)/Fork(k)/PR/Issues |
| --------------------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------ | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ | ---------------- | ------------------------- |
| [sglang](https://github.com/sgl-project/sglang)                    | self-host language                                                      | prompt + custom compiler | stanford & UCBerkely<br />students              | a structured generation language.<br />High-Performance Backend Runtime<br />co-designing the frontend and runtime system.   | 37 / 54          | 2.8 / 0.18 / 8 / 165      |
| [dspy](https://github.com/stanfordnlp/dspy)                        | no-handcraft prompt                                                     | optimizer                | stanfordnlp                                     | The framework for programming—not prompting models.<br />algorithmically optimizing LM prompts and weights                    | 119 / 178        | 13.9 / 1.1 / 62 / 188     |
| [langchain](https://github.com/langchain-ai/langchain)             | include devops<br />self-host language<br />go / js version             | prompt + LCEL            | langchain-ai                                    | a comprehensive ecoysystem for build agent<br />self-host language: LCEL                                                      | 573 / 2898      | 88.5 / 13.9 / 444 / 691   |
| [langgraph](https://github.com/langchain-ai/langgraph)             | multi-agent workflow<br />persistence                                   |                          | langchain-ai                                    | a library for building stateful, multi-actor applications<br />create controllable/persistent agent and multi-agent workflows | 234 / 53         | 4.2 / 0.62 / 17 / 32      |
| [autogen](https://github.com/microsoft/autogen)                    | multi-agent<br />rich-patterns                                          |                          | microsoft                                       | a framework for building multi-agents to solve complex workflows<br />support diverse conversation patterns                   | 67 / 310         | 28 / 4.1 / 114 / 526      |
| [agentUniverse](https://github.com/alipay/agentUniverse)           | multi-agent<br />rich-patterns                                          |                          | alipay                                          | Rich Multi-Agent Collaboration Modes<br />Seamless Integration of Domain Expertise                                             | 103 / 8          | 0.5 / 0.06 / 3 / 1        |
| [livekit/agents](https://github.com/livekit/agents)                | async                                                                   | prompt                   | livekit                                         | an agent sdk for LiveKit WebRTC, used for real-time audio/video generate                                                      | 21 / 18          | 0.64 / 0.10 / 5 / 33      |
| [web-llm](https://github.com/mlc-ai/web-llm)                       | in-browser<br />local-friendly                                          |                          | mlc.ai                                          | leverages WebGPU for hardware acceleration, wihout server-side processing                                                     | 22 / 37          | 11.7 / 0.73 / 1 / 51   |
| [modelscope-agent](https://github.com/modelscope/modelscope-agent) | support async<br />multi-agent (production level)<br />high-scalability | prompt                   | alibaba<br />Institutefor Intelligent Computing | a huggingface-like bridge with llm communities<br />using ray to implement multi-agent mode for efficiency                     | 28 / 37          | 2.2 / 0.24 / 3 / 51       |
| [llama-agents](https://github.com/run-llama/llama-agents)          | async-first<br />multi-agent<br />human-in-the-loop                     | message queue            | LlamaIndex                                      | user <-> control plane <-> MQ <-> agents<br />agents pull from MQ<br />well-abstraction                                        | 51 / 6           | 0.83 / 0.06 / 3 / 18      |
| [dify](https://github.com/langgenius/dify)                         | app development platform                                                |                          | Dify.AI                                         | Coze like platform                                                                                                             | 310 / 286        | 36 / 4.9 / 46 / 271       |
| [Flowise](https://github.com/FlowiseAI/Flowise)                    | just workflow, not agent                                                |                          | FlowiseAI                                       | drag & drop UI to build LLM workflow                                                                                           | 39 / 118         | 27.2 / 14 / 33 / 377      |

# autonomous agent framework

| Project                                                 | TAG                                                                    | driven method            | supported by | recommend reason                                                                                                                    | C1m/Contributors | Star(k)/Fork(k)/PR/Issues |
| ------------------------------------------------------- | ---------------------------------------------------------------------- | ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ------------------------- |
| [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) | autonomous                                                             | prompt                   | AutoGPT      | autonomously accomplish minor tasks<br />thriving ui / cli ecosystem                                                                | 40 / 722         | 164 / 43.4 / 17 / 50      |
| [aiwaves-cn/agents](https://github.com/aiwaves-cn/agents)  | autonomous                                                             | loss and backpropogation | AIWaves      | Agent symbolic learning                                                                                                             | 5 / 22           | 4.8 / 0.37 / 1 / 32       |
| [crewAI](https://github.com/joaomdmoura/crewAI)            | persistent<br />multi-agent<br />complex task solving                  |                          |              | enable AI agents like a well-oiled crew                                                                                            | 47 / 98          | 16.8 / 2.3 / 44 / 412     |
| [llama-agents](https://github.com/run-llama/llama-agents)  | multi-agent<br />async-first                                           |                          |              | async-first framework for building multi-agent systems                                                                             | 48 / 6           | 0.79 / 0.061 / 4 / 16     |
| [MemGPT](https://github.com/cpacker/MemGPT)                | long-term memory/state                                                 |                          |              | Create agents with long-term memory and custom tools                                                                               | 24 / 27          | 10.7 / 1.2 / 14 / 246     |
| [uAgents](https://github.com/fetchai/uAgents)              | support decorates                                                      |                          |              | create agents with simple and expressive decorators                                                                                | 15 / 54          | 0.77 / 0.2 / 22 / 27      |
| [skyvern](https://github.com/Skyvern-AI/skyvern)           | autonomous<br />multimodal<br />manipulate-browser<br />cloud-friendly | dom + Prompt + image     | skyvern      | interact with websites using browser automation<br />support to run multiple instances in parallel to automate workflows at scale | 93 / 14          | 5.4 / 0.39 / 3 / 15       |
|                                                         |                                                                        |                          |              |                                                                                                                                     |                  |                           |
|                                                         |                                                                        |                          |              |                                                                                                                                     |                  |                           |

# programmer agent

key-features:

- AI Team
- devin-like (coding, debug, web browsing, terminal using)
- complex task solving
- 

key-benchmarks:

- [SWEBench](https://www.swebench.com/)
- 

| Project                                                       | TAG                | supported by  | recommend reason                                                                          | C1m/Contributors | Star(k)/Fork(k)/PR/Issues |
| ------------------------------------------------------------- | ------------------ | ------------- | ----------------------------------------------------------------------------------------- | ---------------- | ------------------------- |
| [ChatDev](https://github.com/OpenBMB/ChatDev)                    | AI Team            | OpenBMB       | a virtual software company                                                               | 18 / 50          | 24.3 / 3.1 / 14 / 19      |
| [MetaGPT](https://github.com/geekan/MetaGPT)                     | AI Team            | community     | First AI Software Company                                                                 | 4 / 90           | 41.4 / 4.9 / 38 / 278     |
| [OpenDevin](https://github.com/OpenDevin/OpenDevin)              | devin-like         | community     | collaborate with human to write code, fix bugs, and ship features.                       | 242 / 156        | 28.3 / 3.2 / 32 / 142     |
| [devika](https://github.com/stitionai/devika)                    | devin-like         | stition.ai    | agentic AI software Engineer.<br />support dynamic agent state tracking and visualization | 2 / 43           | 17.8 / 2.3 / 41 / 108     |
| [Devon](https://github.com/entropy-research/Devon)               | devin-like         | community     | An open-source pair programmer                                                            | 169 / 12         | 2.3 / 0.17 / 7 / 14       |
| [SWE-agent](https://github.com/princeton-nlp/SWE-agent)          | devin-like         | princeton-nlp | It solves 12.47% of bugs in the SWE-bench evaluation set and takes just 1 minute          | 45 / 46          | 11.9 / 1.2 / 8 / 56       |
| [auto-coder-rover](https://github.com/nus-apr/auto-code-rover)   | autonomous         | community     | 30.67% (pass@1) in SWE-bench lite with each task costs less than $0.7                    | 5 / 8            | 2.4 / 0.23 / 0 / 12       |
| [plandex](https://github.com/plandex-ai/plandex)                 | all-in-terminal    | plandex-ai    | AI coding agent in terminal, designed for large, real-world tasks.                       | 37 / 15          | 9.8 / 0.7 / 3 / 23        |
| [gpt-engineer](https://github.com/gpt-engineer-org/gpt-engineer) | just terminal tool | community     | an AI tool in terminal                                                                    | 3 / 102          | 51.3 / 6.7 / 4 / 6        |
| [auto-dev](https://github.com/unit-mesh/auto-dev)                | just IDE plugin    | community     | powerful IDE plugin                                                                       | 28 / 16          | 2.6 / 0.3 / 0 / 7         |
| [gpt-pilot](https://github.com/Pythagora-io/gpt-pilot)           | just IDE plugin    | Pythagora     | pairprogrammer in vscode, to build realworld apps                                         | 44 / 44          | 29.1 / 2.9 / 12 / 205     |
| [aider](https://github.com/paul-gauthier/aider)                  | all-in-terminal    | community     |                                                                                           | 268 / 31         | 12.7 / 1.2 / 13 / 77      |
|                                                               |                    |               |                                                                                           |                  |                           |
|                                                               |                    |               |                                                                                           |                  |                           |

# research agent

key features:

- support scraping
- keep track
- support local files

| framework                                                    | TAG                                                                                        | driven method | supported by | recommend reason                                                                                                                     | C1m/Contributors | Star(k)/Fork(k)/PR/Issues |
| ------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ---------------- | ------------------------- |
| [gpt-researcher](https://github.com/assafelovic/gpt-researcher) | autonomous<br />support-scraping<br />keep track<br />support local files<br />multi-agent |               | community    | solve the infinite loop problems by<br />can generate whole research report<br />agents are divided into planner and execution ones. | 40 / 52          | 13 / 1.6 / 9 / 29         |

# agent as OS

key features:

| Project                                      | TAG | driven method | supported by | recommend reason       | C1m/Contributors | Star(k)/Fork(k)/PR/Issues |
| -------------------------------------------- | --- | ------------- | ------------ | ---------------------- | ---------------- | ------------------------- |
| [AIOS](https://github.com/agiresearch/AIOS)     |     |               | community    | LLM as the brain of OS | 17 / 20         | 2.9 / 0.3 / 0 / 7         |
| [MemGPT](https://github.com/cpacker/MemGPT)     |     |               | community    |                        | 28 / 90          | 10.7 / 1.2 / 15 / 249     |
| [phidata](https://github.com/phidatahq/phidata) |     |               | phidata      |                        | 46 / 37          | 10.5 / 1.5 / 21 / 48      |

# *AIGC-centric software architecture

key features:

- distributed

| Project                                          | TAG         | supported by | recommend reason                                                             | C1m/Contributors | Star(k)/Fork(k)/PR/Issues |
| ------------------------------------------------ | ----------- | ------------ | ---------------------------------------------------------------------------- | ---------------- | ------------------------- |
| [unit-mesh](https://github.com/unit-mesh/unit-mesh) | distributed | community    | AIGC-centric distributed software architecture<br />unit are generated by AI | 0 / 3            | 0.18 / 0.02 / 0 / 0       |
|                                                  |             |              |                                                                              |                  |                           |