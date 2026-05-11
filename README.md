# Customer-support-workflow
This project is an AI-powered customer support automation workflow built in n8n. It automatically reads incoming Gmail emails, checks whether the email is related to customer support, generates an AI-based response using Gemini and Pinecone knowledge base, and replies back to the customer automatically.
1. Gmail Trigger
This node monitors the Gmail inbox and automatically starts the workflow whenever a new email is received.
2. Text Classifier
This node analyzes the email content and decides whether the email is a customer support request or just a normal/promotional email.
3. Google Gemini Chat Model (Classifier Model)
This Gemini model helps the Text Classifier understand the meaning of the email and classify it into the correct category.
4. AI Agent
This is the main brain of the workflow. It understands the customer issue, searches for relevant information, and prepares a professional response.
5. Google Gemini Chat Model (AI Agent Model)
This Gemini model powers the AI Agent and generates natural, human-like customer support replies.
6. Pinecone Vector Store
This node stores and retrieves business knowledge like FAQs, refund policies, product details, and support documents for accurate responses.
7. Embeddings Google Gemini
This node converts text and documents into vector embeddings so Pinecone can search and retrieve relevant information intelligently.
8. Add Label to Message
This node adds labels to processed emails in Gmail for better organization and tracking of support conversations.
9. Reply to a Message
This node automatically sends the AI-generated reply back to the customer through Gmail.
10. No Operation, do nothing
This node safely ends the workflow for emails that are not related to customer support.
