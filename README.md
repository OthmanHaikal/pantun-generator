An AI-powered tool that generates and searches Malay Pantun, blending traditional poetry with modern machine learning.

Overview
The Pantun Generator is an innovative application that leverages AI to preserve and celebrate the cultural heritage of Malay poetry. Using a semantic search mechanism powered by Sentence Transformers and Faiss, users can explore a vast collection of Pantun based on themes or keywords.

Features:
Semantic Search: Find Pantun related to a given theme or keyword.
Cultural Significance: Focused on preserving Malay culture through traditional poetry.
Scalable and Fast: Supports large datasets with quick search capabilities using Faiss.
Interactive Querying: A user-friendly CLI for exploring Pantun based on user input.

## **How It Works**
1. **Data Loading:**
   - Pantun data is loaded from a structured text file, where each Pantun comprises four lines separated by blank lines.
   - The data is processed and stored in a structured CSV format.

2. **Embedding and Indexing:**
   - The `distiluse-base-multilingual-cased-v2` model from Sentence Transformers generates contextual embeddings for each Pantun.
   - A Faiss index is built for fast similarity searches.

3. **Interactive Querying:**
   - Users input a query or theme (e.g., "love" or "nature").
   - The tool returns the most semantically similar Pantun from the dataset.

## **Setup Instructions**
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/pantun-generator.git
   cd pantun-generator
   ```

2. **Install Dependencies:**
   Ensure Python is installed (version >= 3.8), then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application:**
   Start the interactive CLI:
   ```bash
   python main.py
   ```

## **Example Usage**
### Query:
```
Input: buatkan saya pantun tentang kasih sayang
```

### Output:
```
Layang - layang putus teraju,
Jatuh tersangkut di pokok delima,
Kasih sayang sudah setuju,
Tentu boleh berkekal lama.
```

## **Project Structure**
```
pantun-generator/
├── data/
│   └── pantun_cleaned.csv       # Cleaned Pantun data
├── embeddings/
│   └── faiss_index.bin          # Prebuilt Faiss index (optional)
├── scripts/
│   ├── data_preprocessing.py    # Data preparation script
│   ├── embedding_generator.py   # Generates embeddings using Sentence Transformers
│   └── semantic_search.py       # Implements the search functionality
├── main.py                      # CLI-based application entry point
├── README.md                    # Project documentation
└── requirements.txt             # Python dependencies
```

## **License**
This project is licensed under the MIT License. Feel free to use and contribute!

## **Acknowledgments**
Special thanks to the creators of Sentence Transformers, Faiss, and the Malay poetry community for inspiring this project.

---
