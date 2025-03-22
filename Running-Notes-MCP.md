# MCP



Q: What is MCP ?     
-> Model Context Protocol: MCP is an open protocol that standardizes how applications provide context to LLMs
 
Model: LLM models
Context: Extra/ External Info (Knowledge / Information to be fed to the model)
Set of Rules Protocol: Rules

LLMs have limited context. We can't every time train a model or feed all the info into a model.
MCP helps in providing context to the model in a structured and efficient way.

What are the components of a MCP Server ?
* MCP Hosts: LLM, IDEs, Cursors etc. e.g. Claude model from Anthropic is a MCP Host if we are using Claude as an LLM
* MCP Client: It is such a software which maintains the connection between MCP servers and Hosts i.e. LLM/IDEs etc.
    * In Cursor a MCP client is there internally built by Cursor, can be used directly.
* MCP Server: Lightweight program that we build for different tasks    
* Local Data Sources: Your computer’s files, databases, and services  
* Remote Services: External systems available over the internet (e.g., through APIs)
How does MCP works?
Ans: It works on standard input output i.e. STDIO

What is a standard input output? 
e.g. A terminal in VSCODE can work as an interface for standard input & output. i.e. we type something as standard input and the terminal shows the output as standard output. 
So it works on a print statement of a terminal
console.log() for getting the output in a structured format. And it feeds this into the LLM.



References: https://modelcontextprotocol.io/introduction
YT videos: https://www.youtube.com/watch?v=vYelTr1uQmA
