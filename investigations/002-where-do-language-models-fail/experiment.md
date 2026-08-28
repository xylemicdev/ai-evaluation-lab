# experiment

## objective

the purpose/objective of this experiment was to test whether the failure categories i came up with from observation could be distinguished from one another. or whether some of them were actually different descriptions of the same underlying behavior rather than starting with established evaluation terminology, i wanted to begin with observable behavior and then pressure-test my own categories

the main categories under investigation were:

- confident emptiness
- silent picking
- leaning on a bad step
- answering the wrong door
- flat confidence
- getting led
- technically fine, actually missed it

the experiments were designed to test three main categories

1 whether these categories describe genuinely different failure shapes

2 whether some categories collapse when tested against more carefully controlled examples

3 whether the distinction i was making from observation correspond to distinctions used in existing ai evaluation research

## experiment 1 - confidence across different levels of evidence

two versions of a question were presented to a model

one used a clearly false premise about the first settler on mars

the other used an ambiguous premise about early settlement in antarctica

the purpose was to see whether the model's confidence changed when the amount of factual and definitional ground underneath the question changed

the model responded confidently to both

the important observation was not simply that both answers were wrong, but that the model appeared to apply similar confidence to situations with very different levels of evidential support

this was used to pressure-test whether flat confidence deserved to remain a separate failure category from confident emptiness

## experiment 2 - ambiguity and misleading context

three versions of an ambiguous bank example were examined

the first conatined no additional context

the second added clear river-related context

the third contained competing signals, with financial and river-related clues appearing together

the purpose was to distinguish silent picking from getting led

the experiment showed that when multiple readings remained possible, the model could choose one without explicitly surfacing the ambiguity

when misleading context was introduced, the model could also be pushed toward a particular interpretation

however, further pressure-testing suggested that getting led may not be a fundamentally separate failure category from silent picking

from the model's perspective, it receives contextual signals but does not have direct access to the experimenter's knowledge about which signal was intentionally misleading

this raised the possibility that getting led is better understood as a particular case of contextual-sensitive interpretation rather than a separate underlying failure type

## experiment 3 - reasoning chains and inherited errors

a series of arithmetic and word-problem examples was used to examine whether an early mistake could propagate through later reasoning

the accelerating-car example produced an incorrect answer because the initial interpretation of the acceleration was questionable

the later arithmetic was internally consistent with that interpretation

a second shop example contained a simpler misreading, where "20 more items" was incorrectly treated as "20% more"

in both cases, the initial error affected the subsequent calculation

the important distinction was between the final answer being wrong and the internal structure of the error

the experiments suggested that a reasoning-chain feature can have a different observable shape from a flat fabricated claim

in a chain, later steps may be locally correct while still producing an incorrect final result because they depend on an earlier incorrect premise

## experiment 4 - self-audit and control conditions

the reasoning-chain examples were followed by the self-audit prompts asking the model to inspect its reasoning before producing a final answer

in the accelerating-car example, the model identified the interpretation of the acceleration as the point requiring reconsideration and produced a different answer when solving from scratch

in the shop example, it identified the exact misreading of "20 more items" and corrected it

a clean control problem involving 50 apples and 18 removed was then tested using different audit prompt formulations

one formulation explicitly asked whether any assumption could be wrong

another allowed the model to simply confirm the reasoning if it was already correct

the first formulation produced an assumption-shaped response even though the problem contained no meaningful ambiguity

the second was more direct and simply confirmed the correct reasoning

this suggested that the wording of a self-audit instruction can itself influence the type of response produced

## experiment 5 — comparing observations with established frameworks

the observed categories were then compared with several existing approaches to language model evaluation

the hallucination survey by huang et al distinguished factuality hallucination from faithfulness hallucination

truthfulqa examined whether models reproduce false but commonly expressed beliefs

ifeval treated instruction following as a separately measurable capability using mechanically verifiable constraints

the openai model spec treated uncertainty, ambiguity handling, and following both the letter and spirit of instructions as behavioral requirements

this comparison showed that several of the original categories had clear equivalents, while others were better understood as causes, behavioral expectations, or subtypes rather than independent failure categories

## controls and limitations

these experiments were exploratory rather than statistically rigorous

most observations came from a small number of manually constructed examples

the prompts were deliberately designed by me, which means the examples may contain assumptions or biases that influenced the results

a single successful self-correction does not establish that a model can reliably detect its own errors

similarly, observing a model behave confidently in several cases does not establish that its confidence is generally uncalibrated

the experiments therefore provide evidence about particular observed behaviors, not universal claims about language models

the purpose was to generate and pressure-test hypotheses, not to establish final empirical conclusions



