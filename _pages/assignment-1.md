---
permalink: /assignments/assignment-1/
title: "Assignment 1: The Evolution of Control"
---

# The Evolution of Control: From Hardware to Software in Cyberpunk Fiction

**Date:** 10/02/2026

---

## Overview

Cyberpunk fiction has always been about the fear of losing control. But as technology evolves, does the language of that fear change? This project uses computational text analysis to compare the "Industrial Cyberpunk" of the 1950s against the "Post-Cyberpunk" of the 2000s. Using [Voyant Tools](https://voyant-tools.org) for exploratory visualization and [R Markdown](https://posit.cloud/) (through posit cloud) for statistical frequency analysis, I track the shift from physical, hardware-based vocabulary to abstract, software-based systems.

⸻

## Section 1: Corpus Selection & Provenance

### The Corpus

My corpus consists of eight short stories divided into two sub-corpora:

- **The 1950s (Hardware):** Four stories by Philip K. Dick.
- **The 2000s (Software):** Four stories by Cory Doctorow.

### Provenance & Access

I sourced the Philip K. Dick texts from Project Gutenberg, selecting the "Plain Text" versions to ensure compatibility with R and Voyant. Project Gutenberg was chosen for its reliability in preserving public domain science fiction. The Cory Doctorow texts were sourced directly from the author's personal website, Craphound.com. Doctorow publishes his work under Creative Commons licenses, allowing for legal text mining. This combination of Public Domain and Creative Commons texts allowed for a seamless, ethically sourced dataset.

### Why This Selection?

I chose this pairing to test a specific hypothesis: that the "Cyberpunk" genre has undergone a fundamental vocabulary shift. Dick writes during the Cold War (fear of bombs/metal), while Doctorow writes in the Internet Age (fear of surveillance/data).

⸻

## Section 2: Computational Analysis and Findings

### Tools Used

I used Voyant Tools because it is accessible, visual, and well suited for comparing word usage across different subsets of a corpus. I applied a stopword list to remove common words, character dialogue markers, and archival metadata such as "Project Gutenberg" and "License."

### Analysis Process

All texts were uploaded into Voyant as a single combined corpus. I then used Voyant’s (trends, cirrus, and links) tools to compare word frequencies and patterns across documents, interpreting differences based on the time period and author of each text.

### Key Findings

#### Finding 1: The Shift from Metal to Network

Using the Trends tool, I compared the words "metal" and "network" along with any other letter attached to the words before or after such as "networks" across the corpus.

**Result:**

As shown in Figure 1, "metal" appears frequently in the Philip K. Dick stories yet almost disappears in the modern texts. "Network" does not appear at all in the 1950s stories but spikes sharply in the Cory Doctorow stories.

**Meaning:**

This shows a clear shift in how the future is imagined. Earlier cyberpunk futures are built from physical materials like steel and machines. Modern cyberpunk futures are built from data, systems, and connections.

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

## Section 3: Critical Reflection

### Interpretation of Results

The computational analysis supports my main hypothesis. While cyberpunk remains focused on fear and loss of agency, the form that fear takes changes over time. In the 1950s texts, danger comes from physical machines and war. In the 2000s texts, danger comes from invisible systems and networks.

The Trends graph is the strongest piece of evidence because it shows a clear crossover point between industrial and digital language. This makes the shift easy to see, even without reading the stories closely.

### Human Context and Meaning

Computational tools cannot understand narrative meaning on their own. For example, Voyant treats "Hendricks" as just a frequent word, but a human reader knows he is a tragic character manipulated by machines designed to imitate humans. The tool shows where themes appear, but humans still have to explain why they matter.

Historical context also matters. The frequent use of words like "war" reflects Cold War fears of physical destruction. Modern cyberpunk reflects a different fear, being controlled or replaced by software systems.

### Limitations and Biases

This analysis has several limitations. First, the corpus is small. Eight stories are not enough to fully represent two entire eras of science fiction. One longer story can heavily influence word frequencies.

Second, data cleaning had a major impact on results. Early versions of the analysis were dominated by licensing language. This shows how easily computational analysis can be misleading if the data is not carefully prepared.

Finally, Voyant focuses on frequency, not meaning. It cannot detect irony, tone, or narrative importance. For instance, now adays a word such as cloud can mean a server on the internet, such a meaning for this word didn't exist in the 1950s which can give wrong interpretations of the text. 

### Future Questions

With a larger corpus, it would be interesting to isolate only Doctorow's texts and examine software-related control more closely. Another direction would be opionion based analysis to compare emotional tone across time.
