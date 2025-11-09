
# Financial Insights Chatbot with Azure OpenAI

## Project Goal

The goal of this project is to build a **data analysis chatbot application** that leverages **Azure OpenAI Services** to extract meaningful insights from complex 10-Q financial documents. This chatbot empowers investment analysts by transforming dense, multi-page reports into accessible, conversational insights—enabling faster, more informed decision-making in high-pressure environments.

By implementing **Retrieval-Augmented Generation (RAG)** and utilizing **GPT-4**, the chatbot can answer questions about financial performance, business operations, risk factors, and management commentary with precision and context-awareness.

---

## Project Overview

Imagine you're a data analyst at a fast-paced investment firm. Each quarter, you're handed a stack of 10-Q filings—hundreds of pages of financial data and corporate disclosures. Your task: extract key insights quickly and accurately.

This project solves that challenge by creating a smart assistant that:
- Understands complex financial language
- Retrieves relevant sections from 10-Q documents
- Provides conversational answers using Azure OpenAI's GPT-4
- Streamlines the data analysis workflow

---

## Retrieving Source Data: Starbucks 10-Q Filings

This project uses **10-Q financial documents** from Starbucks Corporation as the source data for analysis. These quarterly filings are publicly available through the **SEC's EDGAR database** and contain detailed financial performance, risk factors, and management discussions.

### Steps to Download 10-Q Documents

1. **Access the SEC EDGAR Database**  
   Visit the [SEC Search Filings page](https://www.sec.gov/search-filings)  
   Enter `Starbucks` and click on CIK 0000829224

3. **Filter by Filing Type**  
   After retrieving the filings, use the filter to select **"10-Q"** under the "Filing Type" category.

4. **Select the Main Filing**  
   Click on the 1-2 most recent 10-Q filing.  
   In the **"Documents"** tab, choose the main 10-Q document.

5. **Choose HTM Format**  
   Open the document in **HTM** format and from the Menu in the top left-hand corner and **Open as HTML**. Then save to `.pdf` format using Print to PDF.

6. **Upload to Azure Blob Storage**  
   Use Azure Blob Storage to store the documents 

---

## Setting Up the Azure Environment

You'll need to configure the following Azure services:

1. **Resource Group**  
   A container that holds related resources for your Azure solution.
	
2. **Azure Blob Storage**  
   To store the 10-Q documents.
	
3. **Azure AI Search**  
   To index and search the documents.

4. **Azure OpenAI Service**  
   To deploy language models GPT-4 and ADA (text-embedding-ada-002) for embeddings.
