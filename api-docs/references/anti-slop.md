# Anti-Slop Writing Guide

This reference combines guidelines from [humanizer](https://github.com/blader/humanizer) and [stop-slop](https://github.com/hardikpandya/stop-slop) for writing clear, human-sounding documentation.

## Core Principle

LLMs default to statistically common phrasing that sounds generic. Replace statistical likelihood with specificity: actual values, named components, concrete behavior.

## Quality Rubric (Score 1-10 each)

| Dimension | Question |
|-----------|----------|
| Directness | Does it state facts without softening? |
| Rhythm | Does sentence length vary naturally? |
| Trust | Does it respect reader intelligence? |
| Authenticity | Does it sound like a human wrote it? |
| Density | Can anything be cut? |

**Threshold:** Below 35/50 needs revision.

---

## Patterns to Avoid

### Banned Words & Phrases

**Throat-clearing openers (delete entirely):**
- "It's important to note that..."
- "It's worth mentioning that..."
- "Interestingly enough..."
- "As you may know..."
- "Let's dive into..."
- "Let's explore..."
- "In today's world..."

**Inflated significance (use plain language):**
- "pivotal" → important, key
- "testament to" → shows, demonstrates
- "landscape" → field, area, space
- "tapestry" → mix, combination
- "paradigm shift" → change
- "game-changer" → useful, helpful
- "cutting-edge" → new, recent
- "robust" → strong, reliable
- "leverage" → use
- "utilize" → use
- "facilitate" → help, enable
- "comprehensive" → complete, full
- "seamless" → smooth, easy
- "streamlined" → simple, fast

**Copula avoidance (just use "is/are/has"):**
- "serves as" → is
- "stands as" → is
- "acts as" → is
- "functions as" → is
- "represents" → is
- "constitutes" → is
- "boasts" → has
- "features" → has

**Filler phrases (delete or shorten):**
- "in order to" → to
- "due to the fact that" → because
- "at this point in time" → now
- "in the event that" → if
- "for the purpose of" → for, to
- "with regard to" → about
- "in terms of" → (delete or rephrase)
- "it should be noted that" → (delete)

**Hedging language (commit or delete):**
- "potentially"
- "arguably"
- "somewhat"
- "relatively"
- "fairly"
- "quite"
- "rather"
- "may or may not"

**Chatbot artifacts (delete):**
- "I hope this helps!"
- "Let me know if you have questions"
- "Feel free to ask"
- "Happy to help!"
- "Certainly!"
- "Absolutely!"
- "Great question!"

### Structural Patterns to Break

**Binary contrasts:**
```
BAD:  "It's not just X—it's Y"
BAD:  "More than just X, it's Y"
GOOD: State Y directly
```

**Rule of three:**
```
BAD:  "fast, reliable, and secure"
GOOD: Pick the two most relevant, or just one
```

**Dramatic fragmentation:**
```
BAD:  "The result? A complete transformation."
GOOD: Integrate into normal prose
```

**Rhetorical setup:**
```
BAD:  "What does this mean for developers? Everything."
GOOD: State the meaning directly
```

**Em-dash reveals:**
```
BAD:  "One thing matters most—performance"
GOOD: "Performance matters most"
```

**Explained metaphors:**
```
BAD:  "Think of it as a bridge—connecting A to B"
GOOD: Just say it connects A to B
```

---

## API Documentation Specifics

### Description Writing

**Bad (slop):**
> This powerful endpoint enables seamless integration with our comprehensive KMS infrastructure, providing robust cryptographic capabilities.

**Good (direct):**
> Get the encryption public key for an application. Used to encrypt environment variables before deployment.

### Parameter Descriptions

**Bad:**
> The identifier parameter serves as the primary means of uniquely identifying...

**Good:**
> Application ID (40-character hex string, with or without 0x prefix).

### Error Descriptions

**Bad:**
> In the event that authentication fails, the system will return an appropriate error response.

**Good:**
> Returns 401 if the API key is invalid or expired.

### Summary Writing

**Rule:** Maximum 6 words. Imperative verb + object.

| Bad | Good |
|-----|------|
| "This endpoint retrieves a list of..." | "List KMS instances" |
| "Allows users to create new..." | "Create CVM" |
| "Provides functionality for updating..." | "Update compose file" |

---

## Checklist Before Finalizing

- [ ] No sentences start with "It's important/worth noting"
- [ ] No "serves as", "acts as", "stands as" (use "is")
- [ ] No "in order to" (use "to")
- [ ] No rule-of-three lists (use two items or one)
- [ ] No em-dash dramatic reveals
- [ ] Summaries are ≤6 words
- [ ] Each description adds information (not just restating the name)
- [ ] Error messages state what happened, not what "may occur"
