---
title: "Roadmap to Stronger AI"
---

The discussion of the future of AI that I see focusses a great deal on issues like “is it AGI or not” and “is it sentient”.  I just don’t think though are helpful, in part because while I’m incredibly impressed by things like GPT-4, I think there are many more advances ahead of us before those become the immediate problems.  Instead, let me try to lay out a plausible sequence of AI capabilities starting from where we are now that would get us to the point that those discussions matter, going step by step through out long-term roadmap.

# Current Version

The AI we have today is the result of taking models with enormous capacity and training algorithms that can use it and applying them to the task of imitating people.

The starting point was imitating what we say.  The Davinci GPT-3 models were just shown vast piles of text, and got really, really good at predicting the next word.  The surprising thing was that out of that emerged something that looked intriguingly like intelligence.  In hindsight, though, maybe being able to imitate people over sentence-long text generation well enough just has to look reasonably smart unless humans are really dumb.

On top of that, we’ve added the ability to imitate what we want to hear.  First, we gave it examples of what we want - question answering behavior instead of predicting the next word.  Then we built models of “will humans like this answer” - a better objective function than guessing the next word - and trained it to optimize that with RLHF.

What this gave us was a magical system that can give intelligent, reasoned answers about pretty much anything it learned about when it read the Internet.  At the same time, though, it is just a copy of us, and maybe even us not at our most reflective.  It is trained to predict the next word and mimic our standard answers to short-essay responses, not to produce conceptual breakthroughs or be the next Shakespeare.  It can still change the world as we know it even if it never gets beyond where it is today, but let’s try to imagine what the future roadmap could hold.

# Next Releases

Now, I’m going to make the assumption that we either have, or soon will, max out what the process of training models like we have on texts like we can get or generate, in that the cost of incremental improvements gets higher and higher.  And let me also assume that we complete the natural trajectory of media we interact with and bring not just texts but visual and auditory media under the same framework of imitating what we see and hear in them.  Given that the original GPT-4 demo included a preview of that, this doesn’t seem a stretch.  At the same time, being able to see what we see in a picture doesn’t seem like a superhuman ability.

Instead, my claim is that as that process maxes out, AI will be recruited to solve different problems, not by directly imitating human actions, but by learning how to use tools.  There, I’m proposing that AIs could learn to use specifically software tools, learn to use them as well or better than humans, and use them at speeds that we couldn’t hope to match.

You may ask “Aren’t you describing chatGPT plugins?”.  The answer is yes..and no.  The idea of connecting an AI system to an external tool is a well known and important one.  Next word predictors turn out to be terrible at doing math but if you give them the ability to ask “What is 437 + 756?” and get the answer externally, they can do it just fine.  We humans are bad at it too, which is why we invented calculators.  chatGPT plugins at present take a language model and let it connect to calculators (and many other things).  However, the AI has to learn to use this calculator by reading that manual, whereas we humans learned by pressing buttons to solve math problems, and I think those give rise to different levels of integration with our thoughts and plans.  Training an AI model jointly with its tools may be hard, and it hasn’t been the focus so far - possibly because the two best tools we found so far (web browsers and Python interpreters) are so general that they’re more like language than tools - but I’m proposing those joint models as the next step.

What might those look like?

**Data analysts** - We see glimpses in this today of some of the GPT-4 Interpreter demos where people analyze data without needing to write code.  What I’m envisioning here starts as a continuation of that path.  Software tools simply are better than humans at analyzing large volumes of data, and a general purpose AI linked to more traditional data analysis could try out many more options than a human analyst.

**Systems analysts** - Instead of connecting it to something like Pandas for data analysis, imagine connecting it to a physics simulation, or an ecosystem model, or one of another things like that.  By training it to be able to look at the model and the initial data, and predict what will happen in future and come up with heuristics to optimize for various outcomes.

**Reasoners** - The Python interpreter is a powerful but very general tool.  If we want AIs that do careful reasoning, the ability to move between text and things like automated theorem provers or SAT solvers could unlock a different kind of reasoning that human imitation.

**Strategists** - In the early days of RL, we saw some interesting experiments with AI in competitive gameplay, such as AlphaGo, DotA AI5, and the Diplodocus Diplomacy AI.  Training an AI on a wide range of such games through self-play could produce the ability to reason in game-theoretic ways.

**Emotive AIs** - This sounds a bit farfetched:  Get data about human emotive responses and train the AI to respond to and elicit emotional content - and it’s likely hard to get that data.  However, once you rephrase “elicit emotional response” as “get customers to like my advertisements”, it’s not hard to imagine a lot of effort being applied to the problem.

Again, the pattern here is one model that can use text to talk to humans about its goals and results, can formulate text-level plans (”let’s load this data into Pandas and examine some features”), but also really understands the connections between the two at an intuitive (ie, training rather than in-context) level, enabling it to recognize situations like “from the description of the problem, these kinds of programs are likely to produce these kinds of outputs, which can be interpreted in the following ways” 

# Projects for the Future

All discussions about features not in the next release are guesses, and in this space doubly so.  But let’s take the assumptions so far: we have AIs that know how to imitate the way we talk and the way we think (at least in ways we can verbalize), and they know how to use some powerful software tools in ways that in specific niches can achieve superhuman performance.

If you buy that, then the next set of feature requests become fairly clear.  The limit now is the human operator’s ability to figure out how to define its problem clearly, how to solve that problem using all of the tools at its disposal, and ultimately, figure out which problems to spend its time on. 

## Coordination & Planning

Thus far, it has made sense to think of each AI as an individual with a professional skill - writing text, analyzing data, and so on - with the human in the role of the direct manager.  If we need to first understand the simulation, and then analyze the data, and then write up the results, then we have thus far expected the human to come up with the plan to divide up the work to accomplish the goal.  As humans become the limit, pressure will build up to automate more and more of this function - starting with the job of a small team manager and growing to handle projects of increasing complexity.  How might this be done?  Self-play at solving a wide range of challenges given access to the previous layers of AI seems like one possibility.

## Planning

We’ve been waiting for the AGI step, and here we are.  We’ve build AIs that can operate as team managers.  Given a goal, they are able to translate it into subgoals, then into tasks, and then reassemble the results of the tasks back into a solution that achieves the goal.  What’s still left for the human is to specify the goal, which leaves us with a philosophical problem:  What goal are we pursuing when we set goals?  How do we know that they’re the right goals?  The mid-level manager can say that this is a good way to reduce costs, but only the CEO can say whether what the company needs is cost reduction, or a new brand image, or to acquire a supplier.  Thus far, each step has been motivated by the need for the human to solve the next level of problem, and at each step, the easiest solution is to give them a tool for manage the next layer down.  But when we come to the problem of setting high-level goals, that process needs to be grounded on some kind of foundation, and here is where I see drivers that would push towards something that looks like AGI.

## Caveat

In all of this, I have focused on the “discrete” model of AI, where the AI operates as a separate tool or co-worker, that the “integrated” model of something like Copilot where the human is part of every step.  Of course, that will be incredibly important and have its own roadmap of improvements from where we are today.  However, in my own thinking about it, I found it hard to disentangle the AI roadmap from the user interface roadmap in this space - after all, it is about the human-AI interface at some level - so I chose to start from a simpler, clearer problem for now.