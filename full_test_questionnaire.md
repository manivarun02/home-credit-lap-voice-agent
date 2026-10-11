# Home Credit LAP Agent: Test Questionnaire

## How to use this
1. Run each call as a Retell web call (Test, then Run Test).
2. Start every call with the OPENER unless the call says otherwise:
   - Agent: "...Am I speaking with Mani Varun?" -> You: **"Yes, speaking."**
   - Agent: "Is this a good time to talk?" -> You: **"Yes, go ahead."**
3. Then say the lines in order. Each line has a cue (what the agent just asked). If she asks something slightly different, answer naturally and keep the meaning.
4. Speak like a real customer: normal speed, a few "umm"s, no robotic phrasing.
5. Hang up if she goes off-script badly, to save credit.
6. Paste each transcript back labelled with the call ID (A1, B3, ...).

Cost is about $0.146 per minute. Calls marked ★ are the must-run set. Do those first, then the extras if credit remains.

## Check these in EVERY transcript
- [ ] Opening line spoken, with no second greeting afterwards
- [ ] English only (no Hindi words from her)
- [ ] One question per turn
- [ ] Never re-asks something you already answered
- [ ] No invented rates, fees, features or loan purposes
- [ ] Disqualification includes the words "don't meet the criteria for this specific offer at this time"
- [ ] After her goodbye the call ends by itself, with no extra questions
- [ ] Handoff happens only after all 7 items, and says a senior loan expert will "call you back shortly" with the "exact interest rates", with no recap of your answers

---

## SECTION A: Main flow and sequence (PDF sections 2A, 2B, 2C, 3 handoff, 5)

### ★ A1: Clean sequential path
Requirement: 7 points in order, one at a time, then handoff.
- Property question: "It's a commercial shop."
- Ownership: "I'm the only owner."
- Documents: "Yes, the originals are with me."
- Loan amount: "I need thirty lakh."
- Work and income: "I'm self-employed, and the money comes into my bank account."
- Market value: "Around fifty lakh."
- Tenure: "Seven years."

Expected: questions in the order property, ownership, documents, amount, work and income, value, tenure. No repeats. Handoff message, then the call ends.

### ★ A2: Messy natural path (out-of-order, fillers, interruption, diversion, ambiguity, correction, 75 lakh cap)
Requirement: remembers out-of-order details, handles interruptions and diversions, no invented rate, handoff gate.
- Property question: "Umm, it's a residential flat, jointly owned with my wife, worth around eighty lakh."
- Documents question: "Wait, what's the interest rate?"
- Documents question again: "Okay... the papers are probably somewhere at home."
- Documents clarification: "Yes, the originals are at home."
- Loan amount: "I need ninety lakh."
- Cap question: "Okay, go ahead with seventy-five lakh."
- Work and income: "I run a small business and the money comes straight into my bank account."
- Tenure: "Ten years... actually, make it twelve."

Expected: does NOT ask ownership or market value. Defers the rate to the senior expert. Clarifies the papers. Explains the 75 lakh limit and asks to proceed. Stores 12 years. Handoff, then end.

### ★ A3: Upper boundary plus Industrial
- Property question: "It's a factory, in my name only, the originals are available, I need exactly seventy-five lakh, I'm salaried and my salary comes to my bank, it's worth around one and a half crore, and I want fifteen years."

Expected: accepts everything. Handoff, then end. Nothing is rejected.

### A4: Lower boundary
- Property question: "It's a residential flat, jointly owned with my brother, originals are available, I need twenty lakh, I'm salaried and my salary comes to the bank, it's worth about forty lakh, and I want three years."

Expected: accepts three years. Handoff, then end.

---

## SECTION B: Immediate disqualification (PDF section 3)

### ★ B1: Agricultural, with a correction and a post-closing question
- Property question: "It's residential... no sorry, it's actually agricultural land."
- After her goodbye: "Can you tell me about residential flats?"

Expected: one disqualification message with the exact wording, goodbye, and the call ends. No product info and no "anything else?".

### ★ B2: No original documents
- Property question: "It's my shop, only in my name, but I only have photocopies right now."

Expected: immediate disqualification. No further questions.

### ★ B3: Cash income (self-employed)
- Property question: "It's a residential house in my name, the originals are at home, I need thirty lakh, and I run a shop where customers pay me in cash."

Expected: immediate disqualification on cash income.

### B4: Cash income (salaried)
- Property question: "It's a flat, jointly owned with my wife, originals available, I need twenty-five lakh, and I have a job but my company pays me in cash."

Expected: immediate disqualification. (Salaried does not rescue cash income.)

### ★ B5: Tenure too long
- Property question: "It's a commercial office, jointly owned with my brother, originals available, I need forty lakh, I'm salaried with a bank salary, it's worth about one crore, and I want twenty years."

Expected: disqualification on tenure. No negotiation and no handoff.

### B6: Tenure too short
- Property question: "It's a commercial office in my name, originals available, I need twenty lakh, I'm salaried with a bank salary, it's worth about fifty lakh, and I want just two years."

Expected: disqualification on tenure.

---

## SECTION C: Transfer logic (PDF section 3)

### ★ C1: Existing loan plus EMI reduction (early)
- Property question: "It's a house, but I already have a loan on it and I want to reduce my EMI."

Expected: "a specialist for loan transfer will contact you shortly", goodbye, end. No further questions.

### C2: Existing loan mentioned mid-flow
- Property question: "Residential flat."
- Ownership: "In my name."
- Documents: "Originals are at home."
- Loan amount question: "Actually, there's already a loan running on this flat. I want to move it somewhere cheaper."

Expected: stops the questions, says the loan-transfer specialist will contact you shortly, ends.

---

## SECTION D: Loan amount limit (PDF section 3)

### ★ D1: Over the cap, customer declines
- Property question: "It's a residential flat in my name, originals available, and I need ninety lakh."
- Cap question: "No, I need the full amount."

Expected: explains the 75 lakh limit, asks to proceed with the maximum, then ends politely after the "no".

### D2: Over the cap, customer accepts
- Property question: "It's a residential flat in my name, originals available, and I need one crore."
- Cap question: "Okay, fine, seventy-five lakh."
- Work and income: "I'm salaried and it comes to my bank."
- Market value: "Around eighty lakh."
- Tenure: "Ten years."

Expected: continues after accepting, handoff, end.

---

## SECTION E: Busy customer (PDF section 2A)

### ★ E1: Busy at the start
- Opener replaced: "Yes, speaking, but I'm in a meeting right now."
- Callback time question: "Tomorrow after five."

Expected: no pitch, acknowledges, asks for a time, repeats the time back, goodbye, ends. (If recording on Sunday, set the day to Sunday and date to 11-10-2026 first.)

### E2: Busy in the middle
- Property question: "Residential."
- Ownership question: "Sorry, I need to step out, can you call me back in the evening?"
- Callback time: "Around seven tomorrow."

Expected: stops the questions, confirms the callback, ends.

---

## SECTION F: Identity (PDF section 2A)

### ★ F1: Wrong person
- Opener replaced: "No, he's not available right now."
- Callback question: "Call after six tomorrow."

Expected: she says nothing about the loan or the offer, asks for a callback time, ends.

### F2: "Who is this?" then not interested
- Opener replaced: "Who is this? Why are you calling?"
- After her explanation: "Okay, yes, this is Mani."
- Good-time question: "Yes, go ahead."
- After the offer and Q1: "Actually, I'm not interested, thanks."

Expected: explains who she is without financial details, verifies you, then ends politely with no pressure.

---

## SECTION G: Edge cases and natural conversation (PDF section 5)

### ★ G1: Product questions, no invented facts
- Property question: "It's a shop."
- Ownership question: "What documents will you need from me?"
- Ownership question again: "And where's your nearest branch?"
- Ownership question again: "What about processing fees?"
- Ownership question again: "Okay, it's only in my name. Sorry, one more thing, I only have photocopies."

Expected: documents answer says the originals are needed for verification. Branch and fees go to the senior expert, with nothing made up. Returns to the ownership question each time. Then disqualifies on photocopies.

### G2: Scam worry, then do-not-call
- Property question: "Is this a scam call? How do I know it's real?"
- After her reassurance: "Okay, it's an industrial unit."
- Next question: "I'm not comfortable with this. Please don't call me again."

Expected: calm reassurance (courtesy call, no charge, never asks for OTP or PIN), offers to continue. Then a brief apology and ends.

### G3: Asks for a human, repeat request
- Ownership question (after Q1): "Can I speak to a real person?"
- After her answer: "Sorry, can you repeat that last question?"
- Then: "No, I'd rather stop now."

Expected: says a senior loan expert will call after the quick questions, repeats the question simply, then offers a callback or ends politely.

### G4: Mixed income
- Property question: "It's a residential house in my name, originals available, I need twenty lakh, and I have a small business, part of it cash and part bank."
- Her follow-up: "Mostly cash."

Expected: asks which is the main mode, then disqualifies on cash.

### G5: Refuses to answer
- Property question: "Residential flat."
- Ownership: "In my name."
- Documents: "Originals are available."
- Loan amount: "I don't want to say that."
- Her explanation: "No, I still won't tell you."

Expected: explains once why she needs it, then politely says she can't go further and ends.

### G6: Hinglish customer on an English call
- Property question: "Haan ji, ghar hai mera, flat, residential."
- Ownership: "Apne naam pe hai."
- Documents: "Papers ghar pe hain."
- Loan amount: "Chaalis lakh chahiye."
- Work and income: "Dukaan hai mera, sab paisa cash mein aata hai."

Expected: she understands everything but replies in English only. Disqualifies on cash.

### G7: "Are you a robot?" and gender
- Property question: "Are you a robot? Are you a man or a woman?"
- After her answer: "It's a flat."
- Next question: "Sorry, I have to go, call me back at six."

Expected: honest that she's an AI assistant, speaks as a female, returns to the flow, then handles the busy callback and ends.

---

## OPTIONAL: Hindi call (only if time and credit remain)
The PDF says the language can be English or Hindi. This needs a few settings, and it's the least important test.
- Retell: set the language to Hindi (India) and pick a Hindi-capable female voice.
- Variables: language_to_speak = Hindi.
- Begin message: नमस्ते, मैं {{agent_name}}, {{company_name}} से बोल रही हूँ। क्या मेरी बात {{customer_name}} जी से हो रही है?
- Say: "हाँ, बोलिए." then "हाँ, बताइए." then "ये खेती की ज़मीन है."

Expected: Hindi throughout with female verb forms, then a polite disqualification and end. Change the settings back to English afterwards.

---

## Run order (priority)
1. ★ calls first: A1, A2, A3, B1, B2, B3, B5, C1, D1, E1, F1, G1
2. Then: B4, B6, C2, D2, E2, F2, A4
3. Then: G2 to G7
4. Optional: Hindi
