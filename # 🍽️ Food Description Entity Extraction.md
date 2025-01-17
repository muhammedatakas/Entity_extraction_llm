# 🍽️ Food Description Entity Extraction with LLMs

This project demonstrates how to extract structured information from food descriptions using Large Language Models (LLMs). It processes unstructured food descriptions to identify entities like brands, categories, ingredients, and more.

## 🌟 Key Features

- Comprehensive text preprocessing with abbreviation handling
- LLM-based entity extraction using Together AI
- Batch processing with rate limiting
- Extensive data quality analysis
- Result validation and error handling
- Processing pipeline for large datasets

## 🚀 Getting Started

### Prerequisites

```bash
pip install together pandas tqdm ratelimit concurrent-futures
```

### Configuration

1. Get your API key from [Together AI](https://together.ai)
2. Create a `.env` file and add your API key:
```
TOGETHER_API_KEY=your_api_key_here
```

### Data Structure

The system extracts the following entities:
- Brand
- Category
- Sub-Category
- Ingredients
- Preparation Methods
- Cultural Origin
- State
- Additional Features

### Running the Pipeline

1. Place your raw food descriptions CSV in `data/raw_food_descriptions.csv`
2. Open and run `text_classification_with_llm.ipynb`
3. Check output in `data/` directory

## 📊 Output Format

```json
{
    "Brand": "commercial_brand or null",
    "Category": "base_category",
    "Sub-Category": "product_type",
    "Ingredients": ["base_components"],
    "Preparation Method": ["cooking_methods"],
    "Cultural Origin": "geographic_origin or null",
    "State": "physical_state or null",
    "Additional Features": ["modifiers_and_attributes"]
}
```


