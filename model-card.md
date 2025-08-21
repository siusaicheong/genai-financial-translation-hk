# Model Card: Gemma 3 27B Instruct

This model card provides information about the primary large language model used for the examples in the chapter "Generative AI for Financial Translation: Opportunities and Challenges in Hong Kong".

---

## Model Details

- **Model Name:** Gemma 3 27B Instruct
- **Model Type:** A 27-billion parameter, instruction-tuned, open-source large language model.
- **Developed By:** Google
- **Official Model Card:** For comprehensive details on the model's architecture, training data, and evaluation, please refer to the [official Google model card](https://ai.google.dev/gemma/docs/model_card_3).

---

## Intended Use in This Chapter

The Gemma 3 27B Instruct model was selected for the use cases in this chapter for the following reasons:

1.  **High Performance:** It demonstrates strong capabilities in translation and reasoning tasks suitable for the financial domain.
2.  **Open Source:** Its open-source nature allows for greater transparency and academic study.
3.  **Suitability for Local Deployment:** As a model of this size can be run on-premise with appropriate hardware (especially when quantized), it serves as a practical example for organizations in the financial sector where data security and confidentiality are paramount.

The primary use case is to demonstrate the potential applications and limitations of modern LLMs when integrated into a professional financial translation workflow.

---

## Limitations Demonstrated in This Chapter

As shown in the chapter, while powerful, this model is not without limitations. Users should be aware of the following issues, which were observed during testing:

- **Potential for Hallucination:** The model can generate factually incorrect information (e.g., fabricating names, titles, or facts), especially when compared to smaller models in the same family. Even at this scale, it made subtle, domain-specific terminology errors.
- **Instructional Drift:** In long, multi-turn conversations, the model may fail to adhere to instructions provided in earlier prompts, leading to inconsistencies.
- **Limited Reasoning:** The model can exhibit failures in deep, multi-step logical and numerical reasoning, sometimes missing obvious errors or making incorrect assumptions.

**Conclusion:** The use of this model, like any LLM in a high-stakes domain, requires rigorous human oversight, verification, and post-editing to ensure accuracy and reliability.
