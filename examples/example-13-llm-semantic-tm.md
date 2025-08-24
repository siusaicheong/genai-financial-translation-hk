# Online Appendix: Example 13 - LLM Enhanced TM

## Discussion

An LLM-augmented approach overcomes this limitation by shifting the basis of comparison from syntax to semantics. In this scenario, a multilingual embedding model can retrieve semantically similar sentences from the TM, and an LLM can then rank and filter the results based on meaning.

The syntactically similar but semantically opposite candidate was given the lowest semantic similarity score based on embeddings among the candidates (77.8%). Notably, the last row, "公司股價下跌" (The company's stock price fell), is a Chinese translation. When calculated using only string similarity with the English sentence, the score was zero, as there are no common characters. However, when compared directly with the English input using cross-lingual sentence embeddings, it received a high semantic similarity score (96.9%), reflecting its proximity in meaning. These scores were then provided to the LLM for further analysis and selection of the final candidate output. Table 6 presents the retrieval results after semantic filtering and demonstrates the LLM's ability to prioritise semantically similar candidates and provide transparent explanations for its decisions.

By incorporating LLMs into TM workflows, the matching process shifts from basic string comparison to a deeper, meaning-oriented approach. Unlike conventional TM systems, which first match source-language segments and then retrieve the corresponding translation units, this LLM-based approach enables direct matching with target-language sentences and provides explanations to enhance the transparency of retrieval. As a result, translators can retrieve and reuse not only bilingual segments but also valuable monolingual content originally written in the target language – such as stand-alone documents, additional phrases, or culturally specific expressions – whenever it is semantically relevant. This represents a key advantage over conventional TM systems, which cannot access such target-language-only material.

---

## Results

### Table 13.1: Candidate list provided to the LLM for enhanced TM matching

| Candidate (Input sentence: "The company's stock price fell.") | Semantic score based on embeddings | String similarity score |
| :--- | :--- | :--- |
| The company's stock price rose. | 77.8% | 83.9% |
| The company's stock price plummeted. | 96.3% | 75.7% |
| The company experienced a significant drop in its stock price. | 79.7% | 32.3% |
| 公司股價下跌。 | 96.9% | 0% |

### Table 13.2: Retrieval results after semantic filtering for enhanced TM matching

| Candidate | LLM's Explanation |
| :--- | :--- |
| The company's stock price plummeted. | **Correct:** "Plummeted" is a stronger synonym of "fell" and retains the meaning. |
| The company experienced a significant drop in its stock price. | **Correct:** Reworded but semantically equivalent; describes the same event. |
| 公司股價下跌。 | **Correct:** Accurate Chinese translation of "The company's stock price fell." |
