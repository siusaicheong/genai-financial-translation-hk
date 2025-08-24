# Online Appendix: Example 9 - Quality Assurance and Post-Translation Review

## Discussion

Beyond generating and refining drafts, LLMs can support quality assurance (QA) by reviewing and polishing the final target text before delivery. Prompting an LLM to systematically review a target text for specific error categories – such as numerical inaccuracies or stylistic inconsistencies – enables it to complement established approaches to translation QA.

This is especially important in financial translation, where accuracy and precision in numerical data are paramount, as a single misreported digit can have significant consequences. Manually cross-referencing figures between the source and target texts is tedious and error-prone; an LLM can facilitate this QA task. For example, the model was given an English financial text (concerning the net profit of a company) and its flawed Chinese translation, which contained significant numerical errors, and was asked to correct the translation.

The source text contained the figures "US$20 million" and "US$2 million", which were incorrectly rendered in the Chinese translation. The model detected the "significant error in the numbers" and produced a corrected version. It not only adjusted the figures but also explained conventions for writing numbers in Chinese and thus demonstrated a degree of numerical reasoning beyond simple pattern matching. Through such cross-checking, LLMs can serve as proofreading assistants and allow human translators to focus on higher-level aspects of QA that require human expertise and judgement, such as interpreting ambiguous content, ensuring appropriateness in sensitive contexts, fulfilling regulatory compliance requirements, and providing final regulatory certification.

---

## Prompt and Model Output

### User Prompt:
> Given the following financial text in English:
>
> The board of directors of the Company (Board) wishes to inform the shareholders and potential investors of the Company that the Company is expected to record a net profit after tax attributable to equity holders for the half year ended 30 June 2025 of approximately US$20 million, as compared to the net profit after tax attributable to equity holders of US$2 million recorded for the half year ended 30 June 2024.
> 
> Here is a Chinese translation:
>
> 公司董事會（董事會）謹此告知公司股東及潛在投資者，公司預計截至 2025 年 6 月 30 日的半年歸屬於股東的稅後淨利潤約為 200 萬美元，而截至 2024 年的半年歸屬於股東的稅後淨利潤為 20 萬美元。
>
> Correct the Chinese translation above.

### Model Output:
> The Chinese translation has a significant error in the numbers. "200 萬美元" (200 wan USD) translates to 2 million USD, and "20 萬美元" (20 wan USD) translates to 200,000 USD. The original English states $20 million and $2 million.
>
> Here's the corrected Chinese translation:
>
> **公司董事會（董事會）謹此告知公司股東及潛在投資者，公司預計截至 2025 年 6 月 30 日的半年歸屬於股東的稅後淨利潤約為 2000 萬美元，而截至 2024 年 6 月 30 日的半年歸屬於股東的稅後淨利潤為 200 萬美元。**
>
> Here's a breakdown of the changes:
>
> * **200 萬美元** changed to **2000 萬美元** (20 million USD)
> * **20 萬美元** changed to **200 萬美元** (2 million USD)
>
> **Explanation of "萬" (wan):**
>
> * "萬" means ten thousand.
> * Therefore, "2000 萬" (2000 wan) means 2000 * 10,000 = 20,000,000 (20 million).
> * "200 萬" (200 wan) means 200 * 10,000 = 2,000,000 (2 million).
> * "20 萬" (20 wan) means 20 * 10,000 = 200,000 (200 thousand).
