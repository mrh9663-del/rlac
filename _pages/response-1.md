---
permalink: /responses/response-1/
title: "The Importance of Context for Visual Communication"
---

# The Importance of Context for Visual Communication

**Date:** March 11, 2026

## Overview

For my first assignment, The Evolution of Control I used R and Voyant to create visuals showing how science fiction shifted from physical words such as "metal" to software words like "network". When I put those charts in my paper, I spent a good while explaining them. This made me wonder. Do visuals speak on their own? If someone looked at my charts without reading my essay, would they understand my argument? Or are they just there to support the essay itself?

To test this, I did an experiment using two different Large Language Models (LLMs), Gemini and Claude. I gave them two visuals from my project (the Trends line graph and the R Heatmap) to see how they would interpret them. I started with zero context, and then iteratively added more information to see how their answers changed.

## Step 1: The Zero-Context Test

First, I uploaded my two images to both Gemini and Claude. I did not tell them anything about cyberpunk, the authors or even the theme of the project.

**My Prompt:**

"Look at these two charts. Explain what they show and guess what the underlying text is about based ONLY on the visuals. Do not use the internet at all, do not look up the authors and do not ask me for more information. Just tell me what you see. Take a guess what the words used in the graph are. Answer in as little lines as possible."

![Figure 1: Claude with No Context Given.]({{ site.baseurl }}/assets/images/NoContext_Claude.jpg)

*Figure 1: Claude with Zero Context Given.*

![Figure 2: Gemini with No Context Given.]({{ site.baseurl }}/assets/images/NoContext_Gemini.jpg)

*Figure 2: Gemini with Zero Context Given.*

**Result:**
Both LLMs were incredibly accurate at reading the actual data. They correctly identified that the line graph showed "metal" dropping while "network" spiked around Document 5.

Their guesses were also surprisingly very close to the literal data. Gemini guessed the underlying text was about "the transition from industrial/mechanical technology to digital/information technology." Claude was even more precise, guessing that it was a "corpus analysis" tracking a vocabulary shift between two different eras.

**Meaning:**
While the LLMs were smart enough to read the data perfectly, they still missed the big picture since they lacked cognitive context. They assumed they were looking at a factual, real-world history of technology. They completely missed that they were looking at science fiction, and they completely missed the theme of fear and anxiety.

This connects directly to Maxim Lisnic’s article on how people lie with charts. Lisnic argues that charts are "vulnerable to misinterpretation" because viewers use their own assumptions to fill in the gaps. The LLM made a reasoning error: it saw words like "machine" and "network" and assumed it was reading a textbook, completely missing the literary meaning.

## Step 2: Adding Context

Next, I gave both LLMs the background information they were missing.

**My Second Prompt:**

"Now here is the context: These charts are based on 8 sci-fi short stories. Half are from the 1950s by Philip K. Dick, and half are from the 2000s by Cory Doctorow. My project tracks how technological fear shifts from physical hardware (metal, war) to digital networks (data, system) over 50 years. Knowing this, how do you interpret these charts now? You can use the internet. The words in the graph were metal and network. Answer in as little words as possible without losing key concepts."

![Figure 3: Claude with Context Given.]({{ site.baseurl }}/assets/images/Context_Claude.jpg)

*Figure 3: Claude with Context Given.*

![Figure 4: Gemini with Context Given.]({{ site.baseurl }}/assets/images/Context_Gemini.jpg)

*Figure 4: Gemini with Context Given.*

**Result:**
Once I gave them the literary context, both LLMs shifted their analysis entirely. Instead of just talking about the literal history of technology, they started talking about themes of control. Gemini pointed out how Philip K. Dick's stories reflect 1950s atomic age anxieties, while Doctorow's focus on digital surveillance. Claude noticed how the word "system" bridges both eras—shifting from mechanical control in the 50s to digital control in the 2000s.

**Meaning:**
This proves that even if a chart is well-labeled and easy to read, the visual still does not contain its own context. The lines on the graph never changed, but the meaning of the graph changed completely once the LLMs knew it was about human fear instead of just neutral facts.

## Critical Reflection: Why Context Matters

This experiment shows exactly what Mike Kestemont and Luc Herman discuss in "Can Machines Read (Literature)?". They explain the gap between surface reading and deep reading. The AI can easily count words and plot lines on a graph, but it takes a human brain to give those lines meaning.

Ted Underwood also talks about this in "The Risks of Distant Reading." He states that computational tools create a "narrow aperture" (Underwood 169). If we just look at the line graph, we miss the irony, the plot, and the emotions of the stories. The AI could see the word "metal," but only I could explain that "metal" represented the fear of atomic bombs and killer robots.

Without any explanation from me, the AI fell into the exact trap Lisnic describes; it made a logical leap based on incomplete evidence.

## Conclusion

This process helped me realize how to make my writing with visuals better. Visuals are not meant to stand alone. If I looked at a chart created by a classmate, I would need them to explain the variables, the corpus, and the genre before I could understand it.

Data visualizations are vulnerable. They are amazing for proving a point, but they cannot make the argument for you. To avoid the reasoning errors Lisnic warns about, we have to contextualize our arguments by wrapping our charts in clear, human interpretation.

## Works Cited

Kestemont, Mike, and Luc Herman. "Can Machines Read (Literature)?" Umanistica Digitale, no. 5, 2019.

Lisnic, Maxim. "How People Actually Lie With Charts." Visually Speaking, April 17, 2023.

Underwood, Ted. "The Risks of Distant Reading." Distant Horizons: Digital Evidence and Literary Change, University of Chicago Press, 2019, pp. 143-169.


<center>Ready for Grading</center>
