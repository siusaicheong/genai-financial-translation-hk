# Online Appendix: Example 2 - Terminology Extraction

## Discussion

Terminological consistency is a core element of translation quality. Translators often ensure this by building and maintaining project-specific glossaries, a process that can be time-consuming and labour-intensive. LLMs can automate the first step: identifying terms in the source text. In the following example, the model was given a sample corporate communication and asked to provide a list of key expressions requiring standardised translation, together with context-specific definitions.

The model listed ten key terms (e.g., "share registrar", "intermediaries", and "ESG reports") and provided definitions and "Translation Notes" for each, with specific guidance for translation into Chinese. This approach streamlines the initial stage of glossary creation and automates much of the manual identification work.

---

## Prompt and Model Output

### User Prompt:
> Given the following financial text to be translated, identify key terms or technical expressions that require official or standardised translation. Provide a brief, context-specific definition for each.
>
> The English and Chinese versions of the Company's current corporate communications are available on the Company's website at [URL] (the "Company's website") and the website of The Stock Exchange of Hong Kong Limited (the "HKEx's website") at www.hkexnews.hk, respectively (the "Website Version"). The Company strongly recommends that you access the Website Version of the current corporate communications and all future corporate communications.
>
> If you wish to receive the current corporate communications in printed form, please complete the Request Form and return it to the Company c/o XXX Share Registrars (HK) Limited (the "Hong Kong Branch Share Registrar"), the branch share registrar of the Company in Hong Kong, by using the mailing label at the bottom of the Request Form (no need to affix a stamp if posted in Hong Kong; otherwise, please affix an appropriate stamp). The address of the Hong Kong Branch Share Registrar is [Room], [Floor], [Building], [Street], [District], Hong Kong. You may also send an email with a scanned copy of the Request Form to [email]. The Request Form is available for download from the tab headed "Announcement" under the "Investor Relations" section on the Company's website.
>
> As a non-registered shareholder, if you wish to receive corporate communications of the Company in electronic form, you should liaise with your bank(s), broker(s), custodian(s), nominee(s), or HKSCC Nominees Limited through which your shares in the Company are held (collectively, the "Intermediaries") and provide your email address to your Intermediaries. Please contact your Intermediaries for the detailed procedure. If the Company does not receive your functional email address from the Intermediaries, until such time that a functional email address is provided to the Intermediaries, you will be unable to receive any notices of publication of the Website Version of corporate communications (the "Notice of Publication") by email, and the Company would only be able to send you the Notice of Publication in printed form.
>
> The Company's ESG Report is published in electronic form only on the Company's website and the HKEx's website. You may access the ESG Report on the Company's website or by browsing through the HKEx's website.

### Model Output:
> ### Key Terms & Technical Expressions Requiring Standardised Translation:
>
> Here's a breakdown of key terms from the text, requiring careful, standardised translation, particularly for legal and regulatory compliance. I've included context-specific definitions for clarity. I'll focus on terms likely to be problematic in translation to Chinese (Mandarin or Cantonese, depending on the target audience).
>
> **1. Corporate Communications (公司通訊)**
>
> * **Definition:** Official documents released by a company to its shareholders and the public, including annual reports, financial statements, notices of meetings, and other material information. Crucially, this isn't just *any* communication, but those with legal/regulatory weight.
> * **Translation Notes:** Needs a precise, legally recognised term in the target language. Simply translating as "company news" is insufficient. The nuance of *official* communication is vital.
>
> **2. Website Version (網站版本)**
>
> * **Definition:** The version of the corporate communications published on the company's and HKEx's websites. This is important for establishing the official record and date of publication.
> * **Translation Notes:** Needs to clearly indicate it's the *digital* version, as opposed to a printed version.
>
> **3. The Stock Exchange of Hong Kong Limited (香港交易所有限公司) / HKEx (香港交易所)**
>
> * **Definition:** The primary stock exchange in Hong Kong, responsible for listing companies and regulating trading.
> * **Translation Notes:** The official Chinese name is crucial for regulatory compliance. Using the abbreviation "HKEx" requires a clear explanation of its meaning the first time it's used.
>
> **4. Share Registrar (股份登記人) / Hong Kong Branch Share Registrar (香港分部股份登記人)**
>
> * **Definition:** A company responsible for maintaining the register of shareholders, processing share transfers, and distributing corporate communications. The "Branch" designation specifies the registrar operating within Hong Kong.
> * **Translation Notes:** The role is highly regulated. The translation must accurately reflect the legal responsibilities of the registrar.
>
> **5. Request Form (申請表格)**
>
> * **Definition:** A specific form provided by the company allowing shareholders to request printed copies of corporate communications.
> * **Translation Notes:** Needs to be clear that this is a *formal* document for making a specific request.
>
> **6. Intermediaries (中介人)**
>
> * **Definition:** Banks, brokers, custodians, nominees, or HKSCC Nominees Limited through which shares are held on behalf of beneficial owners. These entities act as a go-between between the company and the ultimate shareholder.
> * **Translation Notes:** This is a collective term. The translation needs to convey this collective meaning and the specific roles of each type of intermediary.
>
> **7. HKSCC Nominees Limited (香港中央結算所代理人有限公司)**
>
> * **Definition:** A nominee company operated by Hong Kong Clearing and Settlement Systems (HKSCC), holding shares on behalf of its clients.
> * **Translation Notes:** The full, official Chinese name is essential.
>
> **8. Functional Email Address (有效電子郵件地址)**
>
> * **Definition:** An email address that is actively monitored and capable of receiving electronic communications. It implies an address that is valid and in use.
> * **Translation Notes:** The "functional" aspect is important – it's not just *any* email address, but one that will actually deliver the communications.
>
> **9. Notice of Publication (發佈通知)**
>
> * **Definition:** A notification sent to shareholders informing them that the Website Version of corporate communications is available.
> * **Translation Notes:** Needs to clearly indicate this is a *formal* notification about the availability of official documents.
>
> **10. ESG Report (環境、社會及管治報告)**
>
> * **Definition:** A report detailing a company's performance in Environmental, Social, and Governance factors.
> * **Translation Notes:** The acronym "ESG" is becoming increasingly common, but the full Chinese translation should be provided the first time it's used.
