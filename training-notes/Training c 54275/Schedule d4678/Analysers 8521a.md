# Analysers

T: 2:15-2:45
Time: June 22, 2021 10:15 AM-10:45 AM

Purpose of an analyser is to convert a string into a list of normalised tokens to appear in the inverted index.

### [Anatomy](https://www.elastic.co/guide/en/elasticsearch/reference/current/analyzer-anatomy.html#analyzer-anatomy-tokenizer)

- Character filters
- Tokenizers (only 1)
    - Tokenization
        - Tokenization enables matching on individual terms, but each token is still matched literally.
        - So that "Quick brown fox" can be searched with "quick fox" and "box brown"
- Token filters. (normalise)
    - Normalization
        - text analysis can normalize these tokens into a standard format.

### [Build-in analyzers](https://www.elastic.co/guide/en/elasticsearch/guide/current/analysis-intro.html#_built_in_analyzers)

- Standard analyzer
    - Character filters = removes most punctuation
    - Tokenizers = word boundaries
    - Token filters = lowercases the terms
- Simple analyzer
    - Tokenizers = splits the text on anything that isn’t a letter
    - lowercases the terms
- [Language analyzers](https://www.elastic.co/guide/en/elasticsearch/reference/current/analysis-lang-analyzer.html)
    - [English analyzer](https://www.elastic.co/guide/en/elasticsearch/reference/current/analysis-lang-analyzer.html#english-analyzer)
    

### Exercise

- Demonstrate `_analyze` endpoint
- Recommend creating the index and testing a query
- There is not a single correct answer
- Demonstrate difference in searches between `standard` and `english`
    - query `burger` works in `english` but not `standard`