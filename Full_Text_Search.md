# FULL TEXT SEARCH

### Full Text Search:
Full-text search is the most common technique used in Web search engines and Web pages. A full-text search is a comprehensive search method that compares every word of the search request against every word within the document or database. Full-text search reduces the hassle of searching for a word in huge amounts of metadata, such as the World Wide Web and commercial-scale databases. Full-text search became popular in the late 1990s when the Internet began to become a part of everyday life.

### Lucene:
Apache Lucene is a free, open-source, high-performance, full-featured text search engine library written entirely in Java. It was initially written over 10 years ago by Doug Cutting. It is a technology suitable for nearly any application that requires full-text search, especially cross-platform.

#### Features of Lucene:
 1. **Powerful, Accurate and Efficient Search Algorithms:** It has ranked searching algorithms and many powerful query types like phrase queries, wildcard queries, proximity queries, range queries, and more.
 
 1. **Cross-Platform:** It can run on any platform which supports Java and indexes, and are portable across platforms. Developers can build an index on Linux and copy it to a Microsoft Windows machine and search it there.
 
 1. **Complete query capabilities:** Lucene has features of searching query through keyword, Boolean and +/- queries, proximity operators, wildcards, fielded searching, term/field/document weights, find-similar, spell-checking, multi-lingual search, and more.
 
### Solr:
Apache Solr (stands for Searching On Lucene w/ Replication) is a free, open-source search engine based on the Apache Lucene library. It was created by Yonik Seely in 2004 to add search capabilities to the company website of CNET Networks. it is also used as a document-based NoSQL database with transactional support that can be used for storage purposes and even a key-value store. Solr is enterprise-ready, fast, and highly scalable. The applications built using Solr are sophisticated and deliver high performance.

#### Advantages: 

 1. **High Scalability:** With tools such as Apache ZooKeeper, it is easy to scale Solr up or down, as it relies heavily on automated index replication, distribution, load-balancing, and automated failover and recovery.
 
 1. **Flexibility:** Solr is highly flexible. According to the need of the organization, Solr can be deployed in any kind of system (big or small) such as standalone, distributed, cloud, etc.
 
 1. **Multilingual Support:** Solr can work in several other languages such as Chinese, Japanese, Korean, Arabic, German, French, Spanish, and many others. It has language detection built-in and provides language-specific text analysis tools accordingly.
 
 1. **Text-Centric and Sorted by Relevance:** It is optimized for searching natural-language text, like emails, web pages, resumes, PDF documents, and social messages such as tweets or blogs. It returns documents in ranked order based on how relevant each document is to the user's query.
 
 1. **Large volumes of documents:** It is designed to deal with indexes containing many millions of documents.
 
#### Disadvantages:
 1. **Data Store:** We can bot use solr as a primary data store. Only useful as Secondary Data Store. It is not an ACID-compliant Data Store.
 
 1. **Transactions:** Solr does not offer support for transactions and distributed transactions.
 
 1. **Normalised Data:** It is not optimal for Normalized Data.

### Elasticsearch:
Elasticsearch is an open-source and distributed search and analytics engine built on Apache Lucene and developed in Java. It was released in 2010 and has quickly become the most popular search engine and is commonly used for log analytics, full-text search, security intelligence, business analytics, and operational intelligence use cases. It is a real-time distributed and analytic engine that helps in performing various kinds of search mechanisms. It can achieve fast search responses because, instead of searching the text directly, it searches an index instead. Additionally, it supports full-text search which is completely based on documents instead of tables or schemas.

#### Advantages: 

 1. **Scalable:** Elasticsearch is distributed document-oriented that making it easy to scale up in a large organization. The biggest advantage of Elasticsearch is that it can be scalable across multiple nodes. So eventually, We can start with a single node or two or three nodes, If the workload grows, you can scale across multiple nodes. So, more instances can be added to a cluster whenever needed.
 
 1. **Performance:** By using distributed inverted indices, Elasticsearch quickly finds the best matches for your full-text searches from even very large data sets. It also caches almost all of the structured queries commonly used as a filter for the result set and executes them only once. For every other request containing a cached filter, it checks the result from the cache.
 
 1. **Document Oriented:** Elasticsearch is document-oriented, which does not use schemas and tables to store data. It stores all the data in a document form and JSON Format. It is simple, concise, and easy to read.
 
 1. **Multilingual:** Elasticsearch is multilingual means it is available in various languages. So, the people of different regions can use it in their languages.
 
 1. **Autocompletion and Instant Search:** It automatically provides suggestions to complete queries. The completion suggester provides autocomplete/search-as-you-type functionality. This is a navigational feature to guide users to relevant results as they are typing, which results in improving search precision.
 
 1. **NEAR REAL-TIME OPERATIONS:** Elasticsearch operations such as reading or writing data usually take less than a second to complete. This lets you use Elasticsearch for near real-time use cases such as application monitoring and anomaly detection.
 
 #### Disadvantages:
 
 1. **Language constraint:** To handle the requests and responses, Elasticsearch doesn't have multi-language support. It supports only a JSON format whereas Apache Solr supports CSV, XML as well JSON format.
 
 1. **SSD's requirement:** Elasticsearch needs a group of servers having 64GB of RAM to work efficiently. If we use too many small servers, it creates overhead or if we use a few powerful servers, there is a chance of failover. However, SSDs are more expensive, which creates the infrastructure overpriced.
 
 1. **Well-organized:** To run the queries correctly, you need to take care of a hierarchy of indexes, IDs, and types. Besides this, you also need to ensure the status of all nodes must be 'green' and not 'yellow'. When there is less data, then you can organize the cluster manually. But on a large scale, you need to organize data and infrastructure effectively.
 
### Conclusion:
By going through all this we come to know that each of the Engine has its advantages and disadvantages depending on the use case:

Talking about **Apache Lucene** both *Solr* and *Elasticsearch* are based on Apache Lucene, so both Solr and Elasticsearch have full features of Lucene. Consider Lucene as a Linux system and Solr and Elasticsearch as Ubuntu, we get all the features of Lucene and additional features of each of the engines and are also user-friendly.

Now, Let's see use cases of both the engines so that we can analyze where we will get the most out of each:
 
##### Use Cases for Solr:
 
1. If the data is mostly static and needs full precision for data analysis and very fast performance one should look at Solr because of its caches and the ability to use an uninverted reader for faceting and sorting, for example, E-Commerce.
1. Apache Solr is a mature project with a large and active development and user community behind it, as well as the Apache brand so it is very reliable.

##### Use cases for Elasticsearch:

1. Elasticsearch is better suited and much more frequently used for time-series data use cases, like log analysis use cases.

1. Elasticsearch was young and built on more modern principles, aimed at modern use cases, and was built to make the handling of large indices and high query rates easier.

1. Companies that didn't work on search engines to date and hadn’t invested a lot of time, money, and energy in its adoption, integration, etc can go with it.

1. Companies that had to deal with large volumes of data and needed to more easily shard and replicate data (search indices) and shrink or grow their search cluster.

### References:
1. https://towardsdatascience.com/an-overview-on-elasticsearch-and-its-usage-e26df1d1d24a
1. https://aws.amazon.com/opensearch-service/the-elk-stack/what-is-elasticsearch/
1. https://sematext.com/guides/solr/
1. https://www.tutorialspoint.com/apache_solr/apache_solr_overview.htm
1. https://lucene.apache.org/core/
