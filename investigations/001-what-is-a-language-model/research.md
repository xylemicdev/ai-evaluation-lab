# research

## purpose

this investigation began with a simple question: if a language model is trained only to predict the next token, why does it appear to understand context so well?

the experiments established that relatively small changes in context consistently altered the model's behavior. this document examines how current explanations of language models account for those observations and where those explanations remain incomplete

## explaining the observations

### prediction creates pressure

at first glance, next-token prediction sounds like a surprisingly narrow objective. it appears to ask very little of the model: simply predict the next piece of text

however, the experiments suggest that this objective becomes much more demanding in practice

consider an ambiguous word such as "bank." predicting the correct continuation depends on whether earlier words refer to money, rivers, loans, water, or something else entirely. a model that ignored context would repeatedly make poor predictions across millions of similar examples

during training, the model is rewarded whenever its predictions become more accurate and penalized whenever they become less accurate. over an enormous amount of text, this creates continuous pressure to discover whatever regularities improve prediction

the model is never explicitly instructed to learn relationships between words. instead, learning those relationships becomes one effective way of succeeding at the objective it was actually given

in that sense, relationships are not a separate goal from prediction. they are one consequence of becoming exceptionally good at prediction

---

### reusable patterns instead of isolated examples

a language model is exposed to billions of examples during training

many of those examples express similar ideas using different words or different sentence structures

rather than treating every sentence as an unrelated event, the model benefits from developing reusable patterns that improve predictions across many different situations

for example, words such as "paycheck," "loan," "account," and "deposit" frequently appear in the contexts that make "bank" a likely continuation

from the outside, these reusable patterns often resemble concepts or relationships

this investigation does not establish exactly how those patterns are represented internally. it only suggests that reusing successful patterns provides a more effective strategy than treating every sentence independently

---

### why context changes meaning

the experiments repeatedly demonstrated that relatively small changes in surrouning words could completely change the model's interpretation

the words themselves did not change

only the context changed

this behavior follows naturally from the prediction objective

the probability of a word depends not only on the word immediately before it, but also on the broader context that came earlier in the sequence

as a result, context is not an additional feature layered onto prediction

it is part of the information required to make good predictions in the first place

---

### attention as an architectural solution

understanding why context matters explains only part of the picture

another question naturally follows:

> how can a model effectively use information that appeared many words earlier?

modern language models address this through the transformer architecture and its attention mechanism

rather than allowing earlier information to gradually disappear as more words are processed, attention allows different parts of the context to influence the current prediction directly

this investigation does not demonstrate how attention works internally

however, the observed behavior is consistent with the purpose attention was designed to serve: allowing context to remain useful throughout the prediction process

---

## connecting the observations to current understanding

before beginning this investigation, next-token prediction appeared to be a technically correct but incomplete description of language models

the experiments did not overturn that idea

instead, they gave it more depth

predicting the nextt token is not a shortcut around language

it is precisely because prediction depends on language that the model is continually encouraged to discover increasingly useful structure within it

the object remained simple

the behavior required to achieve that objective proved much richer that it first appeared

---

## limitations

this investigation observed behavior rather than internal computation

it does not establish whether the model understands language in the human sense

it does not identify the exact mechanisms responsible for the observed behaviour

it does not distinguish between behaviour learned during pretraining and behaviour influenced by instruction tuning

the experiments were performed using a single conversational language model and a relatively small number of prompts

different models, prompting styles, or evaluation methods may produce different results

for these reasons, the conclusions of this investigation should be understood as observations supported by evidence collected here rather than universal claims about all language models

---

## references

### 3blue1brown – but what is a neural network?

used to build intuition for how neural networks improve through repeated error correction rather than explicit programming

### 3blue1brown – transformers (attention)

introduced the intuition behind attention and why context can influence prediction across long sequences

### the illustrated transformer (jay alammar)

helped connect the abstract idea of attention with the transformer architecture used by modern language models

### attention is all you need (vaswani et al., 2017)

read primarily for its motivation and architectural ideas rather than its mathematical details

### neural networks and deep learning (michael nielsen)

provided additional intuition for learning, optimization, and neural network behaviour




