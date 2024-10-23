# Test Implementation Guide
## Small-Scale Validation of the Source Text Identification System

### Overview
We'll set up a minimal test environment using two philosophical texts to validate our system's core functionality. This test will help us:
1. Verify the technical implementation
2. Assess the quality of connections identified
3. Evaluate processing time and resource requirements
4. Identify potential issues before full-scale deployment

### Recommended Test Texts
For an ideal initial test, we should use:
1. A source text and its known translation OR
2. Two texts with established philosophical connections

Suggested pairs:
- Aristotle's De Anima (Greek) + Al-Fārābī's commentary on it (Arabic)
- OR -
- Al-Fārābī's Mabādiʾ + the Tehran manuscript you identified

### Step-by-Step Test Implementation

```python
import asyncio
import json
from pathlib import Path
from test_source_identification import (
    PhilosophicalCorpusManager,
    SourceTextIdentifier,
    ResultsAnalyzer
)

async def run_test():
    # 1. Set up test database
    test_db_config = {
        "dbname": "phil_test_db",
        "user": "test_user",
        "password": "test_password",
        "host": "localhost"
    }
    
    # 2. Initialize test environment
    corpus_manager = PhilosophicalCorpusManager(test_db_config)
    await corpus_manager.setup_database()
    
    # 3. Load test texts
    test_texts = [
        {
            "path": "test_data/text1.txt",
            "metadata": {
                "title": "De Anima",
                "author": "Aristotle",
                "date": "4th century BCE",
                "language": "Greek"
            }
        },
        {
            "path": "test_data/text2.txt",
            "metadata": {
                "title": "Commentary on De Anima",
                "author": "Al-Farabi",
                "date": "10th century CE",
                "language": "Arabic"
            }
        }
    ]
    
    # 4. Process texts
    text_ids = []
    for text in test_texts:
        text_id = await corpus_manager.process_text(
            text["path"],
            text["metadata"]
        )
        text_ids.append(text_id)
    
    # 5. Run analysis
    identifier = SourceTextIdentifier(test_db_config)
    results = await identifier.analyze_text(text_ids[1])  # Analyze second text
    
    # 6. Generate report
    analyzer = ResultsAnalyzer()
    report = await analyzer.generate_report(results)
    
    return report

# Run test
if __name__ == "__main__":
    report = asyncio.run(run_test())
    print(report)
```

### Test Setup Instructions

1. **Create Test Database**
```sql
CREATE DATABASE phil_test_db;
```

2. **Prepare Test Data Directory**
```bash
mkdir test_data
# Copy your two test texts into this directory
```

3. **Create Test Configuration**
```bash
# config.json
{
    "openai_api_key": "your-api-key",
    "test_db_config": {
        "dbname": "phil_test_db",
        "user": "test_user",
        "password": "test_password",
        "host": "localhost"
    }
}
```

4. **Run Test Script**
```bash
python test_source_identification.py
```

### Evaluation Metrics

1. **Connection Accuracy**
```python
def evaluate_connections(results, known_connections):
    """
    Compare identified connections with known relationships
    """
    true_positives = set(results) & set(known_connections)
    false_positives = set(results) - set(known_connections)
    false_negatives = set(known_connections) - set(results)
    
    precision = len(true_positives) / len(results)
    recall = len(true_positives) / len(known_connections)
    
    return {
        "precision": precision,
        "recall": recall,
        "f1_score": 2 * (precision * recall) / (precision + recall)
    }
```

2. **Processing Metrics**
```python
import time
from memory_profiler import profile

@profile
async def measure_performance(text_path, metadata):
    start_time = time.time()
    
    # Process text
    corpus_manager = PhilosophicalCorpusManager(test_db_config)
    text_id = await corpus_manager.process_text(text_path, metadata)
    
    # Run analysis
    identifier = SourceTextIdentifier(test_db_config)
    results = await identifier.analyze_text(text_id)
    
    end_time = time.time()
    
    return {
        "processing_time": end_time - start_time,
        "text_length": len(open(text_path).read()),
        "memory_usage": "See memory_profiler output"
    }
```

### Expected Output Example

```json
{
    "analysis_results": {
        "semantic_matches": [
            {
                "source_text": "De Anima",
                "similarity_score": 0.85,
                "matching_concepts": [
                    "soul definition",
                    "faculty psychology",
                    "perception theory"
                ]
            }
        ],
        "structural_matches": [
            {
                "argument_pattern": "definition-division-example",
                "confidence": 0.92
            }
        ],
        "translation_pairs": [
            {
                "greek_term": "ψυχή",
                "arabic_term": "نفس",
                "confidence": 0.95
            }
        ]
    },
    "performance_metrics": {
        "processing_time_seconds": 45.2,
        "memory_usage_mb": 256,
        "api_calls": 12
    }
}
```

### Test Validation Checklist

- [ ] Database successfully created and populated
- [ ] Texts properly processed and embedded
- [ ] Connections identified match known relationships
- [ ] Processing time within acceptable limits
- [ ] Memory usage within bounds
- [ ] API costs tracked and reasonable
- [ ] Output format clear and useful

### Common Issues and Solutions

1. **Memory Issues**
```python
# Add batch processing for large texts
async def process_large_text(text_path, chunk_size=1000):
    with open(text_path) as f:
        while chunk := f.read(chunk_size):
            await process_chunk(chunk)
```

2. **API Rate Limiting**
```python
# Add exponential backoff
async def api_call_with_retry(func, max_retries=3):
    for i in range(max_retries):
        try:
            return await func()
        except RateLimitError:
            await asyncio.sleep(2 ** i)
```

### Next Steps After Successful Test

1. Analyze test results
2. Adjust parameters based on performance
3. Consider scaling to larger text set
4. Document any identified issues
5. Plan full implementation

Would you like me to:
1. Provide a specific text pair for testing?
2. Create a more detailed evaluation framework?
3. Develop additional test scenarios?
4. Add more sophisticated metrics?
