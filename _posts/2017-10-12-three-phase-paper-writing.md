---
layout: post
title:  "Three-phase Paper Writing"
date:   2017-10-12
---

## Three-phase Paper Writing

---

In this post, I describe the process that I follow when writing technical papers. Or perhaps I should say, the process that I *realized I am following* when I write. I never sat down and designed some “master plan” for how to write effective papers. Rather, I recently finished up a conference paper submission and finally decided to take some time to reflect on and distill the paper-writing process that has organically emerged for me over the course of several years of research experience.

My goal with this post is to help demystify the process of writing a good technical research paper. As much as they might read like it, great papers do not spring fully-formed from the minds of their authors. They take a lot of planning and methodical effort to get to that state. There’s creativity involved, for sure, but much of the process is highly repeatable—in fact, you can think of the contents of this post as an *algorithm* for writing papers.

About the title of the post: writing a paper in three phases might sound like more work than doing it in one. But I find that following this process actually saves me time. When I sit down and try to write a submission-worthy draft in one go (a process that got me through most of my schooling up until grad school), I find that I waste a lot of time staring at a blank screen and thinking really hard about what to write. Besides, if you’re a computer scientist like I am, a multi-stage approach shouldn’t be too hard to swallow: we all know that every problem can be solved by adding more layers of abstraction ;)

Before I begin, a caveat: what follows is one person’s opinion. This process works well for me, but your mileage may vary.

### Phase I

To begin with, I determine the *outline* of the paper. My goal with this phase is to block out the major *sections* of the paper, as well as to jot down rough notes about key points I want to emphasize within each section.

When, in the course of a research project, should you start this phase? I like to start once a project has passed the *proof-of-concept* stage: I’ve done enough experiments to be reasonably confident that my idea is going to work, and I have a more-or-less stable roadmap of remaining tasks that need to be done. The amount of time it takes to reach this stage is highly variable, depending on the project.

When organizing the paper into sections, I exercise very little creativity—I follow the same template every time:

**<u>Introduction</u>**: Within this section, I jot down bullet points for the following:

* The area I’m working on and why it’s important.
* The specific problem(s) I’m tackling.
* Why those problems remain tricky with current technologies (i.e. why existing state-of-the-art isn’t quite enough).
* My new insight(s) / approach to solving the problem.
* How I evaluate the new approach (i.e. how to convince the reader that this new approach is valuable).
* Explicitly list the major contributions, i.e. “Our contributions are…” This can feel awkward and pedantic the first time you do it, but this helps reviewers evaluate your work (and they will look for it).
* Road map for the rest of the paper (so the reader can skip to sections of interest, if they so desire).

Having these bullet points make it easy in later phases to build a compelling motivational storyline for the project by just “interpolating” between these points. This is the most detail I put into anything during Phase I, because it’s important to establish the narrative framing of the paper early—that influences everything that follows.

**<u>Related Work</u>**: I jot down notes about papers that are related to mine and how I’ll talk about them in relation to my work. A rule of thumb to follow here: never cite something in Related Work unless you also describe how your work is similar/different to it. In other words, the Related Work section is not a place to name-drop papers you know about. Rather, it’s a guide to help the reader understand how your work relates to other papers *they* might know about. To make this section easier to navigate, I like to organize it into named sub-sections by major topic or theme. For instance, if I’m presenting a system that applies variational inference methods to inverse procedural modeling, I might have a subsection named “Variational Inference” and another named “Inverse Procedural Modeling” (among others).

**<u>Approach</u>**: The goal of this section is to give the reader a high-level understanding of the paper’s new contributions before digging into the details. For papers that describe a new algorithm, working through a concrete example of the algorithm in action often serves well. For papers that present a new system, an overview of the system’s pipeline (both textually and in figure form) can help. Sometimes a paper needs both. I don’t write much here during Phase I; I just record rough ideas I have about illustrative examples / pipeline organization.

**<u>One or more Method sections</u>**: This section digs into the details of how the new method/system works. It’s the only place where I exercise any creativity in section-level organization, because the best organization depends on the method. For example, for a paper that presents a new machine learning model, I might have one section describing the model itself, one section on drawing inferences from the model, and another on learning it from data. During Phase I, I write almost nothing here, as these details often change as the research project progresses.

**<u>Results/Evaluation</u>**: As early as possible, I narrow down the set of results that I think are more important to show, and I create named subsections for each of them (e.g. “Ablation Study,” “Perceptual Evaluation,” “Analysis of Running Time.”) All subsequent work on the project then proceeds with the goal of obtaining these results, and no others. This helps focus project work on concrete deliverables and makes it easier to quantify how much work is left to do before the paper is submittable.

**<u>Discussion and Future Work</u>**: This section starts off with a conclusion paragraph that restates the paper’s main contributions and the evaluations that back them up. I don’t write any of this in Phase I, as it’s much easier to write this once the rest of the paper is done. What I *do* write here in Phase I are notes about my method/system’s known limitations and any ideas for future work. I add to this scratchpad of ideas as the project progresses, which makes it very easy to write the full version of this section in later phases.

As the project progresses, parts of this outline may need to change (“I now see that it won’t be feasible to get that result by the deadline, “this other result is actually really important, “now that I understand the method’s strengths better, it makes more sense to motivate it like this”). Since I haven’t fleshed out any of these sections very much, making such changes is relatively painless.

“But wait,” you’re asking, “where’s the abstract? Doesn’t that come first?” The abstract is actually one of the last things I write. It’s goal is to concisely summarize the paper and what the reader can hope to get out of it; I find this much easier to do when the paper is almost finished.

The paper stays at this phase until the research project reaches *feature freeze*: the details of the algorithm/system have been finalized and the code will not change any further (modulo fiddling with parameters). All that remains is running experiments and generating other results. At that point, I feel it’s safe to move forward into Phase II.

### Phase II

At this point, you could attempt to write out the final draft of the paper. Personally, I find the gap between a Phase I outline and a submittable draft still too large and daunting, so I use a second, intermediate phase to help smooth that transition.

In this phase, I flesh out the *narrative flow* of each section. If the goal of Phase I was to block out the paper at the section level, then the goal here is to block out the paper at the *sentence* level. Specifically, I write down every sentence that will appear in the final draft, but I focus only on the point that sentence makes and not how it makes it. I use a simple text editor (so as not be distracted by irrelevant formatting choices), and I write each sentence on a new line (to emphasize to myself that each sentence must add some meaningful new piece of information—no throwaway sentences allowed). I’ll use incomplete sentences, incorrect grammar, abbreviations, slang—anything that helps me write quickly. I am trying to get into a [flow state](https://en.wikipedia.org/wiki/Flow_(psychology)) by writing down ideas as they sound in my head, without worrying about how they look on the page. If you have a history of “first draft = final draft” writing (like I did), you may find this process deeply uncomfortable at first. It can become more natural with practice, though, and reaching a flow state in this phase can feel very liberating.

It should go without saying, but I also do not typeset any math in this phase. I blow through equations by sketching them out in plain text shorthand.

I haven’t done any measurements, but I suspect that of the three phases, I spend the most time in this one.

What sentences should you write, specifically? Obviously, the answer to that question depends largely on your subject matter, but here is a good rule of thumb: the first paragraph of every section should say what is going to be in that section and why it’s important. Readers don’t want to do extra work to intuit this for themselves, and reviewers often won’t bother—so tell them explicitly. This rule of thumb is an instance of a piece of advice attributed to Dale Carnegie: “Tell them what you’re going to tell them. Next, tell them. Finally, tell them that you told them.”  The introduction-body-conclustion structure of the whole paper serves this purpose at a broad level, but you can (and should!) also apply this principle at the section level.

A related rule of thumb: for every design decision you introduce, have a sentence (or more) justifying why it was necessary (or better than alternative decisions you could have made). If you don’t do this, your paper ends up reading like a technical spec for the system you’ve built (“our system does X, then Y, then Z…”). Your goal when writing a paper is not (just) to tell the reader what you did; it’s to convince them that it was the *right* thing to have done.

Once I’ve finished with the text of a section, I also make figures in this phase. I already described the types of figures that might appear in an Approach section. For the Method sections, a good rule of thumb  is to include one figure for each new component of my method/system—pseudocode, an example, etc. Most technical explanations can benefit from an additional visual channel of information—challenge yourself to come up with one. In the Results/Evaluation section, I create figures and/or tables for all results I plan to show, and I fill them with placeholder values/images until I have real results to add. This makes it easy to tell exactly what and how much data I need to generate to have a ‘finished' results section, which I find both reassuring and motivating.

### Phase III

In this third phase, I rework the sentences I wrote during Phase II, polishing up the wording. I think of Phase II sentences as notes to myself about the points I want to make, while Phase III sentences are for my audience. I also add citations and typeset math here.

Some style tips to keep in mind when writing for this phase:

* Avoid overuse of the passive voice. Don’t waste time being overly zealous about this, but also don’t have a whole paragraph of sentences with verbs like “is selected,” “is initialized,” “is executed,” etc.
* Don’t use citations as nouns, e.g. “According to [3], the optimal method for…” This is un-grammatical: citations are metadata about the text, not part of the text itself.
* Vary your sentence structure. If a bunch of subsequent sentences being with “We do X,” then mix it up. And speaking of the use of “we”…
* Is “we” really appropriate? When describing something that the authors did, then yes (e.g. “We experimented with alternate methods based on…”). However, I find that authors often use “we” to describe an action that is actually performed by some piece of code (e.g. “we take the first item out of the list…”). In these cases, consider using “the system” or “the algorithm” as an alternative to “we.” If this gets repetitive, it’s fine to mix in a little bit of passive voice to keep things fresh.
* Figure captions should describe what the figure contains. “Figure 1: an overview of our system” is insufficient.  The figure should stand on its own: the caption should describe the figure in enough detail that the reader can understand it without having to read the main paper text. Here’s a litmus test you can apply: can the reader get the gist of your paper from just looking at all your figures + captions? This is easier done in some fields than in others (e.g. graphics papers lean figure-heavy by their nature), but it’s a bar worth striving for.

Should you do a Phase II pass over the whole paper before moving on to Phase III, or do both phases one section at a time? I tend to do the latter, as I have an easier time getting into a writing flow when I can build on a very concrete previous section. Your mileage may vary.

### Phase IV+

Ok, I lied: there are more than three phases. In fact, there are as many phases as you have time for before your submission deadline. Why? You should seek feedback on your paper, and this feedback will lead to revision phases.

When you ask someone for feedback on a paper, be specific about what forms of feedback you want. At first, you should ask your readers for comments on the high-level organization of the paper, the motivation, and the overall storyline. Later on (and closer to the deadline), shift focus to asking readers to look for insufficient explanation, unclear wording, and typos.

For the purpose of gathering high-level feedback, can you send someone a Phase I or a Phase II draft? In my experience, this doesn’t always work. A Phase I paper is too incomplete. It’s mostly notes to you, and someone reading it can give you the benefit of the doubt, i.e. “these notes seem like they could be fleshed out into a good paper.” It’s in the execution of these high-level ideas that problems crop up. With a Phase II paper, readers can get caught up in the unfinished and sloppy language, even if you explicitly instruct them to ignore it—it can be hard for even the most well-intentioned reader to see the forest for the trees. The takeaway point: someone needs to simulate the experience of a ‘real’ reader in order to give you good feedback, and the best way to facilitate that simulation is to give them a ‘finished’ artifact to read (the same holds for getting feedback on oral presentations, but that’s a whole other topic).

Is it a waste of time, then, to have to go back and rewrite parts of the paper you thought were finalized? Not at all. The time and effort you spend doing this will help you internalize the lessons you’re learning so you don’t make the same mistakes again. There’s just no substitute for this kind of experience. As you gain that experience, the frequency with which you need to do major re-writes will decrease—you will get faster at this, I promise.

### Miscellaneous Advice

Many publication venues have page limits, and polished paper drafts often end up longer than this limit. Before you start shrinking figures, inserting negative space, or fiddling with font sizes and margins, look for paragraphs whose last line has only a few words. Can you trim some sentences in that paragraph such that the last line disappears? You might be surprised at just how much space you can reclaim this way—in fact, I’ve used this method alone to meet page limits on several submissions. Plus, it often forces you to find and simplify excessively verbose explanations in your paper, which strengthens the paper anyway.


### Conclusion

I hope that having this process explicitly written out proves useful to some new graduate students / aspiring researchers out there. If this method works for you, I’d certainly love to hear from you. Also, let me know if you have any suggestions for how this post could be improved.

<br/>