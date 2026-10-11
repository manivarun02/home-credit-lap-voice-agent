# Home Credit LAP Qualification Voice Agent

AI voice agent for **Home Credit** that calls existing customers about a pre-approved **Loan Against Property (LAP)** offer (up to 75 lakh), runs a 7-point eligibility check, handles diversions, disqualifies ineligible customers, detects loan-transfer cases, and hands qualified leads to a senior loan expert.

Built for the SalesAgents AI "Voice Agent Design" assignment.

## Deliverables
| Item | Location |
|---|---|
| System prompt (exact text used in the tested agent) | [`system_prompt.md`](system_prompt.md) |
| Call recordings + transcripts (audio and logs) | **<PASTE PUBLIC GOOGLE DRIVE LINK HERE>** |
| Test scripts used for the calls | [`tests/`](tests/) |

## Platform and setup
- **Voice platform:** Retell AI (single-prompt agent), web calls for testing
- **LLM:** GPT (selected in Retell), English (US) voice, female
- **Function:** `end_call` (hang-up)
- **Call settings:** End call on silence 10 s, max call duration 5 min
- **Prompt variables:** `company_name`, `customer_name`, `agent_name`, `agent_gender`, `current_date`, `current_day`, `current_time`, `additional_context_from_rag`, `language_to_speak`; `conversation_history` and `customer_utterance` are referenced by name (Retell supplies the live conversation itself)

Test values used: agent_name = Rina, agent_gender = female, company_name = Home Credit, customer_name = Mani Varun, language_to_speak = English, current_day / current_date = actual values on the test day, additional_context_from_rag = short sample product note (documents needed, tenure 3 to 15 years, senior expert gives interest rates, offer up to 75 lakh).

## How the prompt covers the assignment
| Assignment requirement | How it is handled |
|---|---|
| Verify the customer; busy customer gets a callback time | Opening line verifies identity; busy at any point leads to a callback request, read-back and end |
| Offer presented as a loyalty reward, up to 75 lakh | Offer + first question in one short turn |
| 7 data points, sequential | Property type, ownership, original documents, loan amount, occupation + income mode, market value, tenure; one question per turn |
| Out-of-order details are remembered and not re-asked | After every reply the agent takes in everything said and asks the first unanswered item |
| Immediate disqualification | Agricultural, no original documents, cash income, tenure under 3 or over 15 years: "you don't meet the criteria for this specific offer at this time", then the call ends |
| Transfer logic | Existing loan on the property or EMI reduction: "a specialist for loan transfer will contact you shortly", then end |
| Loan above 75 lakh | Explains the limit and asks whether to proceed with 75 lakh |
| Post-qualification handoff | Only after all 7 are answered: senior loan expert will call back shortly with the exact interest rates |
| Handoff gate | Skipped items are asked again before the handoff |
| Natural conversation | Handles full sentences, fillers, corrections, interruptions, diversions; no invented rates, fees or product facts (uses `additional_context_from_rag` only) |
| Variables and gender | All variables from the brief; `agent_gender` kept for the whole call |

## Test scenarios
Scripts are in `tests/`. Scenarios include: agricultural property (with a correction), existing loan / EMI reduction, 90 lakh requested (decline and accept), busy customer, photocopies only, cash income, tenure outside 3 to 15 years, boundary cases (exactly 75 lakh, 15 years), a clean sequential path, and a messy path with out-of-order answers, an interest-rate question, a vague answer and a correction.

## Known behaviour
The model sometimes speaks the complete closing message but does not invoke `end_call` in the same reply. As a safeguard the agent is configured with **End Call on Silence (10 s)**, so the call ends shortly after the closing message.

## Using the prompt
Paste `system_prompt.md` into a Retell single-prompt agent, set the nine variables above, add the `end_call` function, and start the call with this first message:

`Hello, this is {{agent_name}} calling from {{company_name}}. Am I speaking with {{customer_name}}?`
