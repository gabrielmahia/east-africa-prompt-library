# Civic & Government Prompts — Policy, Accountability, Public Services

> Adapted from 1337 Use Cases for ChatGPT (Section 8: Law and Government, Section 10.19: Political Science)
> East African context: Kenya county government, Huduma services, CDF accountability, public policy

---

## 8.14.1 Public Policy Analysis

**General prompt:**
"What are the most effective strategies for addressing [policy issue] in Kenya?"

**Formula:**
"What are the [most/least] effective strategies for addressing [specific policy issue] in [county/national] Kenya? Consider [budget constraints/political context/implementation capacity] and rank by [feasibility/impact/cost-effectiveness]."

**East Africa examples:**
- "What are the most effective strategies for addressing teenage pregnancy in Homa Bay County, Kenya? Consider school re-entry policies, conditional cash transfers, and community health volunteer programs."
- "Analyze public policy options for improving maternal health in Kenya's arid and semi-arid counties. Rank by cost per QALY gained."
- "What legislative and administrative reforms would most effectively reduce corruption in Kenya's public procurement process? Reference the Public Procurement and Asset Disposal Act 2015."

---

## 8.10 Legal Research — Kenya Context

**General prompt:**
"Find legal cases related to [legal issue] in Kenya."

**Formula:**
"I need to find [Kenyan court cases/legislation/regulations] that relate to [specific legal issue]. Focus on [High Court/Court of Appeal/Supreme Court] decisions since [year]."

**East Africa examples:**
- "Find Kenyan court cases related to forced evictions from urban informal settlements. Focus on constitutional petitions invoking Article 43 (right to housing) since 2010."
- "What does Kenya's Data Protection Act 2019 say about the collection and use of biometric data? Summarize the key obligations for data controllers."
- "Analyze the legal framework for community land rights in Kenya under the Community Land Act 2016. What protections exist against expropriation?"

---

## 10.19.3 Public Policy — East Africa

**General prompt:**
"Analyze the public policy implications of [development issue] in East Africa."

**Formula:**
"Analyze [policy issue] across [Kenya/Uganda/Tanzania/Rwanda]. Compare approaches, identify [best practices/gaps/coordination opportunities], and recommend a [regional/national] policy framework."

**East Africa examples:**
- "Compare digital financial inclusion policies across Kenya, Uganda, and Tanzania. Identify what Kenya's M-Pesa regulatory framework got right that others can adopt."
- "Analyze the policy implications of large-scale land acquisitions for agriculture in Tanzania and Ethiopia. What protections should regional frameworks include?"
- "Evaluate the East African Community's common market protocol implementation. Where are the biggest gaps in free movement of people and services?"

---

## civic-agent-kit Integration Prompts

For use with [civic-agent-kit](https://github.com/gabrielmahia/civic-agent-kit):

```
Retrieve the latest Huduma Center service availability 
for [county_name] county.
Return: services_available[], wait_time_estimate, 
        online_alternatives, document_requirements
```

```
Analyze CDF allocation for [constituency] constituency 
in the [year] financial year.
Compare against national average per capita allocation.
Flag any anomalies in procurement records.
```

```
Generate a citizen feedback report for [county] county government.
Aggregate service delivery ratings by department.
Identify top 3 performance gaps and recommend improvement actions.
```

---

## 6.1 Activism and Accountability

**General prompt:**
"How do I analyze and expose misinformation about [policy/issue]?"

**Formula:**
"Analyze [claim/policy statement/government document] from [source] for accuracy. Cross-reference against [official statistics/audit reports/court records]. Identify [factual errors/misleading framing/omissions] and generate a corrected briefing."

**East Africa examples:**
- "Analyze the Kenya government's claim that [unemployment rate] is below 10%. Cross-reference against KNBS Labour Force Report Q4 2024 and identify discrepancies."
- "The county government states KES 50M was spent on borehole construction in 10 wards. Verify this claim against the published procurement records and flag any irregularities."
- "Analyze media coverage of the SGR project in Kenya. Identify the most common factual errors about the loan terms and provide corrections with sources."
