# Supplementary Materials for "Generative AI for Financial Translation: Opportunities and Challenges in Hong Kong"

This repository contains the online appendix and supplementary materials for the book chapter:

> **SIU Sai Cheong. (Forthcoming). "Generative AI for Financial Translation: Opportunities and Challenges in Hong Kong."**

The materials provided here are intended to enhance the chapter's practical examples, promote transparency, and allow for the replication of the use cases discussed.

---

## Repository Contents

This repository is organized as follows:

- **[`model-card.md`](./model-card.md)**: Provides details on the primary language model used for the examples (Gemma 3 27B Instruct), including its intended use and observed limitations.

- **[`toy_tm.tmx`](./toy_tm.tmx)**: A small, sample Translation Memory eXchange (TMX) file used for the semantic TM enhancement examples. This file can be imported into any standard CAT tool.

- **`/examples`**: This directory contains detailed, unabridged walkthroughs for each use case presented in the chapter. Each file includes the full user prompt and the complete, unedited model output.

  - [`example-01-financial-term-analysis.md`](./examples/example-01-financial-term-analysis.md)
  - [`example-02-terminology-extraction.md`](./examples/example-02-terminology-extraction.md)
  - [`example-03-complex-text-analysis.md`](./examples/example-03-complex-text-analysis.md)
  - [`example-04-document-summarisation.md`](./examples/example-04-document-summarisation.md)
  - [`example-05-source-text-qa.md`](./examples/example-05-source-text-qa.md)
  - [`example-06-initial-draft-generation.md`](./examples/example-06-initial-draft-generation.md)
  - [`example-07-iterative-revision.md`](./examples/example-07-iterative-revision.md)
  - [`example-08-draft-synthesis.md`](./examples/example-08-draft-synthesis.md)
  - [`example-09-quality-assurance.md`](./examples/example-09-quality-assurance.md)
  - [`example-10-conventional-term-extraction.md`](./examples/example-10-conventional-term-extraction.md)
  - [`example-11-llm-term-extraction.md`](./examples/example-11-llm-term-extraction.md)
  - [`example-12-conventional-tm-failure.md`](./examples/example-12-conventional-tm-failure.md)
  - [`example-13-llm-semantic-tm.md`](./examples/example-13-llm-semantic-tm.md)
  - [`example-14-instructional-drift.md`](./examples/example-14-instructional-drift.md)
  - [`example-15-reasoning-failures.md`](./examples/example-15-reasoning-failures.md)
  - [`example-16-persona-prompting.md`](./examples/example-16-persona-prompting.md)
  - [`example-17-translation-brief.md`](./examples/example-17-translation-brief.md)
  - [`example-18-one-shot-prompting.md`](./examples/example-18-one-shot-prompting.md)
  - [`example-19-chain-of-thought.md`](./examples/example-19-chain-of-thought.md)

---

## How to Use This Repository

Readers of the chapter can use these materials to:

1.  **Review the Full Examples:** Navigate to the `/examples` directory to view the complete, unabridged prompts and outputs for each use case discussed in the main text.
2.  **Replicate the Findings:** Copy the prompts from the Markdown files and use them with the specified model (or other models) to test the techniques.
3.  **Explore the Translation Memory:** Download the `toy_tm.tmx` file and import it into a CAT (Computer-Assisted Translation) tool to explore the data used in the semantic matching example.

---

## Citation

If you use the materials or code from this repository in your research, please cite the original book chapter.

---

## Contact and Feedback

For any questions or feedback regarding these materials, please feel free to open an issue in this repository or contact the author at `siusaicheong@gmail.com`.
