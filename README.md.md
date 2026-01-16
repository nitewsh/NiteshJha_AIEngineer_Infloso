# LLM-Based Text Summarization Assignment

## Candidate Information
- **Name:** Nitesh Jha  
- **Role Applied:** AI Engineering – LLM  
- **Company:** Infloso  

---

## Project Overview
This project implements an end-to-end **Large Language Model (LLM) based text summarization pipeline** to analyze user reviews and automatically generate meaningful insights.

The solution:
- Produces balanced summaries of positive and negative user feedback
- Extracts the most important reviews using TF-IDF
- Evaluates summarization quality using ROUGE metrics
- Is designed to run stably in CPU-only environments

---

## Dataset Description
- Input dataset: `reviews.txt`
- Each line represents one user review
- Total reviews: 100
- Reviews contain informal, real-world user feedback

Dataset was provided as part of the assignment.

---

## Approach & Methodology

### 1. Data Exploration
- Loaded reviews into a Pandas DataFrame
- Verified dataset size and structure
- Inspected sample reviews to understand text quality

### 2. Data Preprocessing
- Converted text to lowercase
- Removed URLs, special characters, and extra spaces
- Created a cleaned version of each review for analysis

### 3. Sentiment Separation
- Used a keyword-based heuristic to split reviews into:
  - Positive reviews
  - Negative reviews
- This ensures balanced summarization and avoids bias

### 4. Summarization Strategy
- Used the pretrained **facebook/bart-large-cnn** model
- Applied abstractive summarization
- Implemented text chunking to handle long inputs
- Forced CPU execution for stability and reproducibility

### 5. Important Review Extraction
- Used TF-IDF to calculate importance scores
- Selected top 5 most informative reviews across the dataset

### 6. Evaluation
- Used ROUGE-L metric to evaluate summary quality
- Sample-based evaluation due to dataset size
- ROUGE-L provides overlap-based quality measurement

---

## Results
- Generated balanced positive and negative summaries
- Extracted top 5 important user reviews
- Saved outputs as:
  - `final_summary.txt`
  - `top_5_reviews.csv`
- Achieved an average ROUGE-L score for summary evaluation

---

## Technologies Used
- Python
- Hugging Face Transformers
- PyTorch
- Pandas, NumPy
- Scikit-learn
- ROUGE Score
- Google Colab

---

## How to Run the Project

1. Open the Google Colab notebook using the link below
2. Upload `reviews.txt` to Google Drive
3. Update the dataset path if required
4. Run all cells sequentially

---

## Google Colab Notebook
👉 **[Paste your public Google Colab link here]**

---

## Future Improvements
- Use a trained sentiment classifier instead of heuristics
- Fine-tune the summarization model on domain-specific data
- Add topic-wise or aspect-based summarization
- Incorporate human evaluation for summary quality
- Support multilingual reviews

---

## Conclusion
This project demonstrates a practical and scalable application of LLMs for real-world text summarization. The solution prioritizes clarity, stability, and interpretability while delivering meaningful insights from user-generated content.
