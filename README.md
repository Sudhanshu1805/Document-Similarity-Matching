# Invoice Similarity Comparison

## Overview

This project compares invoices based on their text content and visual layout. It extracts text from PDF invoices, analyzes key features, and calculates similarities using three methods:

1. **Cosine Similarity**: Measures the cosine of the angle between feature vectors.
2. **Jaccard Similarity**: Measures the overlap between sets of keywords.
3. **Image Similarity**: Compares visual layouts of invoices.

The goal is to find the most similar invoice from a database of training invoices to a given test invoice.

## Requirements

- Python 3.6 or higher
- Libraries: `PyPDF2`, `re`, `numpy`, `scikit-learn`, `Pillow`, `scikit-image`

## Installation

You can install the required libraries using pip:

bash
```pip install PyPDF2 numpy scikit-learn Pillow scikit-image```

Code Overview
Cell 1: Import Required Libraries
This cell imports all necessary libraries used for text extraction, feature extraction, and similarity calculations.

Cell 2: Define Functions for Text Extraction and Feature Extraction
Defines functions to extract text from PDFs and features such as invoice number, date, amount, and keywords.

Cell 3: Define Functions for Calculating Similarity
Contains functions to compute:

Cosine Similarity: Between feature vectors.
Jaccard Similarity: Between sets of keywords.
Image Similarity: Between visual representations of invoices.
Cell 4: Extract Text and Features from Training PDFs
Extracts text and features from a set of training PDF invoices.

Cell 5: Extract Text and Features from Testing PDFs
Extracts text and features from a set of testing PDF invoices.

Cell 6: Store Training Data in In-Memory Database
Stores extracted features of training invoices in an in-memory database.

Cell 7: Define Function to Find the Most Similar Invoice
Defines a function that finds the most similar invoice in the database based on text and image similarity.

Cell 8: Find and Print the Most Similar Invoices for Test PDFs
Finds and prints the most similar invoices for each test PDF with similarity scores displayed as percentages.

Usage
Update File Paths: Ensure the pdf_directory and test_pdfs paths in the code are correct and point to the directories containing your PDF files.

Run the Code: Execute the cells sequentially in a Python environment (e.g., Jupyter Notebook).

View Results: The most similar invoice for each test PDF will be printed along with the similarity scores in percentage format.

Example Output
Most similar invoice to 'invoice_77098.pdf': invoice_3.pdf with similarity score 85.6789%
Most similar invoice to 'invoice_102857.pdf': invoice_1.pdf with similarity score 90.1234%
