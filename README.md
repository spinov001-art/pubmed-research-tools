# pubmed-research-tools

Python toolkit for PubMed E-utilities API — search 36M+ biomedical papers, track publication trends, monitor new research. Free, no API key needed.

## Quick Start

```python
import requests

# Search PubMed for recent papers
params = {
    "db": "pubmed",
    "term": "machine learning drug discovery",
    "retmax": 10,
    "sort": "date",
    "retmode": "json"
}
r = requests.get("https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi", params=params)
ids = r.json()["esearchresult"]["idlist"]
print(f"Found {len(ids)} papers: {ids}")
```

## Features

- **Search** 36M+ papers by keyword, author, journal, date range
- **Fetch** abstracts, metadata, MeSH terms, citations
- **Track** publication trends over time
- **Monitor** new research in any field (daily/weekly)
- **Export** results to CSV, JSON, or pandas DataFrame
- **No API key** required (10 req/sec without key, 100 req/sec with free NCBI key)

## Use Cases

| Use Case | How |
|----------|-----|
| Literature review | Search by topic + date range |
| Trend analysis | Count papers per year by keyword |
| Author tracking | Monitor specific researchers |
| Drug research | Search clinical trials + outcomes |
| Meta-analysis | Bulk fetch abstracts for NLP |

## Related Projects

- [awesome-web-scraping-2026](https://github.com/spinov001-art/awesome-web-scraping-2026) — 77 free scraping tools & APIs (9 ⭐)
- [nasa-apis-python-examples](https://github.com/spinov001-art/nasa-apis-python-examples) — NASA API examples
- [free-security-apis-toolkit](https://github.com/spinov001-art/free-security-apis-toolkit) — Security APIs toolkit
- [OpenAlex tutorial](https://dev.to/0012303/openalex-api-search-250m-research-papers-for-free-no-api-key-needed-dkm) — Search 250M research papers

## Author

[Alex Spinov](https://dev.to/0012303) | [Portfolio](https://spinov001-art.github.io) | Spinov001@gmail.com

## License

MIT
