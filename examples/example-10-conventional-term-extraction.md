# Online Appendix: Example 10 - Conventional Term Extraction

## Discussion

Terms were initially extracted from a pair of parallel English and Chinese texts related to Hong Kong's economic policy using a conventional tool based on frequency and n-gram analysis. The resulting list includes several incomplete or incorrect pairs, such as "financial markets" matched with the truncated "金融市" (financial market), or "foreign businesses" paired with an imprecise, overly long segment.

For "business initiatives", the extracted Chinese term was "商業" (business), omitting the idea of "initiatives"; for "Hong Kong's", the corresponding term was "香港金融市場" (Hong Kong's financial market). The extracted terms tend to be short, and key expressions such as "fair market" and "exchange controls" are omitted.

---

## Data and Results

### Table 10.1: Parallel English and Chinese paragraphs for term extraction

| English text (Source: HKSAR Government 2020a) | Chinese text (Source: HKSAR Government 2020b) |
| :--- | :--- |
| "Hong Kong is a major international financial centre, comprising an integrated network of institutions and markets which provide a wide range of products and services to local and international customers and investors. Hong Kong's financial markets operate under effective and transparent regulations that are in line with international standards. Another feature is high liquidity in the markets. The Government of the Hong Kong Special Administrative Region (HKSAR) abides by the principle of keeping intervention into the way in which the market operates to a minimum and has endeavoured to provide a favourable environment in which business operates. Its policy of low and simple taxation allows maximum room for business initiatives and innovation. There is a strong emphasis on the rule of law and fair market. There are no barriers of access to the market by foreign businesses, with free flow of capital and information. There are also no exchange controls." | 香港是主要的國際金融中心，金融機構和市場緊密聯繫，為本地和海外的客戶及投資者提供各類投資產品及服務。香港金融市場的在有效和具透明度的監管下運作，各項監管規例都與國際標準一致。另一特點是資金流動性高。香港特別行政區（香港特區）政府恪守盡量不干預金融市場運作的原則，並盡力提供一個有利營商的環境。政府實施低稅政策和推行簡單的稅制，使各類商業有更多主動權及創新空間。香港十分重視法治及維持市場的公平競爭，不會阻止外國公司參與本地的金融市場，資訊及資金自由流動。此外，本港亦無實施外匯管制。 |

### Table 10.2: Term extraction results from a conventional statistical method

*Term extraction configurations: Min. frequency: 1; length range: 1-8 words*

| English | Chinese |
| :--- | :--- |
| Hong Kong | 香港 |
| high liquidity | 資金流動性 |
| business | 營商 |
| foreign businesses | 外國公司參與本地 |
| free flow | 自由流動 |
| products | 產品 |
| financial markets | 金融市 |
| markets | 市場 |
| the principle | 原則 |
| Hong Kong's | 香港金融市場 |
| simple taxation | 簡單的稅制 |
| business initiatives | 商業 |
| institutions | 機構 |
