# Phrase match queries

T: 3:15-3:30
Time: June 22, 2021 11:15 AM-11:30 AM

## Exercise 2 explanation

**What happens if the analyzer removes the stopwords? Would** `match_phrase` **still work?**

Answer: The short answer is yes,

```
# 1. Specify an analyzer that removes the stop words
PUT test
{
  "mappings": {
    "properties": {
      "title": {
        "type": "text",
        "analyzer": "english"
      }
    }
  }
}

# Index a document which get turned into "The car is the money" => ["car", "money"]
PUT test/_doc/1
{
  "title": "time is money"
}

# Query using `match_phrase`. "The car the is money" => ["car", "money"] which matches the indexed document
GET test/_search
{
  "query": {
    "match_phrase": {
      "title": "time is money"
    }
  }
}

# This doesn't work even though the tokens contains both "car" and "money" because it's not in the right order (["money", "car"] doesn't match ["car", "money"])
GET test/_search
{
  "query": {
    "match_phrase": {
      "title": "time on money"
    }
  }
}

```