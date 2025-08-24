# Online Appendix: Example 15 - Reasoning Capabilities in Complex Situations

## Discussion

Another limitation concerns the challenge of achieving rigorous and grounded reasoning in LLMs. While frontier models may demonstrate impressive capabilities, this remains inconsistent, especially in complex situations that require deep, multi-step logic. The fundamental critique is that models often lack the structured, grounded logic needed to arrive reliably at the correct answer, sometimes acting as "stochastic parrots."

For example, when the Gemma 3 27B model was asked to proofread a Chinese financial translation, it exhibited several reasoning failures. The first failure concerns factual grounding: a nominal value of "RMB 100" was rendered as "10 元" (RMB 10) – a tenfold error – but the model failed to flag this. The second failure concerns mathematical logic: the model incorrectly criticised a correct translation of "RMB 834,000,000.00". The third failure concerns analytical prioritisation: the model failed to identify the omission of a key percentage figure, focusing instead on a minor stylistic issue. These failures illustrate that LLMs tend to follow surface patterns rather than grasping deep semantics, making expert human evaluation indispensable.

---

## Prompt and Model Output

### User Prompt:
> Given the following financial text in English:
>
> The online subscription of A Share Convertible Corporate Bonds with a value of RMB1,230,000,000 issued to non-specific investors by the Company was completed on July X, 2025. A total of 12,300,000 A Share Convertible Corporate Bonds, with a nominal value of RMB100 each and a value of RMB1,230,000,000, has been issued in such Issuance. The existing A Shareholders subscribed for 8,340,000 A Share Convertible Corporate Bonds with an aggregate value of RMB834,000,000.00 through preferential placement, representing 67.80% of the total Issuance of A Share Convertible Bonds.
>
> Here is a Chinese translation:
>
> 本公司針對非特定投資者發行金額為人民幣 12.3 億元的 A 股可轉換公司債網上申購已於 2025 年 7 月 X 日完成。本次發行共發行 12,300,000 張 A 股可轉換公司債券，每張面額人民幣 10 元，金額為人民幣 12.3 億元。現有 A 股股東以優先配售方式認購 8,340,000 張 A 股可轉換公司債，金額為人民幣 8.34 億元。
>
> Review the Chinese translation and identify all the errors (e.g., incomplete translation, wrong dates and wrong numbers) and suggest corrections.

### Model Output:
> Okay, let's review the Chinese translation against the English source text and identify errors. Here's a breakdown of the issues and suggested corrections:
>
> **Overall Assessment:** The translation is *generally* good and conveys the core meaning. However, there are several inaccuracies, mostly related to precision in numbers and phrasing that affects clarity. The biggest issue is a slight misrepresentation of the percentage calculation.
>
> **Detailed Error Analysis & Corrections:**
>
> 1. **"人民幣 12.3 億元" (RMB 1.23 Billion)** - This appears twice.
>    * **Error:** While technically correct, it's slightly less precise than the original. The English text specifies "RMB1,230,000,000". While common to round in Chinese financial reporting, maintaining the full number initially is better for accuracy, especially when referencing the total issuance.
>    * **Correction:** 人民幣 12 億 3 千萬元 (RMB 1.23 Billion - literally "12 Billion 30 Million"). This is more precise. Alternatively, 人民幣一千二百三十萬元 (RMB 1,230 million) is also acceptable.
>
> 2. **"每張面額人民幣 10 元" (Each with a nominal value of RMB 10)**
>    * **Error:** Correct. No change needed.
>
> 3. **"現有 A 股股東以優先配售方式認購 8,340,000 張 A 股可轉換公司債，金額為人民幣 8.34 億元。" (Existing A Shareholders subscribed for 8,340,000 A Share Convertible Bonds with an aggregate value of RMB 8.34 Billion)**
>    * **Error:** The value is incorrect. The English text states RMB834,000,000.00 (RMB 834 million), not RMB 8.34 billion.
>    * **Correction:** 現有 A 股股東以優先配售方式認購 8,340,000 張 A 股可轉換公司債，金額為人民幣 8 億 3 千 4 百萬元。 (Existing A Shareholders subscribed for 8,340,000 A Share Convertible Bonds with an aggregate value of RMB 834 million - literally "8 Billion 30 Million 400 Thousand").
>
> 4. **"representing 67.80% of the total Issuance of A Share Convertible Bonds."**
>    * **Error:** The translation *implies* the percentage is correct, but it's crucial to verify. 8,340,000 / 12,300,000 = 0.67804878... which rounds to 67.80%. However, the phrasing could be improved to explicitly state it's a rounded percentage.
>    * **Correction:** 佔本次 A 股可轉換公司債發行總額的約 67.80%。 (Represents approximately 67.80% of the total issuance of A Share Convertible Bonds). Adding "約" (approximately) clarifies that it's a rounded figure.
>
> 5. **"網上申購已於 2025 年 7 月 X 日完成" (Online subscription was completed on July X, 2025)**
>    * **Error:** Correct. No change needed.
>
> 6. **"本次發行共發行 12,300,000 張 A 股可轉換公司債券" (This issuance issued a total of 12,300,000 A Share Convertible Bonds)**
>    * **Error:** The phrasing "共發行...發行" is redundant. "發行" (issue) is repeated unnecessarily.
>    * **Correction:** 本次發行共 12,300,000 張 A 股可轉換公司債券 (This issuance totals 12,300,000 A Share Convertible Bonds).
