# reflection

before this investigation, i was mostly thinking about model failures as different kinds of wrong answers

after going through the experiments and then comparing my categories with existing research, i think that was too simple

the more useful question turned out to be what the answer is being checked against

some failures are about whether the model's claim matches the world

some are about whether it followed the information or instructions given to it

some are about how it behaves when the situation is ambiguous or uncertain

that distinction helped explain why categories that initially looked similar started separating, while others that initially felt separate started collapsing

"confident emptiness" survived fairly well as a useful observable category, although research gives it more precise names depending on the type of factual or faithfulness failure involved

"answering the wrong door" also survived, but i now understand that instruction following is its own evaluation axis rather than simply another form of factual incorrectness

"flat confidence" became much harder to defend as a separate failure category

i still think confidence that does not track evidential support is important, but i now see that confidence may be better treated as a property that cuts across different failures rather than as a failure category by itself

"getting led" went through a similar collapse

when i deliberately introduced misleading context, i initially thought i was testing a distinct failure mode

but the more i pressure-tested it, the less certain i became that the model itself has a separate mechanism for "being misled"

from the model's perspective, a trustworthy clue and an untrustworthy clue are both pieces of context

that means the distinction may exist more clearly from the evaluator's perspective than from the model's perspective

"leaning on a bad step" was more interesting

i still cannot claim that it represents a completely separate underlying mechanism, but i can observe a different structure in the output

a later step can be internally consistent with an earlier mistake

that means an evaluator looking only at the final answer can miss the actual location and structure of the failure

this made me realize that evaluation is not always about asking whether the final answer is correct

sometimes the more useful question is where the response first diverged from the problem

the self-audit experiment also gave me a useful warning

i initially treated asking a model to check its reasoning as though it would reveal something about whether the reasoning was actually sound

the control experiment complicated that assumption

an audit prompt can itself encourage the model to manufacture an assumption or perform a particular style of self-criticism

so even the tool used to inspect a failure can introduce a new behavior that looks like evidence

that feels like one of the most important lessons from this investigation

an evaluation is not just the model's answer

it is the interaction between the model, the prompt, the evaluator's assumptions, the scoring method, and the evidence being used to judge the result

i also came into this investigation thinking my seven categories might become a useful taxonomy

instead, the more valuable result was discovering that a taxonomy needs to be tested against other taxonomies

a category can feel obvious from a handful of examples and still turn out to be a cause rather than a failure type, a behavioral property rather than a content failure, or simply another view of a broader category

that changes how i want to approach future investigations

i don't want to collect terminology just to sound like i understand ai evaluation

i want to be able to start with something i observe, define exactly what i think is happening, design a test that could prove me wrong, and then compare the result against how other researchers have measured the same kind of behavior

that feels much closer to actual evaluation work

investigation 001 taught me to separate observation from interpretation

investigation 002 added another layer

now i also need to separate the failure i observe from the framework i use to describe it

i think that is the more useful lesson to carry forward



