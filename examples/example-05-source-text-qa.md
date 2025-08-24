# Online Appendix: Example 5 - Source Text Quality Assessment

## Discussion

A professional translator's responsibilities include identifying and flagging ambiguities, inconsistencies, or obvious errors in the source text that could affect translation quality, in line with industry best practices. LLMs can assist with this stage of quality assurance, particularly in detecting inconsistencies. In the following example, the model was presented with an excerpt from a financial text about the announcement of interim results for a Group and asked to review the text for factual errors.

The source text contained a factual issue concerning the chronology of the announcement: a financial results announcement for a period ending on 30 June was made before the end of May. The LLM identified this as a "Date Discrepancy/Logical Inconsistency", observing that "This is logically impossible. Financial results cannot be finalised and announced before the period they cover has ended." This type of logical reasoning supports the accuracy and reliability of translated information.

---

## Prompt and Model Output

### User Prompt:
> Review the following financial document to be translated and identify any factual issue(s) or error(s) that the translator needs to clarify with the source text author, if any.
>
> Details of the Group's financial performance will be disclosed in the interim results announcement of the Group for the six months ended 30 June 2025, which is expected to be published before the end of May 2025.

### Model Output:
> Okay, here's a review of the provided financial document snippet, focusing on potential issues a translator needs to clarify *before* translating:
>
> **Potential Factual Issue/Error & Clarification Needed:**
>
> * **Date Discrepancy/Logical Inconsistency:** The document states the financial performance is *for the six months ended 30 June 2025*, but the announcement is expected *before the end of May 2025*. This is logically impossible. Financial results *cannot* be finalized and announced *before* the period they cover has ended.
>
> **Why this is a problem for a translator:**
>
> * **Accuracy is paramount:** Financial translation *must* be accurate. Translating this as-is would perpetuate a clear error.
> * **Potential Legal/Compliance Issues:** Incorrect dates in financial reporting can have serious legal and compliance ramifications. The translator doesn't want to contribute to that.
> * **Understanding Intent:** The translator needs to understand *what* the author intended to convey. Was it a typo? Was the date for the announcement meant to be *after* the end of May?
>
> **What the translator needs to ask the source text author:**
>
> "Regarding the dates in this statement: The document states the financial performance is for the period ending June 30, 2025, but the announcement is expected before May 31, 2025. This appears to be a discrepancy. Could you please confirm the correct date for the announcement? Is the period ending June 30, 2024, instead of 2025?"
>
> **In summary:** The translator should **absolutely** flag this date issue with the author before proceeding with the translation. It's a critical factual error that needs resolution.
