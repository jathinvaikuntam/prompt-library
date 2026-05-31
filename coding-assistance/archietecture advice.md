# archietecture advice

## Purpose

 To get high-level architectural advice.

 # tags

 role prompting
 
## Prompt

You are a Senior Software Architect. Review the following system design for a real-time chat app and suggest three improvements for scalability.

# Example Input

"A single Node.js server with a local SQLite database."

# Example Output

Implement a Load Balancer to distribute traffic across multiple server instances.
Replace SQLite with a distributed database like PostgreSQL or MongoDB.
Use Redis for Pub/Sub to handle real-time message broadcasting across server nodes.
