# AI Agent with External Tool Access
### Objective
 Build an AI agent that can use external tools to answer queries like loan EMI, currency conversion, and weather info.

### Tools & Tech:
- LangGraph (Orchestrator)
- LangChain Tools: Calculator, PythonREPLTool, RequestsGetTool
- Gemini API (LLM)

### Implementation Steps:

- Install LangGraph:
 pip install langgraph
- Define tools in LangChain using the Tool schema.
- Implement a ReAct-style agent for multi-step reasoning.
- Design prompt templates to instruct the agent which tool to use.

### Example Query:

- “What’s the EMI for a ₹10L loan over 5 years at 8.5% interest?”

Code Example:
<img width="1047" height="627" alt="task2_input" src="https://github.com/user-attachments/assets/be013921-9e7f-45c7-830b-9ae6126d0e31" />
Sample Output:
<img width="1327" height="660" alt="task_output" src="https://github.com/user-attachments/assets/cb9e62a0-a4fb-41d5-9a8e-ce09788dce6c" />
