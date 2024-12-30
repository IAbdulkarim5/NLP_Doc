# **Document Retriever from Web-Scraped Dataset**
![logo](deployment/invest.eye.png)

## **Project Overview**
This project demonstrates the creation of a **Document Retrieval System** that dynamically extracts, processes, and retrieves company information from the **Public Investment Fund (PIF)** website. The system supports efficient querying and retrieval of relevant information using various retrieval methods, with an evaluation of their effectiveness.

---

## **Problem Statement**
Investors often face challenges in finding and evaluating relevant information about companies, especially in large datasets or on websites like the **Public Investment Fund (PIF)**. Browsing and gathering relevant data manually is time-consuming and inefficient, leading to delayed or poorly informed investment decisions.

---

## **Motivation**
To empower investors with a tool that provides quick, reliable, and accurate access to essential information about PIF companies. By automating the extraction and retrieval process, we aim to simplify research efforts and enhance decision-making capabilities for investors.

---

## **Solution**
The **Document Retrieval System** leverages data scraping, text preprocessing, and retrieval algorithms to create an efficient search tool. The system dynamically collects company descriptions from the PIF website and uses advanced retrieval methods to display the most relevant information based on user queries. Its integration with Streamlit ensures a smooth and user-friendly experience.

---

## **App Features**
- **Search Bar**: Type a company name, keyword, or investment plan to find related information instantly.
- **Relevance Score**: Each result includes a match percentage to help you gauge its relevance to your query.
- **Source Context**: Results indicate the source company or investment plan title for better understanding.
- **Real-Time Performance**: Immediate and accurate results tailored to your queries.
- **User-Friendly Interface**: A simple and intuitive design powered by Streamlit.

---

## **Future Enhancements**
1. **Semantic Search Integration**: Enhance the system with a semantic search model for deeper contextual understanding and more accurate results.
2. **Financial Insights**: Add detailed financial data and performance metrics for each company to aid in investment decisions.
3. **Global Expansion**: Expand the dataset to include companies and investments beyond the PIF for broader applicability.

---

## **Technical Details**
### **1. Dynamic Data Scraping**
- Uses **Selenium** to loop through all pages of the PIF website, collecting company links and metadata.
- Extracts detailed company information (title and description) from individual pages.

### **2. Data Cleaning and Preprocessing**
- Removes special characters and converts text to lowercase for uniformity.
- Processes the scraped descriptions to remove noise and improve query matching.

### **3. Search System**
We implemented and compared three retrieval methods:

| **Method**            | **Advantages**                                    | **Limitations**                          |
|------------------------|--------------------------------------------------|------------------------------------------|
| TF-IDF (sklearn)       | Simple, efficient for small datasets             | Limited relevance for complex queries    |
| TfidfRetriever (Haystack) | Enhanced precision over basic TF-IDF             | Still lacks optimal ranking in some cases|
| BM25Retriever (Haystack) | Best accuracy and relevance ranking             | Slightly higher computational cost       |

**Result**: The **TF-IDF (sklearn)** method was chosen as the final retrieval algorithm because it was smooth to integrate with Streamlit. Unlike the other two methods, it did not face integration or version issues, which would have required downgrading the Streamlit version.

---

## **Access Invest.Eye**
Explore the tool here: [Invest.Eye](https://investeye.streamlit.app/)

---

## **Usage**
1. Clone the repository to your local system.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Start the Streamlit app by running:
   ```bash
   streamlit run app.py

---

## **Conclusion**
The **Document Retrieval System** efficiently retrieves relevant company information. Among the three methods tested, **TF-IDF (sklearn)** was identified as the most practical solution due to its seamless integration with Streamlit. It provides accurate and reliable results, making it a valuable tool for investors to explore and evaluate PIF companies and their plans.

---



