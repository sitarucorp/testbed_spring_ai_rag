

```bash
irm https://ollama.com/install.ps1 | iex

ollama pull nomic-embed-text
ollama pull llama3.2 @ 2 GiB
ollama pull llama4 # 67 GiB
ollama list
ollama ps
ollama run llama3.2 


docker run -d --name pgvector -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=ragdb -p 5432:5432 pgvector/pgvector:pg17


ollama stop llama3.2 

```

http://localhost:8080/api/rag?question=What%20is%20of%20Spring%20Boot

{

"question": "What is of Spring Boot",

"answer": "Spring Boot is a framework built on top of the Spring Framework that makes it easier to create production-ready Java applications.",

"sources": [

{

"content": "Spring Boot Guide A practical reference document for the Spring AI RAG demonstration. 1. What is Spring Boot? Spring Boot is a framework built on top of the Spring Framework that makes it easier to create production-ready Java applications. It provides sensible defaults, automatic configuration, sta…"

}
]
}

```prototext
http://localhost:8080/api/rag?question=What is Capital of France
{
"question": "What is capital of France",
"answer": "The capital of France is Paris.",
"sources": [
{
"content": "No. Country Capital 1 India New Delhi 2 United States Washington, D.C. 3 United Kingdom London 4 France Paris 5 Japan Tokyo 6 Australia Canberra 7 Canada Otawa 8 China Beijing 9 Brazil Brasília 10 Germany Berlin"
}
]
}


Or 

http://localhost:8080/api/rag?question=What%20is%20capital%20of%20USA

Local LLM translates the USA to a United States country here.
```
or
```bash
http://localhost:8080/api/rag?question=What%20is%20capital%20of%20Aussi

{

"question": "What is capital of Aussi",

"answer": "Canberra is the capital of Australia.",

"sources": [

{ 1 key }

]
}

```