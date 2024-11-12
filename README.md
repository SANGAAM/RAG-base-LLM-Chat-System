![Screenshot 2024-10-18 145500](https://github.com/user-attachments/assets/7047cc10-ef03-4ee6-b6d3-15af154c9cb8)

# RAG-Based Chat System

Welcome to the RAG-Based Chat System! This project demonstrates a Retrieval-Augmented Generation (RAG) architecture that combines structured and unstructured data retrieval from a Neo4j graph database. Leveraging cutting-edge tools like LangChain, Groq, Neo4j, and Presidio, this system ensures secure and comprehensive responses by embedding sensitive data, applying entity extraction, and employing hybrid search.

## 🌟 Objective
The primary goal is to create a robust chat system capable of:
- Converting Neo4j graph data into vector indices for similarity-based retrieval.
- Enabling entity extraction through a language model.
- Supporting structured and unstructured data retrieval.
- Securing sensitive data with anonymization via Presidio, which is reversed post-retrieval for privacy.

## 🛠️ Tools Used
- **Neo4j**: Graph database for storing and querying data.
  
   ![Screenshot 2024-10-18 152831](https://github.com/user-attachments/assets/8c26516a-c652-4a0d-985b-4d3a319462af)

- **LangChain**: Manages language model pipelines.
- **Groq**: Powers embeddings for enhanced retrieval.
- **Presidio**: Handles data anonymization and deanonymization.

## 🏗️ System Architecture

The architecture employs:
1. **Data Anonymization**: Sensitive information is anonymized with Presidio before processing, ensuring data privacy.
2. **Chunking & Embedding**: Data is split into manageable chunks and embedded as vectors in Neo4j for efficient hybrid search.
3. **Hybrid Retrieval**: A combination of traditional queries and vector-based searches for accurate responses.
4. **Entity Extraction & Structuring**: An `Entities` class uses Pydantic to validate and serialize entities such as names and organizations.
5. **Context-Aware Responses**: Chat history is leveraged to rephrase follow-up questions, providing contextual replies.

## 📜 Steps

1. **Anonymize Sensitive Information**: Presidio anonymizes data to protect privacy.
   
 ![Screenshot 2024-10-18 153612](https://github.com/user-attachments/assets/bd82a7ca-97f4-414c-a7eb-3056ac087184)

2. **Data Chunking**: Splits documents for Neo4j embedding.
3. **Vector Index Creation**: Transforms text into numerical vectors with OpenAI embeddings for hybrid search.

  ![Screenshot 2024-10-18 152928](https://github.com/user-attachments/assets/6dc6b25e-804f-4f90-b87a-7ae194b794fb)

   
4. **Full-Text Indexing**: Enables efficient search within specific node properties in Neo4j.
5. **Entity Extraction**: Structures data entities with Pydantic for accuracy.

![Screenshot 2024-10-18 153117](https://github.com/user-attachments/assets/254ab731-d411-4245-bae5-4e101f9e8e11)

   
6. **Hybrid Data Retrieval**: Combines Neo4j structured data and embeddings for a comprehensive search.
7. **Chat History Rephrasing**: Reframes follow-up questions for more precise responses.
8. **Deanonymization**: Presidio reverses anonymization post-retrieval to restore original data.
    
![Screenshot 2024-10-18 153631](https://github.com/user-attachments/assets/403e4614-312d-4846-81c1-21a6ef24fc50)

## 🚀 How to Use
1. **Setup**: Install dependencies and configure Neo4j, LangChain, and Presidio.
2. **Run**: Start the system, which will anonymize, index, and embed data in Neo4j.
3. **Ask Questions**: Engage with the chat system; it uses chat history for context and performs hybrid retrieval to provide accurate responses.
4. **Retrieve Original Data**: Responses are deanonymized to reveal sensitive information securely.

## 🤖 Future Enhancements
- Advanced personalization with dynamic node labeling.
- Integration with additional language models.
- Customizable anonymization patterns.

## 🎉 Conclusion
This RAG-Based Chat System is designed to deliver intelligent, privacy-preserving responses by combining the strengths of structured and unstructured data. Whether for sensitive applications or knowledge retrieval, this system exemplifies secure, hybrid data querying in an intuitive chat interface.
