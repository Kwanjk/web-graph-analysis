# Web Graph Analysis — Important Nodes (Wikipedia Demo)

This project builds a small directed graph of Wikipedia internal links and identifies important nodes via **in-degree**, **PageRank**, and **betweenness**.

## How to Run
1. Create/activate a Python environment.
2. `pip install -r requirements.txt`
3. Open `web_graph_analysis.ipynb` in Jupyter and run all cells.
4. Figures will be saved as PNG; tables saved as CSV.

## Stakeholder & Decisions
- Search/ranking engineers and community moderators.
- Use hubs (in-degree), authorities (PageRank), and bridges (betweenness) to inform ranking and monitoring.

## Data
- Pages are crawled from Wikipedia starting from seeds (Data_science, Machine_learning, Artificial_intelligence).
- Nodes = pages; edges = directed hyperlinks.

## Validation
- PageRank sum ≈ 1
- No negative centralities
- Non-empty graph assertions

## License
For educational use. Respect website terms and robots policies; keep crawl tiny.
