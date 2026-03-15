# Clariti Assistant

WhatsApp AI assistant built using:

- n8n (workflow automation)
- WAHA (WhatsApp HTTP API)
- Groq LLM (Llama 3.3 70B)
- Docker

## Architecture

WhatsApp
↓
WAHA
↓
n8n Webhook
↓
AI Agent
↓
Groq LLM
↓
WAHA sendText

## Workflow Backup

n8n workflows are exported from the container and stored in:

workflows/

Example command used:

docker exec n8n n8n export:workflow --all --separate --output=/tmp/workflows
docker cp n8n:/tmp/workflows ~/chat-agent/

## Server Setup

Server: Domainesia VPS  
Containers:

- n8n
- WAHA

Ports:

- n8n → 5678
- WAHA → 3000

## Purpose

This repository stores:

- n8n workflow backups
- documentation for the chatbot system
