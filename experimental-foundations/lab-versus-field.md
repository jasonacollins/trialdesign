# Lab versus field

A common claim against laboratory experiments is that they do not enable conclusions to be drawn about the "real world" Those critiques tend to rest on three foundations:

-   Lab experiments are conducted in a "sterile environment" with artificial surroundings and tasks.
-   Lab experiments often do not use realistic commodities or stakes. They often involve abstract rewards of materially smaller amounts than may be at stake in the outside world.
-   Lab experiments don't use "real people". We are not interested primarily in the behaviour of students.

These three critiques mean that lab experiments can have limited relevance for predicting field behaviour unless the aspects of behaviour being studied are general across environments, stakes and subject pools.

Field experiment, by contrast:

-   Involve the subject pool that is of interest (i.e. not undergraduates)
-   Can actually be cheaper than lab experiments in that it is easier to get large samples in the field
-   May be better environment for testing size of change. The sterility of the lab often means that the scale of the observed phenomena is not a reliable indicator of the expected external change.
-   Use realistic stakes.

Lab experiments are not, however, without their advantages:

-   Lab experiments can give experimenters **more control**. In the lab, it is easier to give strict instructions that are then followed.
-   Lab experiments can also give **more transparency** about the subject pool (even if they are undergraduate students or workers on Amazon Turk). New subject pools may have idiosyncrasies beyond their field relevance.
-   Lab experiments are typically **more replicable**. They are easier and cheap(er) to replicate. This can provide comfort against surprising results.
-   Lab experiments are often simple more **feasibile**. It is often not possible to experiment in half the market.

The result of this balance of costs and benefits means that lab and field experiments should be seen as being methodologically complementary. Each can enable insights that the other can't. Experiments in one can be used to inform the other.

We will return to the question of lab versus field experiments in more detail later when we explore the generalisability of experiments.

## Types of experiments

One major experimental consideration is whether to experiment in the lab or the field.

### Criteria that define a field experiment

@harrison2004 described six criteria that can be used to delineate between lab and field experiments:

**The nature of the subject pool**: Is the subject pool made up of standard subjects (e.g. students), a more representative subject pool, or a target population? Decision making may vary across pools.

**Information the subjects bring to the task**: Do participants being with them experience in the commodity or task that forms the basis of the experiment? Decisions may vary with the experience brought to the task.

**The nature of the commodity**: Does the experiment use actual rather than abstractly defined goods? The artificiality of abstract goods can affect behaviour.

**The nature of the task or trading rules applied**: Is the task the same that is naturally undertaken in the field? As field experience can enable the development of task specific heuristics, variation in the task can shift decision making.

**The nature of the stakes**: Are the stakes in commensurate to that in the field? Stakes in the laboratory and field can vary markedly, which might be the difference between indifference and engagement.

**The nature of the environment that the subject operates in**: Is the environment the one in which the decision naturally occurs? Different settings might engender role playing, or suggest particular strategies or heuristics to use in making decisions.

### A taxonomy of experiments

This criteria can be used to develop a more refined taxonomy of experiments than simply "lab" or "field", although this is a spectrum rather than a precise taxonomy. Harrison and List developed a spectrum as follows:

**Conventional lab experiments**: Lab experiments typically use a standard subject pool of students (cheap and convenient), an abstract framing, and an imposed set of rules.

**Artefactual field experiments**: Artefactual experiments mimic lab experiments, except that they use non-standard subjects such as people from the market or context of interest.

As one example, Michael Haigh and John List got traders from the Chicago Board of Trade to play games to test whether they exhibit myopic loss aversion. (You might recall from *23713 Behavioural economics and corporate decision making* that myopic loss aversion was Thaler and Benartzi's explanation for the equity premium puzzle.) Would professional traders with experience trading make better decisions? Surprisingly, they found that the traders were even more myopically loss averse in a lab environment than the typical student subjects.

Another example is work by Joe Henrich and colleagues, who recruited subjects from 15 small-scale societies to play the ultimatum game. (Recall that the ultimatum game involves a proposer offering a split with a respondent. If the respondent accepts, they keep the split. If they reject, they both get nothing.) These subjects came from three foraging societies, six societies that practice slash-and-burn horticulture, four nomadic herding groups, and three sedentary agriculturalist societies.

Although no group exhibited the optimal game theoretic solution (offer the smallest possible non-zero sum, accept), Henrich and colleagues found that there was material behavioural variability across the groups. No group offered, on average, less than 25%. But two groups had average initial offers over 50%. Rejection rates also varied materially. Henrich and colleagues argued that economic organisation and the degree of market integration explained a substantial portion of this variation.

**Framed field experiment**: Framed field experiments incorporate elements of the naturally-occurring environment, such as the commodity, tasks, stakes and information sets of the subjects. Subjects understand they are taking part in an experiment and that their behaviour is recorded and scrutinised.

As an example framed field experiment, John List tested expected utility and prospect theory at a sportscard show. He endowed experienced traders with a mug or bar of chocolate and give them an opportunity to trade (as per the famous experiments reported by Daniel Kahneman, Jack Knetsch and Richard Thaler). List found that, among inexperienced consumers, prospect theory adequately explained their behaviour. However, those with intense market experience behaved in accordance with neoclassical predictions.

**Natural field experiments**: Natural field experiments are similar to framed field experiments except that the environment is one where the subjects naturally undertake these tasks and where the subjects do not know that they are in an experiment.

Natural field experiments are different from "natural experiments", a subject you will look at in depth in Principles of Causal Inference. Natural field experiments use treatments constructed by the experimenter to test a hypothesis. Natural experiments use naturally created randomness across treatments to draw conclusions from naturally occurring data. The experimenter has less (usually no) control in natural experiments. Field experiments might be seen as providing a bridge between lab experiments and naturally occurring data, giving mixture of realism and control that you can't achieve otherwise.

You came across a natural field experiment in a previous unit where we saw Marianne Bertrand and Sendhil Mullainathan's tests of labour market discrimination. They sent manipulated CVs tin response to ads in Boston and Chicago, finding that white names received 50% more callbacks for interviews than African-American soundings names.

## Control

A primary requirement of a good experiment is that it tests or controls for alternative hypotheses. If you were to test the success of an intervention to increase savings in December without controlling for the possibility that expenditure tends to increase in the lead up to Christmas, you are going to have a poor experiment.

There are two ways in which we achieve control: directly and indirectly. These are not either/or options. Rather, we tend to use both direct and indirect control together in an experiment.

### Direct experimental control

In a lab experiment, you can directly control many variables. You choose which to keep constant across the experimental participants, such as the rules of the game that they play or their initial endowment. Variables held constant are **control variables**.

You also choose which variables you will vary. Variables that are changed are called **treatment variables**. If you want to to test the effect of a text message to some people and not others, that controlled variation is your experimental treatment.

Typically you will test hypotheses or behavioural interventions by changing one variable at a time. You only change variables which are directly relevant to the hypothesis being tested, otherwise holding the environment fixed. This can help to avoid confounds.

In the field, you control fewer variables, although you maintain direct control of the treatment effects.

### Indirect experimental control

Many variables are difficult to control directly, particularly in the field. For our advertising example above, it's hard to cancel Christmas. You might think that you could compare sales year-on-year, but is this Christmas the same as the last (a salient problem this year!). More subtlety, the customers who will see your intervention may have different propensities to save that those who don't. You can't directly control that.

You can measure variables which you think may affect the propensity to save: gender, age, income, etc, and adjust the analysis after the fact. But there will be more factors than you capture, and likely some important ones that you don't even realise are relevant. These uncontrolled factors will ultimately undermine your experimental conclusions.

There is, however, an indirect way to achieve control: randomisation. By randomly assigning experimental participants to different treatments, we can eliminate differences between the subjects as a cause of differences between treatments. We will discuss how randomisation works on the next page.