# Nova Retail – AI Operations Manager

A multi-agent AI assistant for a small shop. Ask questions in plain English and a team of 8 agents analyses the sales, stock, customer feedback and supplier documents, then answers and proposes actions.

**Nothing is ever sent or ordered automatically.** Every action is a proposal that a person approves or rejects.

## What it does

- Sales: best and worst sellers, revenue, units, orders
- Stock: which products might run out and what to reorder
- Feedback: what customers complain about
- Documents: answers from supplier and policy PDFs, with page citations
- Priorities and weekly report: the most urgent actions

## How it works

A router sends your question to the right agents. They analyse the data in parallel, a coordinator combines the findings, and a verifier re-checks every number before the answer is shown. **Python does the maths, and the AI only explains it in words.**

## How to run

1. Open `NOVA_OPS_Final_Project.ipynb` in Google Colab.
2. Set **Runtime ▸ Change runtime type ▸ T4 GPU**.
3. Click **Runtime ▸ Run all** and open the Gradio link at the end.

## Example questions

- What were my best-selling products last month?
- Which products risk running out of stock?
- What are customers complaining about most?
- What are my three most urgent business actions?

## Built with

Python, LangGraph, Qwen2.5-3B, SQLite, Gradio
