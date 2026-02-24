---
permalink: /assignments/assignment-1/
title: "Assignment 1: The Evolution of Control"
---

# The Evolution of Control: From Hardware to Software in Cyberpunk Fiction

**Date:** 10/02/2026

---

## Overview

Cyberpunk and speculative fiction have long been shaped by technological anxiety. As technology shifted from the atomic age to the digital age, the language of those fears shifted as well. This project investigates whether the vocabulary of "control" moves from the physical battlefield to the digital network across a fifty year gap in fiction.

### Research Questions

This analysis is guided by three focused questions:

1. **Material Shift:**
Does the vocabulary shift from industrial and kinetic terms (such as "metal" and "war") in the 1950s to informational and network-based terms (such as "network" and "data") in the 2000s?

2. **Nature of Control:**
Does the imagined source of threat move from external physical destruction (bombs, machines, war) to internal systemic control (algorithms, corporations, digital infrastructure)?

3. **Method Comparison:**
What different insights emerge when the same corpus is analyzed using exploratory visualization tools Voyant Tools versus structured statistical analysis R Markdown?

I use computational text analysis to compare Philip K. Dick's 1950s short fiction with Cory Doctorow's 2000s short fiction. Using [Voyant Tools](https://voyant-tools.org) for exploratory data analysis and [R Markdown](https://posit.cloud/) in Posit Cloud for statistical confirmation, I track how key terms rise, fall, and cluster across a combined corpus.

⸻

## Section 1: Corpus Selection & Provenance

### The Corpus

This project analyzes eight short stories: four by Philip K. Dick (The Defenders, Second Variety, The Variable Man, Mr. Spaceship) and four by Cory Doctorow (Anda's Game, When Sysadmins Ruled the Earth, Scroogled, Printcrime). I selected these texts to compare two moments in speculative fiction separated by roughly fifty years. The goal was to test whether the language of technological anxiety shifts from industrial and mechanical vocabulary in 1950s fiction to digital and network-based vocabulary in early twenty-first-century fiction.

Rather than separating the stories into isolated corpora, I uploaded all eight texts into Voyant as a single dataset. This allowed me to observe how specific words change in prominence across the ordered sequence of files, revealing patterns of transition within one analytical frame.

### Provenance & Access

The Philip K. Dick stories were sourced from [Project Gutenberg](https://www.gutenberg.org) in Plain Text format to ensure compatibility with Voyant Tools and R Markdown. I removed front matter such as licensing text, editorial notes, and metadata so that the corpus contained only narrative content. Project Gutenberg was selected because it provides reliable public domain texts suitable for computational analysis.

The Cory Doctorow stories were sourced from the author's website, [Craphound.com](https://craphound.com), where they are published under Creative Commons licenses that allow legal text mining. These files were also cleaned to remove non-narrative material before analysis.

This corpus was chosen because it offers a comparison across time while remaining consistent in genre and number of words. By focusing only on short speculative fiction, the analysis highlights shifts in technological vocabulary without introducing major generic differences as data contaminating variables.

⸻

## Section 2: Computational Analysis and Findings

### Tools Used

I used Voyant Tools as it is accessible, visual, and well suited for comparing word usage across different subsets of a corpus. I applied a stopword list to remove common words, and character dialogue markers. 

### Analysis Process

All texts were uploaded into Voyant as a single combined corpus. I then used Voyant’s (trends, cirrus, and links) tools to compare word frequencies and patterns across documents, interpreting differences based on the time period and author of each text.

### Key Findings

#### Finding 1: The Shift from Metal to Network

Using the Trends tool, I compared the words "metal" and "network" along with any other letter attached to the words before or after such as "networks" across the corpus.

**Result:**

As shown in Figure 1, "metal" appears frequently in the Philip K. Dick stories yet almost disappears in the modern texts. "Network" does not appear at all in the 1950s stories but spikes sharply in the Cory Doctorow stories.

**Meaning:**

This confirms a shift in cyberpunk futures, physical materials like steel and machines are replaced with systems and digital infrastructure. This directly addresses the research question regarding whether speculative fiction shifts from industrial vocabulary to informational vocabulary over time.

![Figure 1: Trends graph comparing "metal" and "network" across the two sub-corpora.]({{ site.baseurl }}/assets/images/Unknown.png)

*Figure 1: Trends graph comparing "metal" and "network" across the two sub-corpora.*

⸻

#### Finding 2: Conflict as Physical Space

The Cirrus word cloud shows the most common words across the corpus after cleaning.

**Result:**

As shown in Figure 2, words like "war," "ship," "surface," and "gun" dominate the visualization. Character names such as "Hendricks" and "Reinhart" also appear prominently, especially from Second Variety.

**Meaning:**

This suggests that early cyberpunk focuses heavily on physical conflict and individual actors, often soldiers or men in combat situations. Modern digital terms exist, but they are less visually dominant in the combined corpus.

<iframe style='width: 461px; height: 242px;' src='https://voyant-tools.org/tool/Cirrus/?stopList=keywords-d0f6ded4517b00c9630f0c617cc2255d&whiteList=&visible=75&corpus=d75fbe52b49d0d2d4e6468819da830ff'></iframe>

*Figure 2: Word cloud highlighting physical and military vocabulary.*

⸻

#### Finding 3: Control as a Physical Act

I used the Links tool to examine how the word "control" is connected to other terms.

**Result:**

In Figure 3, "control" is closely linked with words like "turret," "ship," and "globe."

**Meaning:**

This shows that in the older texts, control usually refers to operating or commanding physical machines or weapons. Control is something you hold with your hands, not something embedded in software or surveillance systems.

![Figure 3: Network graph showing collocations of the word "control."]({{ site.baseurl }}/assets/images/Unknown-2.png)

*Figure 3: Network graph showing collocations of the word "control."*

⸻

## Section 3: Statistical Confirmation in R Markdown

While Voyant provides exploratory visuals, R Markdown allows structured confirmation.

### Process:

I used R to generate a heatmap of thematic nouns across the combined corpus, focusing on terms like metal, machine, network, system, data.

### Result:

![Figure 4: R Markdown Heatmap showing key nouns across the corpus.]({{ site.baseurl }}/assets/images/heatmap.png)
*Figure 4: R Markdown Heatmap*

### Interpretation:

- "Metal" is concentrated in Dick's stories.
- "Network" and "Data" are concentrated in Doctorow's stories.
- "System" appears across both periods but shifts meaning: mechanical/political in Dick, digital in Doctorow.

The R results confirm the trends seen in Voyant. Shifts are measurable, not just visual.

⸻

## Section 4: Critical Reflection & Methodology

### The Risks of Distant Reading

In his chapter "The Risks of Distant Reading," Ted Underwood warns that while computational tools reveal large patterns, they can create a "narrow aperture" if we rely on them heavily. He notes that "There are many historical patterns too large to be explored through the narrow aperture of a single reader's memory" (Underwood 169).

Reading these eight stories linearly, I might have missed the subtle, gradual decline of the word metal over 50 years. Voyant made this "large pattern" visible clearly. But there's also risk: as Underwood warns, this approach can "displace a more appropriately literary mode of insight" (Underwood 143). For example, Voyant counts Google in Scroogled as just a word. A human reader knows it represents the villain. So, the tool shows where patterns appear, but us humans must explain why they matter.

⸻

### Methodological Comparison: Interactive vs. Static

Rockwell and Sinclair argue in Hermeneutica that tools like Voyant are designed for "playful" interpretation, letting users manipulate the text dynamically. In my process, this was obvious: I came across the metal/network connection by exploring the tools interactively.

R Markdown, in contrast, is structured and precise. It counts everything first and lets the human analyze later. This is closer to what Kestemont and Herman call "machine reading," where the computer does the heavy lifting before humans intervene.

Takeaway: Voyant is better for exploring ideas and spotting patterns quickly. R Markdown is better for confirming patterns and getting concrete counts.

⸻

### Interpretation of Results

The analysis confirms the main hypothesis: cyberpunk fear and control shift over time.

- In the 1950s texts, danger is physical—machines, metal, and war dominate.
- In the 2000s texts, danger is systemic—data, networks, and software are central.

The Trends graph is key because it shows this shift visually, without needing to read all eight stories closely. Voyant highlights where patterns are, while we humans explain what those patterns mean in context.

⸻

### Limitations and Biases

1. Eight stories aren't enough to fully represent two eras of cyberpunk. One long story can skew results.
2. Early versions of the text files were cluttered with licensing metadata, showing how easily analysis can mislead if preprocessing isn't careful.
3. Voyant counts words but can't detect tone, irony, or semantic shift. For example, feed in the 1950s refers to food; in the 2000s it refers to data streams. Treating them the same can distort interpretation.
4. Terms like war carry historical meaning (Cold War) that Voyant cannot infer. Humans must look for a meaning.

⸻

### Future Questions

With a larger corpus, it would be interesting to isolate only Doctorow's texts and examine software-related control more closely. Another direction would be opionion based analysis to compare emotional tone across time.

⸻

## Works Cited

### Primary Corpus

Dick, Philip K. *The Defenders*. Project Gutenberg, 2010.

Dick, Philip K. *Second Variety*. Project Gutenberg, 2010.

Dick, Philip K. *The Variable Man*. Project Gutenberg, 2010.

Dick, Philip K. *Mr. Spaceship*. Project Gutenberg, 2010.

Doctorow, Cory. *Anda's Game*. Craphound.com, 2004.

Doctorow, Cory. *When Sysadmins Ruled the Earth*. Craphound.com, 2006.

Doctorow, Cory. *Scroogled*. Craphound.com, 2007.

Doctorow, Cory. *Printcrime*. Craphound.com, 2006.

### Secondary Sources

Kestemont, Mike, and Luc Herman. "*Can Machines Read (Literature)?*" Umanistica Digitale, no. 5, 2019.

Rockwell, Geoffrey, and Stéfan Sinclair. *Hermeneutica: Computer-Assisted Interpretation in the Humanities*. MIT Press, 2016.

Underwood, Ted. "*The Risks of Distant Reading.*" Distant Horizons: Digital Evidence and Literary Change, University of Chicago Press, 2019, pp. 143-169.

