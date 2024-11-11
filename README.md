# README: AI Use Case Generation Project

## Project Overview
This project is designed to generate and collect AI use cases and relevant datasets for various industries. It comprises a comprehensive pipeline that scrapes industry data, generates AI use cases using NLP models, and collects relevant datasets from Hugging Face and Kaggle. The methodology integrates web scraping, NLP, and dataset collection to provide a holistic solution for industry-specific AI applications.

## Components

### 1. Environment Setup
- Install the required Python libraries:
  ```
  pip install transformers beautifulsoup4 requests cohere python-dotenv
  ```
- Connect to Google Drive to access secure API keys (e.g., `kaggle.json`).

### 2. API Key Management
- Use the `python-dotenv` package to manage API keys securely:
  ```python
  from dotenv import load_dotenv
  load_dotenv()
  ```

### 3. Core Agents
- **ResearchAgent**: Scrapes industry data using BeautifulSoup.
- **UseCaseGenerationAgent**: Uses Cohere’s API to generate AI use cases based on industry insights.
- **ResourceCollectorAgent**: Collects relevant datasets from Hugging Face and Kaggle.

### 4. Workflow
1. **Input**: User specifies an industry (e.g., “Steel”).
2. **ResearchAgent**: Conducts web scraping to gather industry-related information.
3. **UseCaseGenerationAgent**: Processes the industry data to generate potential AI use cases.
4. **ResourceCollectorAgent**: Retrieves supporting datasets from Hugging Face and Kaggle.
5. **Output**: Displays AI use cases and links to relevant datasets.

### 5. Running the Project
- Ensure all dependencies are installed and environment variables are set.
- Execute the main script:
  ```python
  python main_workflow.py
  ```

## Example Output
**Industry: Steel**

### AI Use Cases:
1. Supply Chain Optimization
2. Enhanced Quality Control
3. Predictive Maintenance
4. Energy Efficiency
5. Demand and Production Forecasting
6. Autonomous Processes
7. Health and Safety Insights

### Dataset Links:
- Hugging Face: [Steel Plates Data](https://huggingface.co/datasets/mstz/steel_plates)
- Kaggle: [Faulty Steel Plates](https://www.kaggle.com/uciml/faulty-steel-plates)

## Future Enhancements
- Integrate more data sources.
- Refine web scraping for more detailed data extraction.

## Architecture Flow
```
User Input --> ResearchAgent --> UseCaseGenerationAgent --> ResourceCollectorAgent --> Output
```

This flow ensures a seamless generation of industry insights and relevant datasets for AI solutions.

# AiPlanet
