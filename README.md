# Mini_Search_Engine
- Search Ranking with BM25 (Best Matching 25) is a state-of-the-art probabilistic keyword ranking function used to estimate document relevance, serving as the default algorithm in modern search engines like Elasticsearch, Lucene, and Solr. It improves upon TF-IDF by incorporating term frequency saturation (diminishing returns on keyword frequency) and document length normalization (penalizing overly long documents), making it a, highly effective and efficient tool for information retrieval. 

Key elements in Mini-Search-Engine:
1. Data Crawler: Using BeautifulSoup to extract URLs, titles from website
2. Inverted Index: An inverted index is a data structure that maps keywords to documents. This data structure makes it trivial to find documents where a certain word appears. When a user searches for some query the inverted index is used to retrieve all the documents that match with the keywords in the query. To implement the inverted index, a defaultdict with the signature dict[str, dict[str, int]] is used to mapping that a given word (a str) returns another mapping from URL (a str) to the number of times that word appears in the URL (a int). The default value of the mapping is a mapping from URL to 0, so if we try to get the value of a keyword that doesn’t exist in a URL we get a zero.
3. Ranking:  A standard BM25 used to ranks documents based in the links.
