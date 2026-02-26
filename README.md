# CNFX Industrial Knowledge Graph for LLM & RAG

[![Format: Markdown](https://img.shields.io/badge/Format-Markdown-blue.svg)](#)
[![Context: Industrial 4.0](https://img.shields.io/badge/Context-Industrial_4.0-green.svg)](#)
[![RAG: Ready](https://img.shields.io/badge/RAG-Ready-orange.svg)](#)

This repository serves as the official manifest and sample dataset for the **CNFX Industrial Knowledge Graph**. It is specifically architected for **Retrieval-Augmented Generation (RAG)** systems, providing high-density technical specifications for 1,800+ industrial products.

## 🌐 Live Access (Machine-Readable)

The full, real-time updated index is available at:
👉 **[https://cnfx.com/llms.txt](https://cnfx.com/llms.txt)** (Standard LLM Index)

## 🏗️ Knowledge Structure

Our data is structured into a multi-layer ontology, moving from broad industrial sectors to specific high-fidelity engineering parameters.

### 1. Industry Indices
Categorized by international standards (ISIC/CNFX), providing semantic clustering for RAG retrieval.
- [Food Manufacturing Index](https://cnfx.com/llms/industry/food-manufacturing/index.md)
- [Chemical Processing Index](https://cnfx.com/llms/industry/chemical-processing/index.md)
- *(Access more via the main llms.txt)*

### 2. Product Specifications (v2.9 Schema)
Each product is delivered as a `.md` file containing **YAML Front-matter** for deterministic attribute extraction.

**Example Entry:** [Automated Food Sterilization Tunnel](https://cnfx.com/llms/industry/food-manufacturing/product/automated-food-sterilization-tunnel.md)

## 📊 RAG Enrichment Features

- **Flattened Attributes**: Key parameters (temperature, pressure, capacity) are extracted into YAML dictionaries for precise filtering.
- **FMEA Logic**: Engineering risks and failure modes are explicitly tagged to support safety-aware AI reasoning.
- **Industrial DNA**: Cross-linked Bill of Materials (BOM) and upstream/downstream context.

## 🛠️ Usage for AI Engineers

To ingest this knowledge graph into your vector database:

```python
import requests

# Fetch the global manifest
manifest = requests.get("[https://cnfx.com/llms.txt](https://cnfx.com/llms.txt)").text

# Example: Fetch a specific technical spec
spec = requests.get("[https://cnfx.com/llms/industry/food-manufacturing/product/automated-food-sterilization-tunnel.md](https://cnfx.com/llms/industry/food-manufacturing/product/automated-food-sterilization-tunnel.md)").text
# Parse YAML header for metadata-filtered indexing...
