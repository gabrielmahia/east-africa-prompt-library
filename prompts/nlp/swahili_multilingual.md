# NLP & Multilingual Prompts — Swahili AI, kenya-rag

> Adapted from 1337 Use Cases for ChatGPT (Section 19.6: NLP/ML, Section 4.20: Dependency Parsing)
> Ecosystem context: Masakhane AfriNLP, Cohere Tiny Aya (70 languages), AfriQA dataset

---

## Swahili Text Processing

**General prompt:**
"Analyze this Swahili text for [sentiment/entities/topics]."

**Formula:**
"Analyze the following Swahili text for [sentiment/named entities/topic classification/summarization]. Return results in [English/Swahili/both]. Handle [informal Swahili/Sheng/code-switching] appropriately.

Text: [input]"

**kenya-rag examples:**
- "Analyze the following Swahili parliamentary speech for: key policy positions, named entities (people, places, organizations), and sentiment toward the proposed bill. Return a structured JSON response."
- "Classify the topic of this Swahili tweet: 'Uchaguzi wa leo umekuwa na mambo mengi ya ajabu Nairobi CBD.' Return: topic, sentiment (positive/negative/neutral), and whether it contains political content."
- "Translate this mix of English and Swahili (code-switching) to clean English, preserving the meaning: 'Nimefika CBD lakini traffic ni too much today, sijui kama nitafika ofisini on time.'"

---

## Multilingual Document Intelligence

**General prompt:**
"Extract structured data from this multilingual document."

**Formula:**
"Extract [specific fields] from the following [document type] which may contain [language 1], [language 2], or [language 3]. Return as structured JSON. Handle: abbreviations, local terminology, and informal language."

**East Africa examples:**
- "Extract the following from this Kenyan court judgment (may contain English legal terminology and Swahili): case number, parties involved, charges, verdict, sentence, and judge's name. Return as JSON."
- "Parse this M-Pesa transaction SMS: 'QJZ4K7HK confirmed. Ksh1,500 sent to JOHN KAMAU 0722123456 on 24/5/26 at 3:14 PM. M-PESA balance is Ksh8,234.00.' Extract: transaction_id, amount, recipient, phone, timestamp, balance."
- "Summarize this NDMA drought bulletin in plain Swahili (200 words) for community radio broadcast in Marsabit County."

---

## Cohere Tiny Aya Integration

Tiny Aya (Feb 2026) — 70-language open model including Swahili, Somali, Amharic, Hausa, Yoruba, Zulu.
Available: HuggingFace, Kaggle, Ollama. Runs offline.

```python
# Swahili NLP with Tiny Aya (offline, privacy-preserving)
from transformers import pipeline

# Load Tiny Aya — Swahili-optimized variant
pipe = pipeline("text-generation", model="CohereForAI/aya-expanse-8b")

# Swahili sentiment analysis
result = pipe(
    "Changanua hisia za sentensi hii kwa Kiswahili: 'Serikali imefanya kazi nzuri sana kwenye mradi huu.'\n\nHisia: ",
    max_new_tokens=10
)

# Swahili → English translation
result = pipe(
    "Tafsiri sentensi hii kwa Kiingereza:\n'Mvua ya masika imechelewa mwaka huu, wakulima wana wasiwasi.'\n\nTranslation:",
    max_new_tokens=50
)
```

---

## kenya-rag Integration Prompts

For use with [kenya-rag](https://github.com/gabrielmahia/kenya-rag):

```
Index the following Kenyan legal documents and enable 
multilingual (English/Swahili) semantic search:
- Kenya Law Reports 2020-2025
- County Government Finance Acts
- KNBS Statistical Abstracts

Query: "vigezo vya kupata mkopo wa serikali" 
(Swahili query → retrieve English legal documents)
```

```
Build a RAG pipeline for Kenya Budget Statement 2026/27.
Enable queries in both English and Swahili.
Return cited excerpts with page references.
```
