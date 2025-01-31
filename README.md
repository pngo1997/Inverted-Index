# 🔍 Information Retrieval: Positional Index, TF-IDF, and Inverted Index  

## 📜 Overview  
This project focuses on key **Information Retrieval (IR)** tasks, including:  
1. **Positional Indexing** – Phrase query searching using a positional index.  
2. **TF-IDF Weighting & Cosine Similarity** – Calculating term weights and identifying relevant documents.  
3. **Inverted Index Construction** – Indexing TED Talk descriptions for efficient retrieval.  

📌 **Datasets Used**:  
- **Positional Index Sample Data** (Manually provided).  
- **Document-Term Matrix** (For TF-IDF calculations).  
- **TED Talks Dataset (`ted_main.csv`)** – Extracting and processing text descriptions.  

📌 **Programming Language**: `Python 3`  
📌 **Libraries Used**: `NLTK`, `NumPy`, `pandas`, `math`, `csv`  

## 🏷️ 1️⃣ Positional Index & Phrase Query Matching  
- **Queries Evaluated**:  
  - `"fools rush in"`  
  - `"fools rush in" AND "angels fear to tread"`  
- **Task**: Identify matching documents and positions from a given **positional index**.  
- **Issue Identified**: The index may have inconsistencies affecting search accuracy.  

## 🔢 2️⃣ TF-IDF Computation & Cosine Similarity  
- **Task**: Compute **TF-IDF** weights.
- **Cosine Similarity**: Determine the most relevant document: cos(θ) = (A • B) / (||A|| ||B||)
- **Goal**: Rank document similarity based on weighted term importance.

## 🔎 3️⃣ Inverted Index Construction (TED Dataset)  
- **Preprocessing**: Tokenization, Lowercasing, Stopword Removal, Stemming.  
- **Index Output Files**:  
1. `TED_term_index.csv` – Term-to-ID mapping with document frequency.  
2. `TED_doc_index.csv` – Document-to-ID mapping (TED Talk URLs).  
3. `TED_inverted_index.csv` – Term ID → (Doc ID, Term Frequency).  
- **Query Processing**: Boolean AND retrieval for:  
- `'climate' AND 'change'`  
- `'climate' AND 'fuel'`  
- `'artificial' AND 'intelligence'`  
- `'giant' AND 'troll'`  
