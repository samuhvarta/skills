# ASD-STE100 rules

ASD-STE100 (Simplified Technical English) is a controlled language. It was made for aerospace maintenance documents. The user chooses one of two levels. Apply these rules to all prose, list items, table cells, and diagram labels.

- **Hard:** all rules in [Sentences](#sentences) and [Structure](#structure); one name for one thing; no contractions; noun clusters of three words or less.
- **Soft:** all other rules in [Words](#words).

## Levels

**Strict conformance**

- Apply as much of the specification as possible. Treat the soft rules as hard rules.
- Use only approved words, with their approved meaning and part of speech. Use technical names as they are. If no approved word fits, use the simplest word and keep it the same through the document.
- Do not use "-ing" forms (except technical names), phrasal verbs, or contractions.
- Keep to the sentence and paragraph limits. Write one instruction per sentence.
- Do not combine sentences to make the text shorter. Short sentences are correct in this level.
- Use the active voice and simple tenses everywhere. Use articles and demonstratives before nouns.

**Optimize for brevity**

- Apply the hard rules always. Apply the soft rules where they do not make the text less natural. Use a common "-ing" form, phrasal verb, or second meaning of a word if the STE form is clumsy.
- Combine two short sentences that carry sparse ideas into one sentence. Keep the result inside the sentence length limits and keep one instruction per sentence.
- Example: "ABC is a new product. ABC is hosted on the XYZ platform." becomes "ABC is a new product hosted on the XYZ platform."
- Do not combine sentences when the result has more than one topic, breaks a length limit, or hides a condition.

## Words

- Use approved words with one meaning only. Example: use "close" as the opposite of "open", not as "near".
- Use a word as the part of speech the dictionary gives. Example: "test" is a noun and a verb. "Monitor" is a noun only, so write "examine" or "look at" for the verb.
- Use technical names (part names, API names, file names) as they are. Write them in `code` when they are identifiers.
- Use one name for one thing. Do not use synonyms for the same thing.
- Use the simple verb forms: infinitive, imperative, simple present, simple past, simple future, past participle as an adjective.
- Do not use "-ing" forms, except in technical names.
- Do not use phrasal verbs. Example: write "start", not "set up" or "kick off".
- Do not use contractions. Write "do not", not "don't".
- Keep noun clusters to a maximum of three words. Break longer clusters with "of" or a short clause.
- Use articles ("the", "a") and demonstratives ("this", "these") before nouns where possible.

## Sentences

- Procedural sentences: maximum 20 words.
- Descriptive sentences: maximum 25 words.
- Write one instruction per sentence. Two actions at the same time can go in one sentence.
- Use the active voice in procedures. Use the active voice in descriptions where possible.
- Write instructions in the imperative ("Close the valve"), not as statements ("The valve should be closed").
- Put a condition first: "If the test fails, stop the service."
- Write one topic per paragraph. A paragraph has a maximum of six sentences.

## Structure

- Use a numbered list for a procedure. Use a bulleted list for items with no sequence.
- Start a description with the most important information.
- Write warnings and cautions as a clear command, then give the reason in one short sentence.

## Checklist

Each sentence passes when all answers to the hard questions are "yes":

1. Is the sentence 20 words or less (procedure) or 25 words or less (description)?
2. Does it have one instruction only?
3. Is it in the active voice, with a simple tense?
4. Does it have no contractions?
5. Are noun clusters three words or less?
6. Is each thing called by the same name as in the rest of the document?

Soft question: does each word have one meaning, with few "-ing" forms and phrasal verbs?

- In **strict conformance**, treat the soft question as hard. A "no" is not acceptable.
- In **optimize for brevity**, a "no" is acceptable only when the STE form is clumsy.

Style questions (both levels): does the text have no metaphor, no em dash, and no superlative without evidence?
