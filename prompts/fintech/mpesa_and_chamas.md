# Fintech Prompts — M-Pesa, Chamas, Mobile Money

> Adapted from 1337 Use Cases for ChatGPT (Section 5.4-5.5: Banking & Financial Services)
> East African context: Kenya M-Pesa ecosystem, chama (rotating credit) groups, USSD-based banking

---

## 5.4.1 Mobile Money Transaction Initiation

**General prompt:**
"How do I send money via M-Pesa to pay for [service]?"

**Formula:**
"I want to [send/receive/withdraw] KES [amount] [via M-Pesa/via Till/via Paybill] for [purpose] from [sender context] to [recipient context]."

**East Africa examples:**
- "I want to send KES 2,500 via M-Pesa to Paybill 247247 for my KPLC electricity bill."
- "I want to withdraw KES 5,000 from my M-Pesa to cash at an agent in Kibera."
- "I want to transfer KES 15,000 via M-Pesa to my chama account for this month's contribution."

**Swahili variant:**
- "Ninataka kutuma shilingi elfu mbili kupitia M-Pesa kwa [mtu/kampuni]."

---

## 5.4.2 Chama (Rotating Credit Group) Management

**General prompt:**
"How do I track contributions and distributions for a rotating savings group?"

**Formula:**
"I am managing a chama with [number] members who contribute KES [amount] [weekly/monthly]. Help me [track contributions/calculate the payout schedule/manage the merry-go-round order]."

**East Africa examples:**
- "I am managing a chama with 12 members who contribute KES 5,000 monthly. Help me calculate the payout schedule for 12 months and track who has received their share."
- "My table banking group has 30 members. Each contributes KES 1,000 weekly. Calculate the interest earned over 6 months at 10% and the total loan book."
- "Help me draft the constitution for a chama with 20 members, monthly contributions, and a loans facility at 10% interest per month."

---

## 5.5.2 Financial Planning for Kenya Context

**General prompt:**
"What are the best strategies for saving money in Kenya with limited formal banking access?"

**Formula:**
"I earn KES [monthly income] and have [fixed expenses]. I want to [save for goal] in [timeframe]. What combination of [M-Pesa savings/SACCO/chama/bank] should I use?"

**East Africa examples:**
- "I earn KES 45,000 monthly as a teacher in Nakuru. I want to save KES 200,000 for school fees in 18 months. Which combination of M-Pesa Lock Savings and a SACCO works best?"
- "I am a boda boda rider in Kisumu earning roughly KES 800 per day. How do I save for a new motorcycle in 12 months?"
- "I am in the Kenyan diaspora sending $300/month home. What is the most cost-effective combination of Wise, M-Pesa Global, and a Kenya SACCO?"

---

## 5.10.7 Financial Analysis for East African Businesses

**General prompt:**
"Analyze the financial health of a small business in Kenya."

**Formula:**
"I run a [business type] in [location, Kenya]. My monthly revenue is KES [amount], costs are KES [amount]. Help me [analyze cash flow/calculate break-even/plan for expansion]."

**East Africa examples:**
- "I run a posho mill in Eldoret. Monthly revenue KES 80,000, costs KES 55,000. Should I buy a second machine at KES 350,000 or expand the grain storage?"
- "I own a matatu on the Nairobi-Thika route. Daily revenue KES 8,000, daily costs KES 5,500. Calculate my payback period on a KES 1.2M vehicle loan."
- "My M-Pesa agent float is KES 50,000. Daily transaction volume is KES 300,000. Analyze my float utilization and suggest an optimal float size."

---

## mpesa-mcp Integration Prompts

These prompts are designed for use with [mpesa-mcp](https://github.com/gabrielmahia/mpesa-mcp):

**STK Push (Customer to Business):**
```
Initiate an M-Pesa STK push for KES [amount] to phone [254XXXXXXXXX] 
with account reference [reference] for [description].
Confirm the transaction ID and timestamp.
```

**B2C Payment:**
```
Send KES [amount] from the business shortcode to phone [254XXXXXXXXX]
as [salary/refund/award]. Log the transaction with the audit trail.
```

**Transaction Status Check:**
```
Check the status of M-Pesa transaction [CheckoutRequestID].
Return the result code, description, and amount confirmed.
```
