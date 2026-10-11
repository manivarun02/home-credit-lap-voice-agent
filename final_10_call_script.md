# Final 10 Calls: Turn-by-Turn Script

How to read this:
- **AI** = what the agent should say. The wording will vary, so judge the meaning and the **bold key points**.
- **YOU** = exactly what you say. Say it naturally, a little "umm" is fine.
- Wait for the agent to finish each line before you speak.
- After a goodbye the call should end by itself. If it doesn't, note it.

Every call starts the same way:

AI: "Hello, this is Rina calling from Home Credit. Am I speaking with Mani Varun?"
YOU: "Yes, speaking."
AI: asks if it's a good time to talk for a couple of minutes.
YOU: "Yes, go ahead."
AI: thanks you as a **valued customer** with a **pre-approved Loan Against Property offer of up to seventy-five lakh rupees**, says it needs a few quick questions, and in the same turn asks the **property type** (residential like a house or flat, commercial like a shop or office, industrial like a factory).

(Calls 4 and 9 below change this opening where noted.)

---

## Call 1: Agricultural property (disqualify + hard stop)
YOU: "It's residential... no sorry, it's actually agricultural land."
AI: understands the **latest answer is agricultural**. **One turn:** kindly says that, going by this, you **don't meet the criteria for this specific offer at this time** (may mention the offer isn't available for agricultural property), thanks you, says goodbye. **Call ends.**
YOU (after her goodbye): "Can you tell me about residential flats?"
AI: at most a very short goodbye, or the call has already ended.

Critical checks:
- [ ] Used the final answer (agricultural), not "residential"
- [ ] Wording includes "don't meet the criteria for this specific offer at this time"
- [ ] No "anything else I can help with", no product info about flats
- [ ] Call ended by itself

---

## Call 2: Existing loan and EMI reduction (transfer)
YOU (property question): "It's a house, but I already have a loan on it and I want to reduce my EMI."
AI: acknowledges, says a **specialist for loan transfer will contact you shortly**, thanks you, says goodbye. **Call ends.**

Critical checks:
- [ ] Asks **no** further questions (no ownership, documents, amount)
- [ ] Says the loan-transfer specialist will contact you shortly
- [ ] Did not ask "do you have an existing loan?" herself before you mentioned it
- [ ] Call ended by itself

---

## Call 3: 90 lakh requested, customer declines the cap
YOU (property question): "It's a residential flat in my name, originals available, and I need ninety lakh."
AI: takes in residential, sole owner, originals available, amount ninety lakh. **Does not ask ownership or documents.** Explains the offer goes **up to seventy-five lakh** and **asks if you'd like to go ahead with that maximum**.
YOU: "No, I need the full amount."
AI: thanks you politely, wishes you well, says goodbye. **Call ends.**

Critical checks:
- [ ] Explained the 75 lakh limit and asked about proceeding with the maximum
- [ ] Did not reject you straight away on hearing 90 lakh
- [ ] Did not re-ask ownership or documents
- [ ] Ended politely after your "no"

---

## Call 4: Busy customer (callback)
Change the opening: after her "Am I speaking with Mani Varun?" say:
YOU: "Yes, speaking, but I'm in a meeting right now."
AI: acknowledges ("Of course, no problem"), asks **what time would suit for a callback**. **No pitch, no offer.**
YOU: "Tomorrow after five."
AI: **repeats the callback back** (tomorrow, after 5 PM, ideally Sunday if you're testing on Saturday), thanks you, says goodbye. **Call ends.**

Critical checks:
- [ ] Did not explain the loan offer
- [ ] Asked for a callback time and repeated it back once
- [ ] Understood "tomorrow" correctly
- [ ] Call ended by itself

---

## Call 5: Photocopies only (no original documents)
YOU (property question): "It's my shop, only in my name, but I only have photocopies right now."
AI: takes in commercial, sole owner, **no originals**. **One turn:** says you **don't meet the criteria for this specific offer at this time** (original documents are needed), thanks you, goodbye. **Call ends.**

Critical checks:
- [ ] Disqualified immediately, no further questions
- [ ] Did not re-ask property type or ownership
- [ ] Wording includes the "criteria for this specific offer" line

---

## Call 6: Cash income
YOU (property question): "It's a residential house in my name, the originals are at home, I need thirty lakh, and I run a shop where customers pay me in cash."
AI: takes in all of it. Spots **cash income** and **disqualifies at once**: you **don't meet the criteria for this specific offer at this time**, thanks, goodbye. **Call ends.**

Critical checks:
- [ ] Disqualified on cash income without asking market value or tenure
- [ ] Did not re-ask anything you already said
- [ ] Self-employed was not the reason, cash was

---

## Call 7: Tenure of 20 years
YOU (property question): "It's a commercial office, jointly owned with my brother, originals available, I need forty lakh, I'm salaried with a bank salary, it's worth about one crore, and I want twenty years."
AI: takes in everything. Notices **twenty years is outside three to fifteen** and **disqualifies**: you **don't meet the criteria for this specific offer at this time**, thanks, goodbye. **Call ends.**

Critical checks:
- [ ] Did **not** give the handoff message
- [ ] Did not ask you to change the tenure or offer a workaround
- [ ] Joint ownership and 40 lakh did not cause any problem

---

## Call 8: Upper boundary plus Industrial (should qualify)
YOU (property question): "It's a factory, in my name only, the originals are available, I need exactly seventy-five lakh, I'm salaried and my salary comes to my bank, it's worth around one and a half crore, and I want fifteen years."
AI: accepts **everything**: industrial is eligible, 75 lakh exactly is fine, 15 years is fine. Asks nothing further. **Handoff:** thanks you, says a **senior loan expert will call you back shortly to give the exact interest rates**. Goodbye. **Call ends.**

Critical checks:
- [ ] Nothing was rejected (75 lakh and 15 years are inside the limits)
- [ ] All 7 points were captured from one reply, with no repeated questions
- [ ] Handoff says "call you back shortly" and "exact interest rates"
- [ ] No recap of your answers, no promise of approval

---

## Call 9: Clean question-by-question path (order test)
After the opening, answer **only what she asks**, one at a time:

AI: property type?
YOU: "It's a commercial shop."
AI: **ownership** (only owner, or joint)?
YOU: "I'm the only owner."
AI: **original documents** ready for verification?
YOU: "Yes, the originals are with me."
AI: **loan amount**?
YOU: "I need thirty lakh."
AI: **salaried or self-employed, and bank or cash**?
YOU: "I'm self-employed, and the money comes into my bank account."
AI: **market value**?
YOU: "Around fifty lakh."
AI: **tenure**?
YOU: "Seven years."
AI: **handoff** (senior loan expert will call you back shortly, exact interest rates). Goodbye. **Call ends.**

Critical checks:
- [ ] Order is property, ownership, documents, amount, work and income, value, tenure
- [ ] One question per turn
- [ ] Short reaction before each next question (sounds human)
- [ ] Handoff only after all seven

---

## Call 10: Messy natural path (out-of-order, diversion, ambiguity, correction, cap)
After the opening:

YOU: "Umm, it's a residential flat, jointly owned with my wife, worth around eighty lakh."
AI: acknowledges. **Next question is the documents** (it must NOT ask ownership or market value).

YOU: "Wait, what's the interest rate?"
AI: says the **senior loan expert will share the exact rate** after the quick check. **No number.** Returns to the documents question.

YOU: "Okay... the papers are probably somewhere at home."
AI: does **not assume**; asks to confirm the original documents are available for verification.

YOU: "Yes, the originals are at home."
AI: asks the **loan amount**.

YOU: "I need ninety lakh."
AI: explains the **75 lakh limit** and asks if you'd like to go ahead with seventy-five lakh.

YOU: "Okay, go ahead with seventy-five lakh."
AI: continues. Next is **work and income** (market value was already given, so it is not asked again).

YOU: "I run a small business and the money comes straight into my bank account."
AI: asks the **tenure**.

YOU: "Ten years... actually, make it twelve."
AI: **handoff**: senior loan expert will call you back shortly with the exact interest rates. Goodbye. **Call ends.**

Critical checks:
- [ ] Did not ask ownership or market value after you gave them
- [ ] No invented interest rate, and returned to the question after the diversion
- [ ] Clarified the vague "papers are somewhere" answer
- [ ] Explained the cap, and carried on after you agreed
- [ ] Took 12 years (the correction), not 10
- [ ] Handoff only at the very end

---

## After the 10 calls
- Paste every transcript in one message, labelled "Call 1" to "Call 10".
- Add a note next to any call where something felt off (voice problem, long pause, she talked over you).
- Don't edit the prompt between calls. If you must, tell me, because the test values get wiped.
