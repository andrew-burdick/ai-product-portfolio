# AI glossary: in my own words

Plain-English definitions of the concepts I use across this portfolio, with why each matters for AI product decisions.

| Term | What it means | Why it matters for a product lead |
| --- | --- | --- |
| Large language model (LLM) | A model trained on vast amounts of text that generates responses by predicting the most likely next words; it does not look facts up | It can sound confident while being wrong, so any product needing accurate facts must supply trusted sources |
| Token | A unit of text the model reads and writes, roughly three-quarters of a word | Cost is charged per token and limits how much fits in the context window, so usage and answer length drive cost |
| Training vs inference | Training builds the model once, at great expense, and is done by the vendor; inference is each use of the model to generate an answer | You pay for inference on every interaction, so operating cost grows with usage |
| Knowledge cutoff | The date after which the model has no training data; private information is never in training data at all | Current or internal information, such as fees and policies, must be supplied at the time of the question |
| Probabilistic output | The model may give different answers to the same question, because it generates rather than retrieves | One good test proves little; quality must be tested across many questions and monitored after launch |
| Context window | The model's working memory for one request: instructions, conversation so far, documents, the question and the answer, all measured in tokens; nothing carries over between requests | Everything in the window is paid for on every call, so long conversations and large documents multiply cost and slow responses |
| System prompt | The standing instructions that set the assistant's role, tone, scope and refusal rules | Treat it like product requirements: owned, version-controlled, risk-approved and re-tested on every change, because one edit changes behaviour across every conversation |
| Context engineering | Deciding what goes into the context window: which documents, how much history, which examples and instructions | More is not better; the right context improves accuracy while controlling cost and latency |
| Grounding | Giving the model trusted source material in its context, so its answer is based on that material rather than its training memory | Reduces hallucination and makes answers auditable, but only if the source documents themselves are accurate and current |
| Retrieval | The search step that finds the right documents for each question from a larger library | If retrieval picks the wrong or outdated document, the model will confidently answer from it, so retrieval quality is a product risk, not just a technical detail |
# AI glossary: in my own words

Plain-English definitions of the concepts I use across this portfolio, with why each matters for AI product decisions.

| Term | What it means | Why it matters for a product lead |
| --- | --- | --- |
| Large language model (LLM) | A model trained on vast amounts of text that generates responses by predicting the most likely next words; it does not look facts up | It can sound confident while being wrong, so any product needing accurate facts must supply trusted sources |
| Token | A unit of text the model reads and writes, roughly three-quarters of a word | Cost is charged per token and limits how much fits in the context window, so usage and answer length drive cost |
| Training vs inference | Training builds the model once, at great expense, and is done by the vendor; inference is each use of the model to generate an answer | You pay for inference on every interaction, so operating cost grows with usage |
| Knowledge cutoff | The date after which the model has no training data; private information is never in training data at all | Current or internal information, such as fees and policies, must be supplied at the time of the question |
| Probabilistic output | The model may give different answers to the same question, because it generates rather than retrieves | One good test proves little; quality must be tested across many questions and monitored after launch |
| Context window | The model's working memory for one request: instructions, conversation so far, documents, the question and the answer, all measured in tokens; nothing carries over between requests | Everything in the window is paid for on every call, so long conversations and large documents multiply cost and slow responses |
| System prompt | The standing instructions that set the assistant's role, tone, scope and refusal rules | Treat it like product requirements: owned, version-controlled, risk-approved and re-tested on every change, because one edit changes behaviour across every conversation |
| Context engineering | Deciding what goes into the context window: which documents, how much history, which examples and instructions | More is not better; the right context improves accuracy while controlling cost and latency |
| Grounding | Giving the model trusted source material in its context, so its answer is based on that material rather than its training memory | Reduces hallucination and makes answers auditable, but only if the source documents themselves are accurate and current |
| Retrieval | The search step that finds the right documents for each question from a larger library | If retrieval picks the wrong or outdated document, the model will confidently answer from it, so retrieval quality is a product risk |
| RAG (retrieval-augmented generation) | The full flow of retrieving relevant documents, placing them in the context, and generating an answer from them | Lets a model answer on current and private information without retraining; quality depends on both the documents and the retrieval |
| Hallucination | A fluent, confident output that is factually wrong | Wrong answers don't look wrong, so in banking they create conduct and complaints risk; layered guardrails and evaluation are essential |
| Refusal rule | An instruction telling the model to say it doesn't know, or to decline, when the answer isn't in its sources or the request is out of scope | A clear "I can't find that, please ask a banker" is safer than a confident guess; refusal correctness should be tested |
| Model routing | Sending each request to the most suitable model: simple questions to a small, fast, cheap model, complex ones to a more capable model | Balances cost, speed and quality, and turns the "cheapest vs best model" debate into an evidence-based design choice |
| Guardrail metric | A measure watched alongside the main success metric to make sure improving one thing doesn't harm another | Stops a team "succeeding" harmfully, e.g. cutting complaint wait times while complaint volumes quietly rise |