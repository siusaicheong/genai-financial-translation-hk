# Online Appendix: Example 19 - Chain-of-Thought Prompting

## Discussion

Chain-of-Thought (CoT) prompting enables structured, step-by-step reasoning by instructing the model to externalise its process before producing a final answer. Studies show that CoT can improve translation quality, especially for complex or ambiguous texts, by making the model's decision process more transparent.

To demonstrate the impact of CoT, a baseline translation of a paragraph about a cross-border payment system was produced using only a provided glossary. The resulting translation was accurate but overly literal. When given the same task with a detailed CoT prompt, the model followed a complete reasoning chain. It generated three distinct drafts (literal, fluent, and concise), critically reviewed each, and synthesised the best elements into a final, more nuanced version. The output demonstrates the LLM's ability to execute this full reasoning chain, providing multiple drafts, a self-review, and a justified final translation.

---

## Prompt and Model Output

### User Prompt (Without CoT):
> Translate the following paragraph about "Payment Connect" from English into Traditional Chinese (zh-HK). Please use the official terms provided in the glossary.
>
> Source Text:
>
> "Payment Connect refers to the linkage between the Mainland's Internet Banking Payment System (IBPS) and Hong Kong's Faster Payment System (FPS), which supports secure, efficient and convenient real-time cross-boundary payment for residents and institutions in both places. By simply inputting the recipient's mobile number or account number, residents in both places can make instant small-value cross-boundary remittances."
>
> Official Glossary / Key Term Translations:
>
> Payment Connect: 跨境支付通
> Internet Banking Payment System (IBPS): 網上支付跨行清算系統
> Faster Payment System (FPS): 快速支付系統「轉數快」
> cross-boundary payment: 跨境支付
> small-value cross-boundary remittances: 小額跨境匯款

### Model Output (Without CoT):
> Here's the translation of the paragraph into Traditional Chinese (zh-HK), using the provided glossary terms:
>
> 「**跨境支付通**是指中國內地**網上支付跨行清算系統**與香港**快速支付系統「轉數快」**的聯動，支援兩地居民及機構進行安全、高效和便捷的即時**跨境支付**。只需輸入收款人的手機號碼或帳戶號碼，兩地居民便可進行即時**小額跨境匯款**。」
>
> **Explanation of choices:**
>
> * I directly substituted the English terms with their corresponding Traditional Chinese translations from the glossary.
> * The sentence structure is kept as close to the original English as possible while sounding natural in Chinese.
> * 「是指」 (shi zhi shi) is used to clearly define what "Payment Connect" *is*.
> * 「支援」 (zhi yuan) is used for "supports" as it's a common and appropriate term in this context.
> * 「便可」 (bian ke) is used for "can" to create a smoother flow.

### User Prompt (With CoT):
> Task: Translate the following paragraph about "Payment Connect" from English into Traditional Chinese (zh-HK). Please use the official terms provided in the glossary and follow the chain-of-thought process outlined below.
>
> Source Text:
>
> "Payment Connect refers to the linkage between the Mainland's Internet Banking Payment System (IBPS) and Hong Kong's Faster Payment System (FPS), which supports secure, efficient and convenient real-time cross-boundary payment for residents and institutions in both places. By simply inputting the recipient's mobile number or account number, residents in both places can make instant small-value cross-boundary remittances."
>
> Official Glossary / Key Term Translations:
>
> Payment Connect: 跨境支付通
> Internet Banking Payment System (IBPS): 網上支付跨行清算系統
> Faster Payment System (FPS): 快速支付系統「轉數快」
> cross-boundary payment: 跨境支付
> small-value cross-boundary remittances: 小額跨境匯款
>
> Instructions for the Chain-of-Thought Process:
>
> Step 1: Generate Three Distinct Draft Translations.
> Based on the source text and ensuring the mandatory use of the Official Glossary provided above, produce three different draft translations. Each draft should explore a slightly different stylistic choice while remaining accurate.
> Draft A: A literal, direct translation that closely follows the source sentence structure.
> Draft B: A more fluent, slightly reorganized translation that prioritizes naturalness in Chinese.
> Draft C: A concise, official-sounding translation suitable for a formal announcement.
>
> Step 2: Self-Review and Final Version.
> Critically evaluate the three drafts. Point out the strengths and weaknesses of each, specifically mentioning how they incorporated the official terms. Then, combine the best elements of all three drafts to produce a single, polished final version. Explain why your final version is the optimal choice, considering accuracy, clarity, and style for a Hong Kong audience.
>
> Please present your response by clearly labeling each step.

### Model Output (With CoT):
> ## Translation of "Payment Connect" into Traditional Chinese (zh-HK)
>
> **Step 1: Generate Three Distinct Draft Translations**
>
> **Draft A (Literal, Direct Translation):**
>
> 「跨境支付通」是指中國大陸的網上支付跨行清算系統與香港快速支付系統「轉數快」之間的連結，支援兩地居民及機構安全、高效和便捷的即時跨境支付。只需輸入收款人的手機號碼或帳戶號碼，兩地居民便可進行即時小額跨境匯款。
>
> **Draft B (Fluent, Reorganized Translation):**
>
> 「跨境支付通」連接了中國大陸的網上支付跨行清算系統和香港的快速支付系統「轉數快」，為兩地居民和機構提供安全、高效及方便的即時跨境支付服務。 透過輸入收款人的手機號碼或帳戶號碼，兩地居民即可輕鬆進行小額跨境匯款。
>
> **Draft C (Concise, Official-Sounding Translation):**
>
> 「跨境支付通」是中國大陸網上支付跨行清算系統與香港快速支付系統「轉數快」的互聯互通，支援兩地居民及機構進行安全、高效的即時跨境支付。 兩地居民可透過輸入收款人手機號碼或帳戶號碼，即時進行小額跨境匯款。
>
> **Step 2: Self-Review and Final Version**
>
> **Review of Drafts:**
>
> * **Draft A:** This draft is the most literal. It accurately incorporates all the official terms. However, the sentence structure feels slightly clunky and less natural in Chinese. The repetition of "即時" (instant) feels redundant.
> * **Draft B:** This draft flows more naturally in Chinese. The use of "連接了" (connected) and "透過" (through) improves readability. It also uses "輕鬆" (easily) which adds a slight positive connotation. It effectively uses all official terms.
> * **Draft C:** This draft is the most concise and has a formal tone, suitable for an official announcement. The phrase "互聯互通" (interconnectivity) is a common term used in official Chinese contexts regarding payment systems. It also effectively uses all official terms. However, it might be *too* concise and lack some of the explanatory detail of the other drafts.
>
> **Final Version:**
>
> 「跨境支付通」連接了中國大陸的網上支付跨行清算系統和香港的快速支付系統「轉數快」，為兩地居民和機構提供安全、高效及方便的即時跨境支付服務。只需輸入收款人的手機號碼或帳戶號碼，兩地居民即可輕鬆進行小額跨境匯款。
>
> **Justification:**
>
> This final version is the optimal choice because it strikes a balance between accuracy, clarity, and style. It builds upon the strengths of Draft B (natural flow) and incorporates the concise, official tone of Draft C. Specifically:
>
> * **Accuracy:** It uses all the official terms from the glossary correctly and maintains the original meaning of the source text.
> * **Clarity:** The sentence structure is clear and easy to understand for a Hong Kong audience. The use of "只需" (simply) and "即可" (can) makes the process sound straightforward.
> * **Style:** The tone is professional and informative, suitable for a wide range of contexts, from public announcements to user guides. The inclusion of "輕鬆" (easily) adds a user-friendly touch without sacrificing formality.
> * **Hong Kong Context:** The phrasing and word choices are natural and commonly used in Hong Kong Cantonese and written Chinese. The use of 「轉數快」 in its full form is important for recognition by the Hong Kong public.
