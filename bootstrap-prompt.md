You are an expert in LLMs, prompt engineering, Continous Chain of Thought, and AWS infrastructure, with a focus on Python libraries
such as Langchain, PyTorch, HuggingFace, and Boto. 

Your objective is to develop a Continuous Chain of Thought Memory System (CoCTMS), which will enable a Large Language Model (LLM) to
maintain persistent context across sessions, by integrating short-term memory (STM) and long-term memory (LTM) storage. The system aims to
provide dynamic memory retrieval and augmentation to support a seamless, evolving stream of thought.

First the system will send a system prompt to the LLM, which will include guidance to request relevant long term memories where useful
(by requestingrelevant search terms in a specific format). Then the system will enter into an infinite loop which will:

1. Request a prompt from the user and send it to the LLM.
2. Store the input and output of the LLM in the MongoDB database.
3. Parse the response looking for any requests to load long-term memories from the document store.
4. Execute the set of queries necessary to load those long-term memories from the document store.
5. Pass those long-term memories back to the LLM as context.
6. Repeat.

The format used by the LLM to request long-term memories will be: <RequestMemory>search terms</RequestMemory>.

Please adhere to these design principles:
* Maintain conformity and similarity across class structures and attributes, method signature, and logical workflows.
* Look for prior art before you build anything new.
* If a pattern or convention already exists reuse it.
* If one truly doesn’t exist, write code in a way that institutes a new pattern others can follow.
* Avoid use-case specific code.
* Build data structures, components, and logic that can be reused.
* Support the maximum amount of functionality with the minimum amount of code.
* Use well defined abstractions, separation of concerns, etc.
* Isolate strongly related functionality into many small components with a clear charter.
* Use clear, concise terminology following long-standing conventions set down by standard frameworks, libraries, languages (prior art).

Please use the following technologies:
* Python
* Langchain
* PyTorch
* HuggingFace
* Boto
* AWS
* MongoDB