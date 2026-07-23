# reflection

## what surprised me

i expected the investigation to challenge the idea that a language model is "just" a next-token predictor

instead, the opposite happened

the experiments never forced me to abandon that description. they forced me to take it more seriously

what surprised me most wasn't that context mattered. i already believed that in some vague sense. what surprised me was how little context was often needed. in many of the experiments, a single surrounding word was enough to completely change the model's behaviour

i also expected missing context to produce confident mistakes. instead, the model often became more cautious, offering multiple interpretations rather than committing to one. i hadn't expected uncertainty itself to emerge as part of the behaviour

perhaps the biggest surprise was realizing how easy it is to accidentally explain more than the evidence supports. several times during the investigation, i caught myself making claims about what the model "must" be doing internally. going back and separating observation from explanation turned out to be just as important as running the experiments themselves

---

## what changed in my thinking

before this investigation, i thought of next-token prediction as an accurate but almost dismissive description of language models. it sounded like a technical detail that couldn't possibly explain behaviour that often feels surprisingly intelligent

i don't think that anymore

i now see next-token prediction as a deceptively simple objective. the objective itself doesn't ask the model to understand relationships, context, or ambiguity. it only asks it to become better at prediction

but prediction across billions of examples quietly creates pressure to discover whatever structure makes better prediction possible

i haven't stopped thinking of language models as prediction systems

i've stopped underestimating what prediction alone can give rise to

---

## what i'm still uncertain about

this investigation answered one question but exposed several others

i'm more convinced than before that context is essential to good prediction. i'm much less certain about what kind of internal representations the model develops while learning

when i say the model has learned a "relationship," what does that actually mean? is it storing reusable concepts, or is that simply the most useful language humans have for describing behaviour we don't yet fully understand?

i'm also not convinced that observing intelligent-looking behaviour tells us much about what is happening internally. behaviour is evidence, but it isn't explanation

those questions feel worth investigating rather than answering too quickly

---

## one sentence for my future self

don't confuse a simple objective with simple behaviour. sometimes the most interesting systems emerge from goals that sound almost trivial


