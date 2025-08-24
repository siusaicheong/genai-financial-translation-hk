# Online Appendix: Example 4 - Document Summarisation and Analysis

## Discussion

A high-level overview of a long text is valuable for comprehension and translation alike. LLMs can produce concise summaries that provide such overviews. For example, the model was given a text about a sub-tenancy agreement and its impact on financial reporting and listing rules, and was prompted to provide a summary and explanation of key points.

The LLM delivered a multifaceted summary. It explained the sub-tenancy agreement, outlined the financial impact, clarified the listing rule significance, and noted that the sub-tenancy arrangement qualifies as "a disposal of an asset". Such summaries can help financial translators quickly orient themselves and understand lengthy documents, thereby supporting source text comprehension.

---

## Prompt and Model Output

### User Prompt:
> Summarise and explain the key points of the following financial text:
>
> SUB-TENANCY AGREEMENT
> >
> On XX July 2025, XXX Limited (as sub-landlord) entered into a Sub-Tenancy Agreement with YYY Limited (as sub-tenant), pursuant to which XXX Limited agreed to sublet the premises to YYY Limited for a term commencing from XX July 2025 to XX March 2027 (both days inclusive).
>
> LISTING RULES IMPLICATIONS

> The Sub-Tenancy Agreement triggered the Company to de-recognise the right-of-use assets for the head lease under the Head Tenancy Agreement, and at the same time, recognise the value of the lease receivable and a net gain in connection with the sublease of the premises under the Sub-Tenancy Agreement. Accordingly, the transaction under the Sub-Tenancy Agreement is regarded as a disposal of asset by the sub-landlord for the purpose of the Listing Rules.

### Model Output:
> ### Summary of the Financial Text: Sub-Tenancy Agreement & Listing Rules
>
> This text describes a **sub-tenancy agreement** and its impact on the financial reporting of the company (XXX Limited). Here's a breakdown of the key points:
>
> * **What happened:** XXX Limited (the original tenant - now a *sub-landlord*) rented a property to YYY Limited (the *sub-tenant*) through a sub-tenancy agreement. This agreement is valid from July 2025 to March 2027.
> * **Key Financial Impact:** This sub-letting isn't just a simple rental agreement; it has significant accounting consequences. Because of this agreement, XXX Limited had to:
>     * **Remove (de-recognise) an asset from its books:** Specifically, the "right-of-use asset" related to their original lease (the "Head Tenancy Agreement"). This asset represented their rights to use the property under the original lease.
>     * **Add new assets & profit:** They now *recognise* a "lease receivable" (the money they'll receive from YYY Limited) *and* a "net gain" – meaning they made a profit on the sublease.
> * **Listing Rules Significance:** Crucially, this transaction is considered a **disposal of an asset** according to the "Listing Rules" (likely rules governing publicly traded companies). This means it's a significant event that needs to be reported and potentially reviewed by regulatory bodies.
>
> **In simpler terms:**
>
> Imagine XXX Limited leased an office. They then decided to rent *part* of that office to another company, YYY Limited. Because they're now effectively passing on their rights to use the space, they have to adjust their financial records. They no longer show the full value of the original office lease on their books, but instead show the money they're receiving from YYY Limited and any profit made from the arrangement. This is a big enough deal that it needs to be reported to regulators.
>
> **Why is this important?**
>
> This highlights how subleasing can have complex accounting implications. It's not just about collecting rent; it affects a company's reported assets, liabilities, and profits, and requires compliance with relevant financial regulations.
