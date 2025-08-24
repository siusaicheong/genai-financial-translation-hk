# Online Appendix: Example 12 - Conventional TM

## Discussion

Conventional TMs typically use fuzzy matching algorithms based on string similarity to calculate match scores. However, these algorithms may fail to recognise semantic similarity between sentences that use different wording but share the same meaning. For instance, when seeking a TM match for the input "The company's stock price fell", a conventional TM may assign a higher score to the semantically opposite "The company's stock price rose" than to the semantically similar "The company's stock price plummeted", simply because of fewer character differences. This limitation is even more pronounced with paraphrases that are structurally different but maintain similar meaning, such as "The company experienced a significant drop in its stock price."

---

## Results

### Table 12.1: Examples of conventional string-based TM similarity

| Candidate (Input sentence: "The company's stock price fell.") | Score |
| :--- | :--- |
| The company's stock price rose. | 83.9% |
| The company's stock price plummeted. | 75.7% |
| The company experienced a significant drop in its stock price. | 32.3% |
