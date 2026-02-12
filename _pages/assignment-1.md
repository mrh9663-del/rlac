---
permalink: /assignments/assignment-1/
title: "Assignment 1: The Evolution of Control"
---

# The Evolution of Control: From Hardware to Software in Cyberpunk Fiction

**Date:** 10/02/2026

---

## Introduction

Cyberpunk stories have circled around fear. Fear of technology, fear of failing to stay in control, and fear of what happens when humans are no longer on top. However, the kind of technology people fear has changed over time. This paper looks at how cyberpunk fiction shifts from physical, industrial technology to digital software based systems. Instead of reading each story closely, I use computational analysis to look for patterns across multiple texts at once.

⸻

## Section 1: Corpus and Research Questions

### Corpus Description

My corpus is made up of eight science fiction short stories split into two groups. The first group contains four stories by Philip K. Dick, published around 1953. These texts come from early science fiction and are often viewed as a foundational pillar for cyberpunk themes. The second group contains four short stories by Cory Doctorow, published between 2004 and 2007, which represent a more modern, post cyberpunk era.

All texts were uploaded into [Voyant Tools](https://voyant-tools.org) as plain text files. Before analysis, I removed front matter and legal boilerplate so the corpus only contained narrative content. I also added stop-words to make sure they don't contaminate the results.

### Why This Corpus

I chose this corpus because Philip K. Dick and Cory Doctorow write in very different technological moments. Dick was writing during the Cold War and the industrial age, while Doctorow writes during the internet and information age. While both deal with technology and power, I suspected that the language they use to describe control would be different.

### Research Questions

This project focuses on three main questions: 

1. Does cyberpunk vocabulary shift from physical and industrial terms (like metal, ship, gun) to digital and abstract terms (like network, system, code)?
2. How does the idea of control change across time, from physical control of machines to software based or systemic control?
3. Does older cyberpunk rely more on physical violence compared to modern cyberpunk?

### Why Computational Analysis

A computational approach makes it possible to compare patterns across texts without focusing on just one story in depth. Using Voyant Tools allows me to do distant reading and visualize trends across a 50-year gap. These patterns would be hard to notice through close reading alone.

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
