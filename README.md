# Reflective AI Chart Generator

A Python-based agentic AI project that uses OpenAI models to generate, evaluate and refine data visualisations through the **Reflection design pattern**.

## Overview

The project demonstrates how feedback from a vision-capable LLM can improve AI-generated visualisations.

Using a coffee sales dataset, the system compares total sales in Q1 2024 and Q1 2025, evaluates the resulting chart and generates improved Python code.

## Workflow

**Generate → Execute → Reflect → Refine**

1. **Generate:** An OpenAI model generates Python charting code from a natural-language instruction and dataset schema.
2. **Execute:** Reviewed Python code produces the initial chart using Pandas and Matplotlib.
3. **Reflect:** An OpenAI vision-capable model evaluates the chart and suggests improvements.
4. **Refine:** The feedback guides the generation of revised charting code, which is reviewed before creating the improved chart.

## Technologies

- Python 3.12
- OpenAI API (`gpt-4o-mini`)
- Pandas and Matplotlib
- Jupyter Notebook
- Python-dotenv

## Getting Started

Clone the repository and navigate to the `chart-generation` directory.

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

Create a `.env` file containing:

```dotenv
OPENAI_API_KEY=your_openai_api_key
```

Open `reflective_chart_generator.ipynb` in Jupyter or VS Code and run the cells sequentially.

**Note:** An OpenAI API key with available credit is required. API calls may incur charges.

## Results

The workflow produces two visualisations:

- `coffee_sales_initial.png` — Initial bar chart.
- `coffee_sales_refined.png` — Revised chart with improved labels and formatting.

The example illustrates how LLM-generated feedback can guide iterative improvements in data visualisation.

## Limitations and Future Work

The current implementation requires manual review and execution of generated code. It is therefore a demonstration of the reflection pattern rather than a fully autonomous agent.

Future improvements could include isolated code execution, automated validation, structured evaluation criteria and multiple reflection cycles.

## Acknowledgement

Inspired by the *DeepLearning.AI Agentic AI* course. The notebook has been adapted and simplified for independent learning and experimentation.