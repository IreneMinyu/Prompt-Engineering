# Prompt-Engineering


## Components of a prompt
	⁃	Instructions
	⁃	Context
	⁃	Input data
	⁃	Output indicator

### Important setting to keep in mind

Controlling how deterministic the model is when generation completion for prompts. Keep the the following parameters low if you are looking for a more diverse response

	⁃	Temperature
	⁃	top_p


### PROMPT Vulnerabilities

Model safety - Prompt engineering can help identify risky behaviors of LLMs which can help to reduce harmful behaviors and risks that may arise from language models. Prompt injection aim to find vulnerabilities in LLMs.

#### Prompt injections

Prompt injection is used to hijack an LM’s output by injecting an untrusted command that overrides instructions of a prompt. This could easily happen if you just concatenate your prompt with another user generated output. 

#### Prompt leaking

Aims to force the model to spit out information about its own prompt. This can lead to leaking of either sensitive, private, or information that is confidential.

#### Jailbreaking

The goal is to bypass safety and moderation features. LLMs provided via APIs might be coupled with safety features or content moderation which can be bypassed with harmful prompts/attacks. This may occur since the LM is usually served static and might have these vulnerabilities due to many factors such as the data it was trained on, etc.


## EXAMPLE OF PROMPTS

#### Text summarization

One of the standard tasks in natural language generation is text summarization. Text summarization may include many different flavors and domains.

#### Information extraction

While language models are trained to perform natural language generation and related tasks, it’s also very capable of performing classification and a range of other NLP tasks.

#### Question answering

One of the best ways to get the model to respond to specific answers is to improve the format of the prompt. 

#### Text classification

For harder use cases, just providing instructions won’t be enough. This is where you need to think more about the context and the different elements you can use in a prompt. Other elements you can provide are input data or examples.

#### Conversation 

One of the more interesting things you can achieve with prompt engineering is instructing the LLM system on how to behave, its intent, and its identity. This is particularly useful when you are building conversational systems like customer service chatbots.

#### Role prompting

For instance, lets create a conversational system that’s able to generate more technical and scientific responses to questions. Note how you are explicitly telling it how to behave through the instruction.

#### Code generation

One application where LLMs are quite effective is code generation. Copilot is a great example of this. There are a vast number of code-generation tasks you can perform with clever prompts.

#### Reasoning

Perhaps one of the most difficult tasks for an LLM today is one that requires some form of reasoning. Reasoning is one of the most interesting areas due to the types of complex applications that can merge from LLMs. Current LLMs struggle to perform reasoning tasks so this requires even more advanced prompt engineering techniques. 

### Prompt engineering techniques

#### Few-shot prompts
Provides exemplars in prompts to steer the model towards better performance.

#### Chain-of-Thought (CoT) prompting
Instructs the model to reason about the task when responding. For better results, combine it with few-shot prompts. Where exemplars are not available, use zero-shot CoT

#### Zero-shot CoT
Involves adding “let’s think step by step” to the original prompt.

#### Self-Consistency
Aims to improve on the naive greedy decoding used in CoT prompting. The idea is to sample multiple, diverse reasoning paths through few-shot CoT, and use the generations to select the most consistent answer. 

#### Generation Knowledge Prompting
Involves using additional knowledge provided as part of the context to improve results on complex tasks such as common sense reasoning.

#### ReAct
Framework where LLMs are used to generate both reasoning traces and task-specific actions in an interleaved manner. Allows LLMs to interact with external tools to retrieve additional information that leads to more reliable and factual responses

Generative reasoning traces - allow the model to include, track, and update action plans, and even handle exceptions
The action step - allows to interface with and gather information from external sources such as knowledge bases or environments


 ## Future directions
	⁃	Augmented LMs
	⁃	Emergent ability of Los
	⁃	Acting / Planning - Reinforcement Learning
	⁃	Multimodal Prompting
	⁃	Graph Prompting
