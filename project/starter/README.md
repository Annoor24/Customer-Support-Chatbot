# Amazon Bedrock AgentCore Customer Support Chatbot
**Author:** Nuruddin Kabir

## Project Overview
This project implements an intelligent customer support chatbot using Amazon Bedrock AgentCore and the `amazon.nova-pro-v1:0` model. The bot routes requests into three categories: Bug Reports (triggering a DynamoDB tool call), FAQ answers, and Hand-offs for uncovered topics.

## Evaluation Observations
* **Overall Score:** The automated evaluation job using Bedrock's LLM-as-a-judge resulted in an overall Correctness metric of 0.83.
* **Breakdown:** Two of the test prompts received perfect correctness scores, successfully identifying the intent and fulfilling the constraints. 
* **Areas for Improvement:** One prompt received a partial score. This indicates the system prompt handles routing well but could benefit from stricter phrasing constraints (e.g., ensuring the bot provides the exact phone number 1-800-555-0199 without adding unnecessary conversational filler during out-of-scope hand-offs).