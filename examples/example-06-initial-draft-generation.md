# Online Appendix: Example 6 - Initial Draft Generation

## Discussion

Generating a high-quality initial draft with a machine translation system can save considerable time and effort, and an LLM can be applied effectively for this purpose. In this example, the model received a sample financial announcement regarding a board meeting and was asked to produce an initial Chinese translation and briefly explain key terms used.

The model produced a Chinese draft in a formal, legalistic register suited to this type of document. Although the output was in Simplified Chinese, the tone and vocabulary matched those of official financial announcements. The model selected formal expressions such as "谨此宣布" for "announces" and appropriate financial terms, such as "中期业绩" for "interim results". This output demonstrates the model's ability to provide a coherent draft, allowing the translator to concentrate on post-editing and refinement.

---

## Prompt and Model Output

### User Prompt:
> Translate the following financial text into Chinese, providing a very brief explanation of key choices and terms.
>
> The board of Directors (the "Board") of XXX Group Limited (the "Company") announces that a meeting of the Board of the Company will be held on X August 2025 for the purpose of, inter alia approving the interim results of the Company and its subsidiaries for the six months ended 30 June 2025 and considering the payment of an interim dividend, if any.

### Model Output:
> Here's the translation, followed by explanations of key choices:
>
> **Chinese Translation:**
>
> XXX集团有限公司（"本公司"）董事会（"董事会"）谨此宣布，本公司董事会会议将于2025年8月X日举行，会议议题包括但不限于批准本公司及其子公司截至2025年6月30日止六个月的 interim results（中期业绩），并考虑派发 interim dividend（中期股息），如有的话。
>
> **Explanation of Key Choices & Terms:**
>
> * **XXX集团有限公司 ("本公司"):** "XXX Group Limited" is translated directly. The phrase in parentheses, "本公司" (běn gōngsī), means "this company" and is a standard way to define a company for repeated reference in formal Chinese documents. Using quotation marks around it establishes it as a defined term.
> * **董事会 ("董事会"):** "Board of Directors" is translated as 董事会 (dǒngshìhuì), which literally means "board of directors." Again, the quotation marks define it as a specific term.
> * **谨此宣布 (jǐn cǐ xuānbù):** This is a very formal way to say "hereby announces," common in official company announcements.
> * **Interim Results (中期业绩 - zhōngqí yèjì):** "Interim results" is commonly translated as 中期业绩. It's a standard financial term. Keeping the English term in parentheses is helpful for clarity, especially for those familiar with English financial reporting.
> * **Interim Dividend (中期股息 - zhōngqí gǔxī):** Similarly, "interim dividend" is translated as 中期股息. Again, the English term is included in parentheses.
> * **截至…止 (jiézhì…zhǐ):** This phrase means "as of/ended..." and is standard for reporting periods.
> * **如有的话 (rú yǒu de huà):** This translates to "if any" and is a common way to express contingency in Chinese.
> * **包括但不限于 (bāokuò dàn bù yǒuxiàn yú):** This translates to "including but not limited to" - a standard legal/formal phrasing.
>
> **Overall Style:**
>
> The translation aims for a formal, legalistic tone, appropriate for a company announcement. It uses standard Chinese financial terminology and maintains the structure of the original English text for clarity.
