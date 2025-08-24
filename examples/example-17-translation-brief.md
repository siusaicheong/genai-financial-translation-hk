# Online Appendix: Example 17 - Providing a Detailed Translation Brief

## Discussion

Embedding a detailed translation brief in a prompt enables the translator to specify essential parameters for the task, such as background information, purpose, audience, and style. To illustrate, when a prompt simply instructed an LLM to translate an excerpt from an HKMA statistical release, the output was in Simplified Chinese, "HIBOR" was retained as an English acronym, and "best lending rates" was rendered in a way that did not conform to established Hong Kong financial terminology.

In a subsequent prompt, a comprehensive translation brief was supplied, specifying the translation was for an HKMA press release aimed at Hong Kong financial professionals, requiring Traditional Chinese, and calling for strict adherence to official HKMA terminology. The translation produced under these instructions was markedly more appropriate. It used Traditional Chinese characters, rendered key financial terms with precision (e.g., "HIBOR" was translated as "香港銀行同業拆息"), and adopted a formal, authoritative tone. This comparison demonstrates that a well-structured translation brief can transform a generic LLM translation into a polished, locally relevant, and publication-ready text.

---

## Prompt and Model Output

### User Prompt (Before Brief):
> Translate the following text into Chinese:
>
> The ratio of new mortgage loans priced with reference to HIBOR increased from 91.8% in April to 93.4% in May. The ratio of new mortgage loans priced with reference to best lending rates decreased from 2.3% in April to 1.9% in May.

### Model Output (Before Brief):
> 以下是翻译：
>
> **以HIBOR为参考定价的新按揭贷款比例从4月份的91.8%上升至5月份的93.4%。以最佳贷款利率为参考定价的新按揭贷款比例从4月份的2.3%下降至5月份的1.9%。**
>
> Here's a breakdown of the translation choices:
>
> * **HIBOR:** Generally kept as HIBOR in Chinese financial contexts.
> * **Best Lending Rates:** 最佳贷款利率 (zuì jiā dài kuǎn lì lǜ) - standard translation.
> * **Ratio:** 比例 (bǐ lì) - most common and accurate translation in this context.
> * **Increased/Decreased:** 上升 (shàng shēng) / 下降 (xià jiàng) - standard terms for increase/decrease.
> * **Mortgage Loans:** 按揭贷款 (àn jiē dài kuǎn) - standard translation.
> * **Priced with reference to:** 以...为参考定价 (yǐ...wéi cān kǎo dìng jià) - accurately conveys the meaning of being priced based on a benchmark.

### User Prompt (With Brief):
> Primary Goal: Translate an HKMA press release for Hong Kong financial professionals and the media. The translation must be formal, authoritative, and ready for immediate publication. Your explanation after translation should be concise.
>
> Source Text:
> "The ratio of new mortgage loans priced with reference to HIBOR increased from 91.8% in April to 93.4% in May. The ratio of new mortgage loans priced with reference to best lending rates decreased from 2.3% in April to 1.9% in May."
>
> Key Instructions:
> Language & Region: Use Traditional Chinese (繁體中文) with terminology and expressions standard in Hong Kong's financial sector.
> Tone: Formal, official, and objective. No colloquialisms.
> Terminology: Adhere strictly to official HKMA translations and established financial terms common in Hong Kong.
> Sentence Structure: This is a critical rule. To ensure readability, break down long sentences with commas. Aim for each clause (the text between commas) to be under 20 characters.
> Fluency: Where it sounds more natural in Chinese, use verbs instead of nouns.
> Conventions: Format all dates, numbers, and official titles according to Hong Kong standards.

### Model Output (With Brief):
> ## Translation:
>
> 「以香港銀行同業拆息 (HIBOR) 定價的新按揭貸款比例, 由四月份的 91.8%, 增至五月份的 93.4%。以最優惠利率 (P 利率) 定價的新按揭貸款比例, 則由四月份的 2.3%, 減至五月份的 1.9%。」
>
> ## Explanation:
>
> This translation prioritizes clarity and adherence to Hong Kong financial terminology. The original English sentences were broken down into shorter clauses separated by commas to improve readability in Chinese. "Priced with reference to" was translated using the standard verb phrase "以…定價" (yi…dingjia - priced at/with…). All terms (HIBOR, best lending rates) are rendered using their established Chinese equivalents commonly used in HKMA publications and financial news. Dates and numbers follow Hong Kong conventions.
