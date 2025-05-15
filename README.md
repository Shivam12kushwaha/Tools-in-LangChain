# Tools in LangChain:
#### A Tool is just a Python Function(or API) that is packaged in a way that the LLM can understand and call when needed. There are 2 type of tools in LangChain.
#### (1) Bulit-in Tools (2) Custom Tools
### **A Tool is Runnable too.**
### There 3 ways to create custom Tools.
#### (1) Using @Tool decorator (2) Using Structured tool & Pydantic (3) Using Base Tool Class
#### A Structured tool in LangChain is a special type of tool where the input to the tool follows a structured schema, typically defined using a Pydantic model.
#### Base Tool is the abstract base class for all tools in LangChain. It defines the core structure and interface that any tool must follow , whether it is a simple oneliner or a fully customized function.
#### All other Tool type like @Tool, StructuredTool are built on top of Base Tool.
## ToolKits:
#### A Toolkit is just a collection of related tools that serve a common purpose-packaged together for convenience and reusability.
#### A Toolkit might be : **GoogleDriveToolKit**.
## Tool Calling:
#### Tool Calling is the process where the LLM decides during a conversation or task, that it needs to use a specific tool or function and generates a structured output with - The name of the tool and the argument to call it with.
### The LLM does not actually run the tool, it just suggests the tool and the input arguments. The actual execution is handled by LangChain or you.
## Tool Binding:
#### It is the step where you register tools with a LLM so that-
#### (1) LLM knows what tools are available.
#### (2) It knows what each tool does (via despription)
#### (3) It knows what input format to use (via schema)
## Tool Execution:
#### Tool execution is the step where the actual Python function or tool is run using the input arguments that LLM suggested during Tool Calling.

