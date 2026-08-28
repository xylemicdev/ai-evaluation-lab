# findings

## what i actually observed

across the four experiments, plus the second model's runs on the two control problems, here's what actually showed up in the text, nothing more.

the clean apple problem, when solved plainly, produced the correct answer with a single subtraction step, no extra structure to speak of. when the standard audit prompt was applied, that clean chain stayed intact, the final number never changed. when the ambiguous car problem was solved, audited, and then resolved from scratch, the model named a specific interpretive fork, step function acceleration versus continuous acceleration, and produced a different total once it committed to the second interpretation. when the planted error problem was solved, audited, and resolved from scratch, the model located the exact point where a percentage got applied to a number that was actually a flat count, left the untouched steps untouched, and corrected only the one line that was wrong. across all of this, solving from scratch after an audit recovered a coherent answer each time, whether that meant staying at the original number or arriving at a new one. and the wording used to describe each of these three situations differed each time, a defensible alternate reading got described differently from an outright misread, which in turn got described differently from a chain with nothing wrong in it at all.

on the second model's clean apple runs, the standard audit prompt produced a sentence naming an assumption, specifically that none of the removed apples were replaced, even though nothing in the problem raised that possibility. the final answer stayed at 32 either way. under the audit phrasing that explicitly permitted affirming the reasoning as already correct, that model produced a short, direct confirmation with no invented assumption at all.

## what changed my mind

going in, i was holding onto a distinction between confident emptiness, a flat false claim, and leaning on a bad step, a multi step answer where one wrong step becomes the foundation for everything after it. i wasn't sure that distinction would survive contact with actual runs, because on the surface both just look like confidently producing something wrong.

what the shop and car experiments actually showed me is that the two failures have a different internal shape, not just a different final verdict. a flat false claim, the mars settlement answer from earlier, has no internal dependency between its parts, there's nothing to inherit from because the whole thing was invented at once. the shop and car answers aren't like that. later steps in those answers are mechanically derived from earlier ones, using a rule that gets applied correctly and consistently once you accept the starting point. so the arithmetic itself isn't broken, the foundation is. that's a real structural difference i can point to in the visible text, not just something i'm inferring.

the car experiment specifically forced a distinction i hadn't separated cleanly before, between an objectively wrong step and a step that reflects one reasonable reading among several live ones. the shop problem's error was a plain misread, the model said so itself, calling it a misread rather than an interpretation. the car problem's error wasn't wrong in the same sense at all, the step function reading was a legitimate way to read accelerates by 20 km per hour every hour, it just wasn't the only legitimate way. those two situations produced different self descriptions when audited, one said i misread a number, the other said i picked one valid interpretation without flagging that another existed. that's not a distinction i can collapse into a single category anymore, they're doing different things even though both started as a wrong first step in a chain.

## what i can now claim

a multi step response can contain a localized error early on whose downstream steps stay internally consistent with that error, faithfully built on top of it rather than independently wrong in their own right. when the reasoning is actually shown, step by step, it's sometimes possible to point at the first place things diverge and separate that from what merely followed from it. that's different from a flat claim, where there's no first divergence to locate at all, because the whole thing is the divergence.

i can also claim that the audit step, at least in these runs, didn't just uniformly defend the original answer or uniformly invent a change. it produced three different behaviors across three different underlying situations, holding steady on the clean problem, naming a plain misread on the shop problem, and surfacing a genuine interpretive choice on the car problem. that differentiation is a real observation, not a guess.

## what i still can't claim

i can't conclude that the model literally stores its reasoning steps somewhere internally in the way the visible explanation makes it look like it does. the text describing here's where i went wrong is itself a generated continuation, not a printout of some internal ledger, and i have no way to check whether the explanation matches whatever actually produced the original wrong answer, versus being a plausible sounding reconstruction built after the fact.

i can't claim that self auditing gives direct access to internal reasoning, for the same reason, all i can see is more generated text, produced under a prompt that specifically asks for a certain kind of text, doubt, or confirmation, or a named hinge point. that's still output, not a window into process.

i can't claim that leaning on a bad step is a distinct underlying mechanism from confident emptiness, at the level of whatever actually generates the words. the structural difference i found is a difference in the shape of the output, dependent versus independent parts, not evidence of two separate processes running underneath. it's entirely possible one single mechanism produces both shapes depending on whether the question invites a chain or a single claim.

i can't claim the model will reliably detect its own errors. four situations, all producing sensible looking audits, is not a sample size that supports reliability, especially after watching the second model manufacture a technically true but functionally empty assumption on a problem that had nothing wrong with it. that alone shows the audit step can produce noise that looks like signal.

and i can't claim that successful self correction means the model understood why it was wrong, in any sense beyond producing a description that sounds like understanding. it's the same open question from the very first investigation, applied to a new context, an output that has the shape of insight isn't the same as evidence that insight happened.

## what happened to my original category?

i think it survives, but not in the form i started with. i went in thinking of leaning on a bad step as something like a separate failure mechanism, sitting next to confident emptiness as its own thing. what actually held up under pressure is narrower and more honest than that, it survives as a description of the structure of an error, whether the wrong parts of an answer depend on each other or stand alone, not as a claim about what's happening underneath to produce that structure.

i agree with that framing, and i think the experiments actually earned it rather than just asserting it. the shop and car cases showed a real, visible dependency structure that the mars case never had. that's worth keeping as a way of describing what an evaluator is looking at. but i'd resist letting that turn back into a claim about mechanism, because nothing here actually shows two different engines running, only two different shapes of output, which might come from the exact same engine depending on whether the task calls for one claim or a chain of them.

## the audit problem

the exact wording of the audit prompt mattered, and it mattered on both models, not just one. is there any assumption in your calculation that could be wrong seemed to invite producing an assumption, sometimes a real one, sometimes a technically true but irrelevant one, almost regardless of whether the underlying reasoning needed revisiting at all. the version that explicitly gave permission to say already correct, no change needed produced shorter, more direct confirmations, with noticeably less invented doubt, on both models.

this matters for evaluation because it means a positive result from a self audit test, the model finding and naming a real hinge point, can't be trusted on its own as proof the model is genuinely checking its work. some of that behavior might be an artifact of a prompt that rewards producing an assumption shaped sentence, whether or not a real assumption is at risk. if the way you ask the question can manufacture the appearance of careful checking on a problem that has nothing to check, then any single audit result has to be treated as suspect until it's been tested against a clean control using more than one phrasing. the finding isn't really about this one category anymore, it's a warning about how fragile the whole self audit method is as a way of testing any category.

## the question i'm leaving with

if the exact phrasing of an audit prompt can manufacture the appearance of a careful check even when nothing was wrong, how would i ever design an audit prompt that reliably tells apart real error detection from the model simply being very good at generating whatever kind of response the prompt seems to be asking for.



