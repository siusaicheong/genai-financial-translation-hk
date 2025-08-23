# Online Appendix: Example 1 - Financial Term Analysis

## Discussion

Financial texts often contain highly specific terms with significant legal or accounting implications. An LLM can act as an on-demand knowledge resource and provide immediate expert clarification of a given term or phrase. In this example, when prompted to explain the key expression “unaudited consolidated management accounts for the six months ended 30 June 2025” from a financial announcement, the model broke it down into its components. It clarified that “unaudited” means the accounts “have not been independently verified by an external auditor” and that “consolidated” refers to accounts covering both the main company and all entities controlled by the group concerned. The model not only conveyed the surface meaning but also highlighted financial nuances that junior translators might overlook, such as the distinction between management accounts and financial reports for external stakeholders. This complements conventional glossaries, which typically depend on the translator’s context analysis to select relevant term explanations and may not cover complex, multi-part terms as seen in this example.

---

## Prompt and Model Output

### User Prompt:
> Given the financial text below:
>
> The Board would like to inform the shareholders of the Company (the “Shareholders”) and potential investors that, based on the preliminary assessment of the Group’s unaudited consolidated management accounts for the six months ended 30 June 2025 and the information currently available to the Board, the net profit of the Group for the six months ended 30 June 2025 is expected to record an increase in the approximate range of XX% to YY% as compared to the net profit of the Group for the six months ended 30 June 2024 as disclosed in its 2024 interim report. Such increase was primarily due to the increase in the Group’s revenue as driven by the increase in sales orders from the data centre in the cable assembly sector.
>
> Explain the term “unaudited consolidated management accounts for the six months ended 30 June 2025” in the above context.

### Model Output:
> Let's break down "unaudited consolidated management accounts for the six months ended 30 June 2025":
>
> * **Six months ended 30 June 2025:** This specifies the *period* the financial information covers – the first half of the year 2025 (January 1st to June 30th).
>
> * **Management Accounts:** These are financial reports prepared *internally* by the company's management team for their own use in making decisions. They are not prepared with the same level of detail or scrutiny as reports intended for external stakeholders (like shareholders). They focus on providing a snapshot of performance *during* the period, helping management understand what's happening *now*.
>
> * **Consolidated:** This means the accounts aren't just for the main company ("the Company") but include the financial results of all the entities that the Group *controls* (its subsidiaries). It presents the financial performance as if the entire Group were a single entity.
>
> * **Unaudited:** This is the crucial part. "Unaudited" means these accounts have *not* been independently verified by an external auditor. An auditor's job is to provide an objective opinion on whether the financial statements present a true and fair view of the company's financial position. Because these accounts are unaudited, they are considered *preliminary* and subject to change. They are based on the best information available *at this time*, but haven't had the rigorous examination of a full audit.
>
> **In summary:** "Unaudited consolidated management accounts for the six months ended 30 June 2025" are internal, preliminary financial reports combining the results of all companies within the Group for the first half of 2025, and they haven't been officially checked by an independent auditor. The Board is using these *early* figures to give shareholders an *initial* indication of how the company is performing.
