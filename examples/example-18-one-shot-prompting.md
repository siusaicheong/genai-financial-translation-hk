# Online Appendix: Example 18 - One-Shot and Few-Shot Prompting

## Discussion

One-shot (or few-shot) prompting provides concrete examples of the desired style, leveraging the in-context learning capability of LLMs. For financial reports with standardised formats, translators can include previously published content in prompts to enhance output consistency.

As an example, a new press release concerning Hong Kong's foreign currency reserve assets was first translated using a zero-shot prompt (with no example). The translation was generally accurate, but differences in phrasing and formatting were evident. The translated title included the word "公布" (released), resulting in "香港最新外匯儲備資產數字公布", whereas the official Chinese version omits "公布".

The model was then asked to translate the same text again, this time using a previously published bilingual release as a style exemplar. As a result, the LLM produced output closely matching the official version, replicating both the phrasing and the numerical formatting. This outcome highlights the effectiveness of one-shot prompting in achieving brand or style consistency.

---

## Prompt and Model Output

### User Prompt (Zero-Shot):
> Translate the following text from English into Traditional Chinese:
>
> Hong Kong's Latest Foreign Currency Reserve Assets Figures Released
> The Hong Kong Monetary Authority (HKMA) announced today (7 July) that the official foreign currency reserve assets of Hong Kong amounted to US$431.9 billion as at the end of June 2025 (end-May 2025: US$431.1 billion) (Annex).
> Including unsettled foreign exchange contracts, the foreign currency reserve assets of Hong Kong at the end of June 2025 amounted to US$431.8 billion (end-May 2025: US$431.0 billion).
> The total foreign currency reserve assets of US$431.9 billion represent over five times the currency in circulation or about 37% of Hong Kong dollar M3.

### Model Output (Zero-Shot):
> Here's the translation of the text into Traditional Chinese:
>
> **香港最新外匯儲備資產數字公布**
>
> 香港金融管理局（金管局）今日（7月7日）公布，截至2025年6月底，香港的官方外匯儲備資產為4319億美元（2025年5月底：4311億美元）（附件）。
>
> 連同未結算的外匯合約，香港於2025年6月底的外匯儲備資產為4318億美元（2025年5月底：4310億美元）。
>
> 4319億美元的外匯儲備資產總額，超過流通貨幣五倍，或約佔香港貨幣供應M3的37%。
>
> **Notes on the translation:**
>
> * **香港金融管理局 (Hong Kong Monetary Authority):** This is the standard and official translation.
> * **金管局 (HKMA):** This is a common abbreviation used in Chinese media.
> * **外匯儲備資產 (Foreign Currency Reserve Assets):** This is the standard translation.
> * **未結算 (Unsettled):** Accurately conveys the meaning of contracts that haven't been finalized.
> * **流通貨幣 (Currency in Circulation):** Standard translation.
> * **M3:** Generally kept as "M3" in Chinese financial reporting.
> * **附件 (Annex):** Standard translation.
> * Dates are kept in the same format as the original for clarity.

### User Prompt (One-Shot):
> Task: Please translate the following new press release about Hong Kong's foreign currency reserve assets into Traditional Chinese (zh-HK). Your translation must strictly follow the style, terminology, and formatting of the provided example from a previous month.
>
> Example of a Previously Published Translation (Reference Text):
>
> Source English:
> Hong Kong's Latest Foreign Currency Reserve Assets Figures Released
> The Hong Kong Monetary Authority (HKMA) announced today (6 June) that the official foreign currency reserve assets of Hong Kong amounted to US$431.0 billion as at the end of May 2025 (end-April 2025: US$410.2 billion) (Annex).
> Including unsettled foreign exchange contracts, the foreign currency reserve assets of Hong Kong at the end of May 2025 amounted to US$430.9 billion (end-April 2025: US$409.4 billion).     
> The total foreign currency reserve assets of US$431.0 billion represent over five times the currency in circulation or about 38% of Hong Kong dollar M3.
>
> Target Chinese (zh-HK):
> 香港最新外匯儲備資產數字
> 香港金融管理局（金管局）今日（6月6日）公布，香港於2025 年5月底的官方外匯儲備資產為4,310億美元（2025年4月底為4,102億美元）（附件）。
> 連同未交收外匯合約在內，香港於2025年5月底的外匯儲備資產為4,309億美元（2025年4月底為4,094億美元）。
> 為數4,310億美元的外匯儲備資產總額，相當於香港流通貨幣5倍多，或港元貨幣供應M3約38%。
>
> New Text to Translate:
> Hong Kong's Latest Foreign Currency Reserve Assets Figures Released
> The Hong Kong Monetary Authority (HKMA) announced today (7 July) that the official foreign currency reserve assets of Hong Kong amounted to US$431.9 billion as at the end of June 2025 (end-May 2025: US$431.1 billion) (Annex).
> Including unsettled foreign exchange contracts, the foreign currency reserve assets of Hong Kong at the end of June 2025 amounted to US$431.8 billion (end-May 2025: US$431.0 billion).
> The total foreign currency reserve assets of US$431.9 billion represent over five times the currency in circulation or about 37% of Hong Kong dollar M3.
>
> Please provide the translation for the New Text to Translate, ensuring it matches the pattern seen in the reference text.

### Model Output (One-Shot):
> 香港最新外匯儲備資產數字
> 香港金融管理局（金管局）今日（7月7日）公布，香港於2025年6月底的官方外匯儲備資產為4,319億美元（2025年5月底為4,311億美元）（附件）。
> 連同未交收外匯合約在內，香港於2025年6月底的外匯儲備資產為4,318億美元（2025年5月底為4,310億美元）。
> 為數4,319億美元的外匯儲備資產總額，相當於香港流通貨幣5倍多，或港元貨幣供應M3約37%。
