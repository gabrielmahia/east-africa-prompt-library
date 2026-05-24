# Diaspora Prompts — RemitAI, Kenyan Diaspora Services

> Adapted from 1337 Use Cases for ChatGPT (Section 5.25: Managing Personal Finances, Section 7.35: Personal Finance)
> East African context: Kenyan diaspora in UK, US, Canada, Middle East; remittances, property, citizenship

---

## Diaspora Remittance Optimization

**General prompt:**
"What is the cheapest way to send money from [country] to Kenya?"

**Formula:**
"I am sending [currency] [amount] from [origin country] to Kenya to [recipient type]. Compare [Wise/Western Union/M-Pesa Global/bank wire] for: total cost, exchange rate, speed, and recipient delivery method. Recommend the best option."

**East Africa examples:**
- "I am sending $500/month from the United States to my family in Nakuru. Compare Wise, Remitly, and M-Pesa Global for total cost including fees and exchange rate spread. Assume recipient collects via M-Pesa."
- "I need to send £2,000 urgently from the UK to pay school fees in Nairobi by Friday. Which service is fastest and what are the total costs?"
- "I send AED 3,000 monthly from Dubai to Kenya. My family is in a rural area near Kisumu with no bank. Compare options that deliver to M-Pesa agents vs. physical cash pickup."

---

## Kenya Property Investment from Diaspora

**General prompt:**
"How do I invest in Kenya real estate as a diaspora member?"

**Formula:**
"I am a Kenyan in [country] with [budget in KES/USD] looking to [buy land/build a house/buy an apartment] in [location in Kenya]. Guide me through: legal requirements for diaspora ownership, recommended developers/agents, financing options (KCB diaspora mortgage, NCBA), title deed verification, and pitfalls to avoid."

**East Africa examples:**
- "I am a Kenyan in the UK wanting to buy 1/8 acre in Kitengela for KES 800,000. Walk me through the legal process: what documents do I need, how do I verify the title deed remotely, and which lawyers specialize in diaspora property transactions?"
- "I want to build a 3-bedroom house in Eldoret with a budget of KES 4.5M. I am in Canada. How do I manage the construction remotely, which contractors are reputable, and how do I protect myself from fraud?"
- "What are the current NSSF and NHIF rules for Kenyans working abroad? Should I maintain contributions and what are the pension implications?"

---

## Dual Citizenship and Kenyan Identity

**General prompt:**
"What are the rules for dual citizenship for Kenyans in [country]?"

**Formula:**
"I am a Kenyan citizen who has [become a citizen of/is applying for citizenship in] [country]. What are the: (1) Kenya's position on dual citizenship under the 2010 Constitution, (2) requirements to retain my Kenyan citizenship, (3) implications for property ownership, voting, and work permits, (4) process to reaffirm Kenyan citizenship if lost."

**East Africa examples:**
- "I became a US citizen in 2022. Do I still hold Kenyan citizenship? What documents do I need to get a Kenyan passport? Can I own property in Kenya?"
- "I hold a Kenya passport and UK Indefinite Leave to Remain. If I naturalize as British, what happens to my Kenyan citizenship under the 2010 Constitution?"

---

## RemitAI Integration Prompts

For use with [remit-ai](https://github.com/gabrielmahia/remit-ai):

```
Compare remittance options for sending [amount] [currency] 
from [origin_country] to Kenya.
Recipient collects via: [M-Pesa/bank/cash pickup].
Return: top 3 options ranked by total cost, with exchange rates and fees.
```

```
What Kenyan government services are available online for diaspora?
List: eCitizen services, passport renewal, NTSA, NSSF, NHIF.
Indicate which require physical presence and which are fully remote.
```
