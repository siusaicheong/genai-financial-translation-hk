# Online Appendix: Example 7 - Iterative Translation Revision

## Discussion

LLMs can refine an initial draft through iterative, conversational prompting. In this process, the model reviews and revises its previous output, particularly to align with a specified style. Building on the previous example, the model was asked to revise its translation to match HKEX style.

The model adjusted the translation for HKEX style. The revisions included switching to Traditional Chinese characters, replacing "宣布" with "公告", and using "附屬公司" for "subsidiaries" instead of "子公司". Such targeted, instruction-based revision can improve both efficiency and consistency in a domain where regulatory compliance is critical.

---

## Prompt and Model Output

### User Prompt:
> Revise the translation above to adopt the Hong Kong Stock Exchange style and terms—such as using Traditional Chinese characters and financial terminology/sentence patterns commonly used in Hong Kong. For specific terms, provide only the Chinese terms without including the original English.

### Model Output:
> Here's the revised translation, adopting Hong Kong Stock Exchange style (Traditional Chinese characters, HKEX terminology), with only the Chinese terms provided for specific financial terms:
>
> **Revised Translation:**
>
> XXX集團有限公司（「本公司」）董事會（「董事會」）謹此公告，本公司董事會將於二零二五年八月X日舉行會議，會議議程包括但不限於批准本公司及其附屬公司截至二零二五年六月三十日止六個月的中期業績，及考慮派發中期股息（如有）。
>
> **Key Terminology (as used in HKEX announcements - *without* the English):**
>
> * **集團有限公司:** 集團有限公司 (jítuán yǒuxiàn gōngsī) - Group Limited
> * **附屬公司:** 附屬公司 (fùshǔ gōngsī) - Subsidiaries
> * **中期業績:** 中期業績 (zhōngqí yèjì) - Interim Results
> * **中期股息:** 中期股息 (zhōngqí gǔxī) - Interim Dividend
> * **公告:** 公告 (gōnggào) - Announcement (preferred over 宣布 in HKEX context)
> * **議程:** 議程 (yìchéng) - Agenda
> * **二零二五年:** 二零二五年 (èr líng èr wǔ nián) - 2025 (HKEX style uses full year numbers)
>
> **Changes & Rationale:**
>
> * **Traditional Characters:** The entire translation is now in Traditional Chinese characters, as required by the HKEX.
> * **公告 (gōnggào) instead of 宣布 (xuānbù):** "公告" is the standard term for an announcement in HKEX filings.
> * **附屬公司 (fùshǔ gōngsī) instead of 子公司 (zǐ gōngsī):** While both mean "subsidiary," 附屬公司 is the preferred term in HKEX documents.
> * **Full Year Numbers:** HKEX announcements typically write out years in full (e.g., 二零二五年 instead of 2025).
> * **議程 (yìchéng) for Agenda:** More common in formal HKEX announcements than other terms for agenda.
> * **Sentence Structure:** Minor adjustments to sentence flow to align with typical HKEX announcement phrasing. The overall structure remains similar to the original for clarity.
> * **Removed Parenthetical English:** As requested, the English terms are *not* included in parentheses. The assumption is the audience is familiar with the standard HKEX financial terminology.
>
> This revised translation is now much closer to the style and terminology you would find in an official announcement published by a company listed on the Hong Kong Stock Exchange.
