# Web Graph Analysis — Wikipedia Crawl

### 📌 Goal  
Explore the structure of a web-based network by crawling Wikipedia articles and building a directed graph. The project identifies **important nodes** using multiple centrality measures.

### 🧑‍🤝‍🧑 Stakeholder  
- Researchers & educators interested in **network science**.  
- Digital librarians and platform engineers who want to **understand which pages/articles are most influential** in knowledge graphs.  

### ❓ Question  
Which Wikipedia articles are structurally “important” in the graph of related topics (Data Science, Machine Learning, Artificial Intelligence)?  

### ⚙️ Methods
- Crawled ~120 Wikipedia articles using `requests` + `BeautifulSoup`.  
- Built a **directed graph** (`DiGraph`) in NetworkX where:  
  - **Nodes** = Wikipedia articles.  
  - **Edges** = hyperlinks from one article to another.  
- Analyzed importance using:  
  - **In-degree centrality** (popularity by incoming links).  
  - **PageRank** (Google’s algorithm for influence).  
  - **Betweenness centrality** (bridges between clusters).  

### 📊 Results (Top Nodes)
- **By In-Degree**: `Main_Page`, `Machine_learning`, `Data_mining`  
- **By PageRank**: `Main_Page`, `Machine_learning`, `Regression_analysis`  
- **By Betweenness**: `Data_mining`, `Cluster_analysis`, `Regression_analysis`  

### 📷 Figures  
- `fig_indegree_distribution.png`  
- `fig_top_in_degree.png`  
- `fig_top_pagerank.png`  
- `fig_top_betweenness.png`  

### 📑 Tables  
- `table_summary_top25.csv` → overview of top nodes across metrics.  
- `table_top_in_degree.csv`  
- `table_top_pagerank.csv`  
- `table_top_betweenness.csv`  

### ✅ Validation
- Sanity checked crawl: skipped non-article namespaces (`Category:`, `Help:`, etc.).  
- Removed duplicate links.  
- Verified NetworkX metrics against small test graphs from class exercises.  

### ⚠️ Limitations
- Crawl capped at **120 pages** → not the full Wikipedia.  
- Bias toward **seed pages** (Data Science, Machine Learning, AI).  
- Results reflect structural importance only — not necessarily topical importance.  

### 📂 Repo Structure
- **web_graph_analysis.ipynb** – Main notebook  
- **README.md** – Project documentation  
- **requirements.txt** – Python dependencies  
- **figs/** – Output plots  
- **tables/** – Output CSV summaries  

### ▶️ How to Run
# Install dependencies
pip install -r requirements.txt

# Run in Jupyter Notebook
jupyter notebook web_graph_analysis.ipynb

# OR run in Jupyter Lab
jupyter lab web_graph_analysis.ipynb
