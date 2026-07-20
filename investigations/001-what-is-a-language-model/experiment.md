# experiment

## objective

the purpose of these experiments was to investigate a single question:

> how much does context influence the way a language model interpretes language?

this investigation wasn't designed to measure the mode's intelligence, factual accuracy, or reasoning ability in general. it is focused on something much narrower. if the model's only training objective is to predict the next token, then changing the surrounding context should consistently change what it predicts next

the experiments were designed to observe whether that expectation holds in practice

---

## experiments

### experiment 1 - ambiguous word: "bat"

**purpose**

observe whether surrounding context changes the interpretation of an ambiguous word

**prompts**

> he grabbed the bat before stepping up to the plate
>
> he grabbed the bat before it flew out of the cave

**observation**

the interpretation changed completely even though the ambiguous word remained the same. nearby context provided enough information to distinuish between a baseball bat and the animal

---

### experiment 2 - ambiguous word: "seal"

**purpose**

repeat the ambiguity test with a different word

**prompts**

> the seal slid off the rock into the water
>
> the seal on the envelope was broken

**observation**

again, the surrounding context was sufficient to resolve the ambiguity without changing the word itself

---

### experiment 3 - pronoun resolution

**purpose**

observe whether context changes the interpretation of an otherwise identical sentence

**prompts**

> the trophy didn't fit in the suitcase because it was too big
>
> the trophy didn't fit in the suitcase because it was too small

**observation**

changing a single adjective changed which object the pronoun referred to. the grammatical structure remained unchanged, suggesting that interpretation depends on more than syntax alone

---

### experiment 4 - sarcasm

**purpose**

test whether context changes the interpretation of identical wording

**prompts**

> i waited two hours in the rain for the bus. what a great start to the day
>
> i finally got the promotion i've been working toward for years. what a great start to the day

**observation**

the final sentence remained identical in both prompts, yet the model interpreted one as sarcasm and the other as sincere. the surrounding situatio determined the reading

---

### experiment 5 - missing context

**purpose**

observe the model's behavior when context is intentionally removed

**prompts**

> that's cold
>
> i told him about the accident and he laughed. that's cold

**observation**

without context, the model responded cautiously and offered multiple interpretations. once context was supplied, the response became specific and considerably more confident

---

### experiment 6 - competing contextual clues

**purpose**

test whether one misleading clue outweighs several consistent clues

**prompts**

> the bank was flooded after the storm, and the tellers had to be evacuated 
>
> the current at the bank was too strong for anyone to stand near the water 

**observation**

the model appeared to favour the interpretation supported by the strongest overall collection of contextual evidence rather than a single potentially misleading word

---

### experiment 7 - ambiguous word: "current"

**purpose**

repeat the ambiguity test using technical and non-technical meanings

**prompts**

> check the current before you touch that wire
>
> the current pulled the swimmer further from shore

**observation**

the surrounding context consistently determined whether "current" referred to electricity or moving water

---

### experiment 8 - minimum useful context

**purpose**

observe how little context is required before ambiguity disappears

**prompts**

> spring
>
> the spring
>
> the spring in the mattress
>
> the spring by the mountain

**observation**

very little context was needed before the model settled on a specific interpretation. a short contextual phrase was often sufficient

---

## recurring patterns

across these experiments, context consistently influenced interpretation more than isolated words did

ambiguous words rarely remained ambiguous once informative context was introduced

pronoun resolution appeared to depend on semantic plausibility rather than gramatical structure alone

when context was absent, the model often became more cautious instead of confidently selecting one interpretation

in these experiments, a small number of highly informative contextual clues were often sufficient to resolve ambiguity

---

## limitations

these experiments were performed using an instruction-tuned assistant rather than a raw base language model

the experiments are intentionally small and qualitative. they demonstrate observable behaviour but cannot explain the internal mechanisms responsible for that behaviour

the prompts were deliberately simple and should not be assumed to represent all forms of language or all possible contextual relationships

the observations support the claim that context strongly influences interpretation, but they do not establish how that information is represented internally

## new questions

does the model build an internal representation of the world, or is real-world plausibility an emergent consequence of learning language patterns?

why are some contextual clues more influential than others?

how much context is actually necessary before additional context stops improving interpretation?

does instruction tuning make the model more cautious when context is insufficient, or would a base language model behave differently?

what internal mechanism allows the model to combine many contextual clues into a single interpretation?


