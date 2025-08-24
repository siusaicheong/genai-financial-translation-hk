# Online Appendix: Example 8 - Draft Synthesis and Consolidation

## Discussion

In complex projects, a translator may need to consolidate multiple drafts into a single, unified version. Continuing with the previous example, the model received three different Chinese translation drafts (a machine translation, an LLM translation, and a human translation) and was instructed to provide an enhanced final version.

The model compared the three translations, identified the weaknesses of the NMT draft, and recognised the stylistic strengths of the human-translated version. It adopted the expression "藉以" (by means of) from the human translation and incorporated it into the final output to introduce the purpose of the meeting. This example shows the model's ability to function as a consolidator of translation drafts. By aggregating input from diverse sources, the LLM can help streamline the refinement process and produce a polished, unified translation.

---

## Prompt and Model Output

### User Prompt:
> Further enhance the translation with reference to the following additional translation drafts. Explain your decisions (whether you keep your own version or use one of the new versions provided):
>
> Draft 1 (NMT):
> XXX 集團有限公司（以下簡稱「本公司」）董事會（以下簡稱「董事會」）宣布，本公司董事會會議將於 2025 年 8 月 X 日舉行，會議的主要目的是批准本公司及其子公司截至 2025 年 6 月 30 日止六個月的中期股息，並考慮派發中期股息（如有）。
>
> Draft 2 (Another LLM):
> XXX集團有限公司（「本公司」）董事會（「董事會」）謹此公告，本公司董事會會議將於2025年8月X日舉行，旨在（其中包括）批准本公司及其附屬公司截至2025年6月30日止六個月之中期業績，及考慮派發中期股息（如有）。
>
> Draft 3 (Human):
> XXX集團有限公司（「本公司」）董事會（「董事會」）宣佈，本公司將於二零二五年八月X日舉行董事會，藉以（其中包括）批准本公司及其附屬公司截至二零二五年六月三十日止六个月之中期業績，以及考慮派發中期股息（如有）。

### Model Output:
> After reviewing the additional drafts, here's the enhanced translation, along with a detailed explanation of my decisions:
>
> **Enhanced Translation:**
>
> XXX集團有限公司（「本公司」）董事會（「董事會」）謹此公告，本公司將於二零二五年八月X日舉行董事會會議，藉以（其中包括）批准本公司及其附屬公司截至二零二五年六月三十日止六個月之中期業績，以及考慮派發中期股息（如有）。
>
> **Decision Rationale – Comparing to the Drafts:**
>
> * **My Previous Version vs. Draft 1 (NMT):** Draft 1 uses "以下簡稱" ("yǐxià jiǎncheng" – hereinafter referred to as) to define "本公司" and "董事會". While grammatically correct, this is *less* common in formal HKEX announcements. My previous version, and now this enhanced version, uses the more standard quotation mark definition ("「本公司」"). Draft 1 also incorrectly states the primary purpose is to approve the "中期股息" (interim dividend) *itself* – the purpose is to approve the *results* which *include* information about a potential dividend. Therefore, I rejected Draft 1.
>
> * **My Previous Version vs. Draft 2 (Another LLM):** Draft 2 is very close to my previous version and is generally good. However, it uses "旨在 (zhǐzài)" – meaning "aims to" – which feels slightly less formal than the phrasing in Draft 3. I initially preferred my previous version's "會議議程包括但不限於" (agenda includes but is not limited to), but after further consideration, the "藉以 (jièyǐ)" construction in Draft 3 is more elegant and frequently seen in HKEX announcements.
>
> * **My Previous Version vs. Draft 3 (Human):** Draft 3 is the strongest of the three. The key improvement is the use of "藉以 (jièyǐ)" – meaning "by means of" or "in order to". This is a very common and sophisticated phrasing in HKEX announcements to introduce the purpose of a meeting. The "以及 (yǐjí)" instead of "及 (jí)" for "and" also feels slightly more polished in this context. The human translator clearly understands the nuances of HKEX style.
>
> **Specific Changes Made (Adopting elements from Draft 3):**
>
> * **"將於…舉行董事會會議" instead of "將於…舉行會議":** Specifically mentioning "董事會會議" (Board Meeting) is more precise and standard.
> * **"藉以（其中包括）" instead of "包括但不限於":** This is the most significant change. "藉以" provides a more formal and elegant introduction to the meeting's purpose. "其中包括" (including among others) is a good equivalent to "including but not limited to" in this context.
> * **"以及" instead of "及":** A subtle stylistic preference for a more polished feel.
>
> **Final Justification:**
>
> This enhanced translation now incorporates the best elements of all the drafts, prioritizing the stylistic conventions and phrasing commonly found in official announcements published by companies listed on the Hong Kong Stock Exchange. The use of "藉以" is the key improvement, elevating the translation to a more professional and authentic HKEX style. It maintains the clarity and accuracy of the original meaning while adhering to the specific requirements of the target audience and context.
