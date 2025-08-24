# Online Appendix: Example 14 - Context Limitations and Instructional Drift

## Discussion

A further technical limitation of LLMs is the context window – the maximum amount of text, including user input and conversation history, that a model can process at one time. While context windows are increasing rapidly, this theoretical capacity presents two main challenges. First, fully utilising a large context window is computationally expensive, requiring significant VRAM to store the entire conversation and model state. Often, hardware limitations prevent users from leveraging the full advertised context length. Second, a model may fail even when operating within the context limit and on adequate hardware. Instructional drift occurs when a model forgets or disregards earlier instructions in a long conversation, possibly because it disproportionately weights more recent prompts. Language models often struggle to retrieve information from the middle of a long context.

To demonstrate this, a multi-round translation task was conducted using a 4-bit quantised Gemma 4B model with its context window set to 8,192 tokens – far below its maximum of 128,000 tokens. The 4B model was selected to demonstrate how context window usage and memory constraints affect smaller, quantised models. Table 8 presents samples from three rounds of conversation, each based on an excerpt from a different HKMA press release.

In Round 1, the user prompted the model to translate "Northern Metropolis" as "北部都會區", which the model did. After an intermediate task, the user asked the model in Round 3 to translate a new text containing "Northern Metropolis" and reminded the model to "follow the Chinese terms … we provided before". Despite only using about 74% of the context window, the model did not remember the instruction and produced the incorrect term "北约都会区" in Simplified Chinese, violating both terminological and style requirements. This is a clear example of instructional drift. The most reliable way to counter this is through active human intervention – including constant oversight, explicit instruction reinforcement, and output consistency monitoring – rather than passively expecting the model to maintain instruction adherence. This failure mode is a regulatory concern. The SFC warns that "an AI LM's performance may drift and degrade over time such that it no longer does what it was initially designed to do", while the HKSAR Government calls for "Reliability and Trustworthiness" in AI systems. The SFC's requirement for "ongoing review and monitoring" and the HKMA's mandate for "proper validation of the GenAI models" are designed can help address this risk.

---

## Prompt and Model Output

### User Prompt (Round 1):

> Translate the following into Chinese (Note that Northern Metropolis is 北部都會區):
>
> The following is issued on behalf of the Hong Kong Monetary Authority:
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Hong Kong Monetary Authority (HKMA), together with the banking sector, introduced today (April 8) sector-specific support measures to further assist more small and medium-sized enterprises (SMEs) in obtaining bank financing and in their upgrade and transformation. The measures were introduced following meetings held by the Banking Sector SME Lending Coordination Mechanism (Mechanism) and the Taskforce on SME Lending (Taskforce) today.
> 
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Since the launch of the "9+5" (Note 1) SME support measures by the HKMA and the banking sector last year, more than 39 000 SMEs have benefitted from these measures, involving an aggregate credit limit of over HK$95 billion. The total amount of dedicated funds for SMEs set aside by the participating banks in the Taskforce in their loan portfolio has increased from HK$370 billion in October 2024 to more than HK$390 billion at present.
> 
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;With the establishment of the Taskforce in August 2024, the HKMA and the banking sector have been actively strengthening the work of supporting SMEs at both the individual case and the industry levels. Up until the end of March 2025, the Taskforce has received around 590 enquiries and cases from various industries through different channels, of which nearly 90 per cent have been handled. At the industry level, the Taskforce has held more than 160 engagement events with trade associations and representatives from different industry sectors―including the retail and wholesale, import and export and manufacturing, construction, and transport sectors ― to gain a deeper understanding of the operations of SMEs in various industries.
> 
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In the light of the current trade tension and uncertainties surrounding the external economic environment, and after taking into account and discussing the views of the commercial sectors in the Mechanism and Taskforce meetings, the banking sector reaffirmed its commitment to actively implement the "9+5" SME support measures previously launched. The banking sector will continue to be accommodative in offering credit reliefs, including flexible repayment arrangements and deferment of repayment period, referencing the principles under the Pre-approved Principal Payment Holiday Scheme, to assist corporates in coping with their liquidity needs. Furthermore, banks will introduce more targeted support for various industries under the overarching principle of prudent risk management:
> 
> Import and export and manufacturing sectors: The commercial sectors reflected their concerns about the current global trade frictions during the meeting. The participating banks agree to provide flexible extensions to trade facilities (e.g. 90 or 120 days), or offer alternative suitable credit arrangements (such as repaying the trade loans by instalments, providing partial principal repayment options, or even offering principal moratorium), to assist individual customers experiencing short-term cashflow pressure due to trade frictions. The Mechanism and the Taskforce will closely monitor the latest developments regarding global tariff disputes and maintain dialogue with the import and export and manufacturing sectors. 
>  
> Construction sector: The participating banks will assist corporates facing cashflow pressure, particularly subcontractors in the construction sector that may be experiencing sudden cashflow pressure due to capital chain rupture, through a collaborative mechanism. The banks will collaboratively offer flexible financial arrangements as far as practicable to alleviate customers' cashflow pressure. 
> 
> Transport sector: The participating banks will actively consider introducing financing products that are better suited to the transport sector, with a view to supporting the Government's implementation of measures to enhance taxi services. The banks will offer more flexible repayment arrangements to assist customers in coping with operational challenges, taking into account individual circumstances. The banks will also consider correspondingly extending the loan tenor to support the development of the sector (Note 2).  
> ​  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Furthermore, the HKMA and the banking sector will support the economic development of Hong Kong in other areas, including:
> 
> Lease extension: The banking sector will strengthen the promotion of the Extension of Government Leases Ordinance (the Ordinance) (Note 3). Banks will ensure that frontline staff are familiar with land lease extension matters under the Ordinance, so that they can properly address customers' mortgage enquiries related to land leases and offer suitable services to them. 
> 
> Northern Metropolis development: With the HKMA's facilitation, the Hong Kong Association of Banks and the Chinese Banking Association of Hong Kong have recently engaged with the Development Bureau to gain an understanding of the latest development of the Northern Metropolis. The banking sector will explore ways to provide suitable financing support to tie in with the Government's implementation of large-scale land disposal and other developments. 
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The HKMA and the banking sector will maintain close communication with the commercial sectors through the Mechanism and the Taskforce and work in concert to support the business development and transformation of SMEs.

### Model Output (Round 1):
> Here's a translation of the provided text into Chinese, aiming for clarity and accuracy suitable for a formal announcement:
>
> **香港金融管理局發布**
>
> （香港，2024年4月8日）香港金融管理局（HKMA）與銀行業合作，今日（2024年4月8日）推出針對性的支持措施，以進一步協助更多小及中型企業（SMEs）獲得銀行貸款並進行升級和轉型。這些措施是在銀行業 SME 融資協調機制（Mechanism）及 SME 融資任務組（Taskforce）今日舉行的會議後推出的。
>
> 自香港金融管理局與銀行業去年推出「9+5」 (備註1) SME 支持措施以來，超過39,000家SME已從這些措施中受益，涉及超過港幣950億元的總額信貸額度。在任務組中參與的銀行撥設用於SME的專項資金從2024年10月27日的370億港元增加至目前超過390億港元。
>
> 隨著任務組於2024年8月成立，香港金融管理局與銀行業積極加強了對SME的支持工作，無論是個別案件還是行業層面。截至2025年3月底，任務組已收到來自各行各業的約590個查詢和案件，其中近90%已得到處理。在行業層面上，任務組與零售及批發、進出口及製造、建築和運輸等不同行業協會以及代表進行了超過160場交流活動，以更深入地了解SME在各行業的運作情況。
>
> 鑒於目前貿易緊張局勢以及外部經濟環境的不確定性，並考慮到機制和任務組會議中商業部門的觀點，銀行業確認將繼續積極推行「9+5」SME支持措施。銀行業將繼續提供靈活的融資補貼，包括符合預先批准的本金減免計劃原則的彈性還款安排和還款期限延遲，以協助企業應對其流動資金需求。此外，銀行將在謹慎風險管理原則下，向各行業推出更多有針對性的支持措施。
>
> 進出口及製造業：會議中商業部門表達了對目前全球貿易摩擦的擔憂。參與銀行同意提供與貿易融資相關的靈活延期（例如90或120天），或提供替代性合適的信貸安排（如分期償還貿易貸款、提供部分本金償還選項，甚至提供本金凍結期），以協助因貿易摩擦而面臨短期現金流壓力的個人客戶。機制和任務組將密切監察全球關稅爭端最新發展並與進出口及製造業部門保持對話。
>
> 建築業：參與銀行將協助面臨現金流壓力，尤其是在資本鏈中可能出現突然現金流壓力的建築行業承包商，透過協同機制。銀行將盡可能提供靈活的財務安排以減輕客戶的現金流壓力。
>
> 運輸業：參與銀行將積極考慮更適合運輸業的融資產品，以支持政府加強計程車服務的措施。銀行將提供更靈活的還款安排，以協助客戶應對運營挑戰，並充分考慮個人情況。銀行也將相應地延長貸款期限，以支持該行業的發展（備註2）。
>
> 此外，香港金融管理局與銀行業將在其他方面支持香港經濟發展，包括：
>
> 租約延期：銀行業將加強推廣《政府租約延期條例》（備註3） 。銀行將確保前線員工熟悉該條例下的土地租約事宜，以便妥善處理客戶有關土地租約的貸款查詢並為他們提供適當服務。
>
> 北部都會區發展：在香港金融管理局的協助下，香港銀行會計師公會和香港銀行業務委員會最近與發展局接觸，以了解北部都會區的最新進展。銀行業將探索如何提供相容的融資支持，以配合政府的大規模土地處分和其他發展項目。
>
> 香港金融管理局與銀行業將透過機制和任務組與商業部門保持密切溝通，並共同支持SME 的業務發展和轉型。

### User Prompt (Round 2):
> Translate the following text into Chinese - follow the Chinese terms (if any) we provided before:
> 
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Hong Kong Monetary Authority (HKMA) and the Asian Infrastructure Investment Bank (AIIB) today (June 26) signed a partnership agreement to support venture capital (VC) in emerging Asia, marking a new milestone in deepening the ties and collaboration between the two institutions.
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Under the partnership, the HKMA and the AIIB will collaborate closely to invest in a portfolio of VC funds that prioritise investments across emerging markets in Asia. The HKMA and the AIIB aim to jointly support the development of innovative technologies and business models for green and technology-enabled infrastructure in Asia's emerging economies, while promoting Hong Kong's established ecosystem for VCs and innovators across the region.
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Financial Secretary of the Hong Kong Special Administrative Region Government, Mr Paul Chan, said, "Energy transition and infrastructure development of the Global South require substantial financial investment and support from technological applications in various fields. This collaboration combines and leverages the HKMA's and the AIIB's knowledge, experience, networks, and strengths. It supports emerging Asian economies in accelerating their development towards more prosperous and inclusive growth through innovation and technology. Additionally, it aids in building a more vibrant venture capital and innovation ecosystem within the region and further reinforces Hong Kong's status as an international financial, innovation and technology centre."
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Chief Executive of the HKMA, Mr Eddie Yue, said, "As a leading innovation technology hub, as well as a green finance hub in Asia, Hong Kong has been a staunch supporter of innovation and sustainable investment. We are pleased to join hands with the AIIB, which enables the HKMA to tap into its extensive expertise and network in sourcing investable opportunities in emerging Asia with a proper risk management and governance framework. We believe this strategic partnership will provide a demonstration effect on the scaling of capital for emerging Asia's innovators."
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The President of the AIIB, Mr Jin Liqun, said, "Hong Kong, China is a valued member of the AIIB and has played a pivotal role in the Bank's growth, including through its leading global financial centre. The strategic partnership with the HKMA further deepens this relationship. By bringing together our respective strengths and expertise, the partnership will help mobilise capital for infrastructure, foster innovation, and accelerate the transition toward a sustainable and prosperous future across Asia."

### Model Output (Round 2):
> Here's the translation of the provided text into Chinese, incorporating the previously established terminology and aiming for a professional tone:
>
> **香港金融管理局與亞投行簽署合作協議，支持亞洲新興市場風險投資 (VC)**
>
> （香港，2024年6月26日）香港金融管理局（HKMA）及亞投銀行今日（2024年6月26日）簽訂合作協議，以支持亞洲新興市場的風險投資（VC），標誌著兩家機構深化聯繫與合作的一個重要里程碑。
>
> 根據該項協議，香港金融管理局和亞投銀行將密切合作，投資於一個優先投資於亞洲新興市場的 VC 基金組合。香港金融管理局和亞投銀行旨在共同支持亞洲新興經濟體在綠色及科技賦能基礎設施方面創新技術和商業模式的發展，同時推動香港作為該地區風險投資者和創新者的成熟生態系統。
>
> 香港特別行政區財務長徐洪基表示：「全球南方能源轉型與基礎設施發展需要大量的財政投入以及來自各個領域技術應用的支持。這項合作整合並利用了香港金融管理局及亞投銀行的知識、經驗、網絡和優勢，有助亞洲新興經濟體透過創新和科技加速向更繁榮和包容的增長方向邁進。此外，它也有助於該地區建立一個更加活躍的風險投資和創新生態系統，並進一步鞏固香港作為國際金融、創新及科技中心的地位。」
>
> 香港金融管理局行政總監葉惠恆表示：「作為亞洲領先的創新科技樞紐以及綠色金融樞紐，香港一直堅定支持創新和可持續投資。我們很高興與亞投銀行合作，使香港金融管理局能夠利用其在亞洲新興市場尋找可投資機會方面的廣泛知識、經驗、網絡和框架。我們相信，這項戰略性夥伴關係將為亞洲新興領域的創新者提供資本規模擴大的示範。」
>
> 亞投行主席金立峰表示：「中國香港是亞投行的寶貴成員，並在該銀行發展中發揮了關鍵作用，包括透過其領先的全球金融中心地位。與香港金融管理局的戰略性合作進一步加深了這項關係。通過整合各自的優勢和專業知識，這項合作夥伴關係將有助於動員資本用於基礎設施建設、促進創新並加速亞洲向可持續繁榮的未來轉型。」

### User Prompt (Round 3):
> Translate the following text into Chinese - follow the Chinese terms (if any) we provided before:
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Government of the Hong Kong Special Administrative Region of the People's Republic of China (the HKSAR Government) today (June 4) announced the successful pricing of approximately HK$27 billion worth of green bonds (the Green Bonds) and infrastructure bonds (the Infrastructure Bonds) denominated in Hong Kong dollars (HKD), Renminbi (RMB), US dollars (USD), and euro (EUR) under the Government Sustainable Bond Programme and the Infrastructure Bond Programme.
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Following a virtual roadshow on June 2, 2025, the Green Bonds and Infrastructure Bonds were priced on June 3, 2025 as follows:
> 
> HKD1.5 billion 30-year infrastructure tranche at 3.85 per cent;
> RMB4 billion 20-year green tranche at 2.60 per cent;
> RMB4 billion 30-year infrastructure tranche at 2.70 per cent;
> USD1 billion 5-year green tranche at 4.151 per cent; and
> EUR1 billion 8-year green tranche at 3.155 per cent.
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The offering attracted participation from a wide spectrum of investors from more than 30 markets across Asia, Europe, Middle East, and the Americas, with total order amounting around HK$237 billion equivalent, representing a subscription ratio of around 3.3 to 12.5 times. In particular, the HKD 30-year bond was offered for the first time by the HKSAR Government, and is the longest tenor HKD bond issued by the HKSAR Government so far. The 20-year and 30-year RMB bonds, which were first introduced last year, also received overwhelming support, doubling in issuance size from last year.
>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Financial Secretary, Mr Paul Chan, said, "The issuance of green bonds by the HKSAR Government aims to attract and channel market capital to support green projects, promoting the sustainable development in Hong Kong. The issuance of infrastructure bonds helps to accelerate the development of projects such as the Northern Metropolis and facilitate the early completion of projects for the good of the economy and people's livelihood. Global institutional investors responded enthusiastically to the subscription, fully reflecting their confidence in Hong Kong's sound public finance and long-term development. Among which the inaugural offering of the 30-year HKD government bonds helps to extend the HKD benchmark yield curve, further promoting the development of the local bond market."

### Model Output (Round 3):
> Here's the translation of the provided text into Chinese, adhering to previously established terminology and maintaining a formal tone:
>
> **香港特别行政区政府成功发行约270亿港元绿色债券及基础设施债券**
>
> （香港，2024年6月4日）香港特别行政区政府今日（2024年6月4日）宣布，其绿色债券 (Green Bonds) 和基础设施债券 (Infrastructure Bonds) 的发行已成功完成，这些债券分别以港元 (HKD)、人民币 (RMB)、美元 (USD) 和欧元 (EUR) 计价，是在香港特别行政区可持续债券计划和基础设施债券计划框架下进行的。
>
> 在2025年6月2日举行的虚拟路演后，绿色债券和基础设施债券于2025年6月3日以以下价格确定：
>
> * 港币15亿 (HKD1.5 billion) 期限为30年的基础设施期权，利率为3.85%；
> * 人民币40亿 (RMB4 billion) 期限为20年的绿色期权，利率为2.60%；
> * 人民币40亿 (RMB4 billion) 期限为30年的基础设施期权，利率为2.70%；
> * 美元10亿 (USD1 billion) 期限为5年的绿色期权，利率为4.151%；以及
> * 欧元10亿 (EUR1 billion) 期限为8年的绿色期权，利率为3.155%。
>
> 此次发行吸引了来自亚洲、欧洲、中东和美洲超过30个市场的广泛投资者参与，总认购金额约为237亿港元（相当于），认购比例达到3.3至12.5倍。特别地，香港特别行政区政府首次推出期限为30年的港币债券，是香港特别行政区政府迄今为止发行期限最长的港币债券。去年首次引入的20年和30年人民币债券也获得了强劲的支持，发行规模比去年翻倍。
>
> 财政司司长徐洪基表示："香港特别行政区的绿色债券发行旨在吸引并引导市场资金支持绿色项目，促进香港的可持续发展。基础设施债券的发行有助于加快北约都会区等项目的建设步伐，并为经济和民生带来早期的效益。全球机构投资者对认购表现出热情，充分反映了他们对香港稳健公共财政和长期发展的信心。其中，首次发售30年港币政府债券有助于延伸港币基准收益率曲线，进一步促进本地债券市场发展。"
