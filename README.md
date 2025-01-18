MemoryMatrix

MemoryMatrix is an open-source, AI-agnostic memory persistence system designed to capture, store, and retrieve user knowledge across multiple AI models and user interactions. Think of it as a long-term, cross-platform "memory capsule" that preserves insights about user behavior, preferences, and context over time.

This project allows developers to implement a standardized user memory system that works with any LLM today and is ready for future AI tools tomorrow. Persistence is the key!

Key Features:

Knowledge Graph: Structured data storage for user knowledge, preferences, and relationships.
Embedding Search: Semantic similarity search using vector embeddings (e.g., OpenAI or local embeddings).
Cross-Compatibility: Works with existing AI models and future tools via an open API.
Open Source: Use, extend, and contribute as you like (with attribution, per license terms).
License:
This project is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0). See the LICENSE file for details.

If you use or adapt this project, please cite the original repository with the following:
MemoryMatrix: A Cross-Platform AI Memory System. URL: https://github.com/[YOUR_REPO]/memory-matrix

Quick Start:

Installation:

Clone the repository and install dependencies: git clone https://github.com/[YOUR_REPO]/memory-matrix.git cd memory-matrix pip install -r requirements.txt
Running the API:

Run the backend locally to interact with the MemoryMatrix system: uvicorn src.api.main:app --reload
You can now access the API locally at http://localhost:8000.
Adding a Memory:
Here’s an example of how to log a memory into the system:

from examples.add_memory import add_memory

Storing a memory about user preferences for Jazz.
add_memory("Jazz Music Interest", "I love jazz and classical piano.", metadata={"tags": ["music", "preferences"], "timestamp": "2023-10-30T10:00:00Z"})

Querying the Memory:
Using the semantic search functionality, you can retrieve memories based on a query.

Here's an example:

from examples.query_memory import search_memory

results = search_memory("I like piano and jazz music.", top_k=3)
print(results)

Contributing:
Contributions are welcome! Whether you’re fixing bugs, adding features, or providing feedback, we’d love to have your input. See the CONTRIBUTING.md file for detailed contributing guidelines.

Roadmap:

Add Neo4j integration for a more scalable knowledge graph.
Enhance API with filters, output formatting, and fine-grained query control.
Build an optional web-based dashboard for visualizing user memory data.
Add support for additional embedding backends (e.g., SentenceTransformers).
Citation:
We kindly request you include the following citation when using the MemoryMatrix codebase in your work:
MemoryMatrix: https://github.com/[YOUR_REPO]/memory-matrix

