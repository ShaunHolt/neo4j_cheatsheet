# neo4j_cheatsheet

Just some helpful commands as I learn more about neo4j

### Wipe database
Although I'm not sure if this is the right way to do it:

```
MATCH (n)
DETACH DELETE n
```

### Creating the graph
To do until I can get the Mendeley API working

```
CREATE
(paper1:Paper {title: "Measuring justice in machine learning", author: "Lundgard, Alan", category: "justice", url: "http://arxiv.org/abs/2009.10050", location: "arxiv"}),
(paper2:Paper {title: "Qlib: An AI-oriented Quantitative Investment Platform", author: "Yang, Xiao", author: "Liu, Weiqing", author: "Zhou, Dong", author: "Bian, Jiang", author: "Liu, Tie-Yan", category: "investments", url: "http://arxiv.org/abs/2009.11189", location: "arxiv"}),
(paper3:Paper {title: "Knowledge-Aided Open-Domain Question Answering", author:"Zhou, Mantong", author:"Shi, Zhouxing", author:"Huang, Minlie", author:"Zhu, Xiaoyan", category: "open domain qa", url: "http://arxiv.org/abs/2006.05244", location: "arxiv"}),
(site1:Site {title: "The Annotated Transformer", category: "learning NLP", url: "https://nlp.seas.harvard.edu/2018/04/03/attention.html"})
```

### Returning subsets from the graph
MATCH (p:Paper)
WHERE p.category = "investments"
RETURN p

