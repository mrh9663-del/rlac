---
permalink: /assignments/assignment-2/
title: "Assignment 2"
---

# Assignment 2

## Distant Reading the Future: A Comparison of Stylo and TF-IDF

To read science fiction from the 1940s and 50s is to step into a world shaped by fear. The atomic bomb, the Cold War, and rapid technological change all show up in these stories. Writers imagined alien planets, machines and in some cases broken futures, however underneath that, they were  writing about their own reality. Normally, we study this by close reading: looking at themes and meaning inside individual texts.

However in this paper, instead of asking what these stories mean, it will ask how do we measure how they are written and what they are about using computational methods, and are those two things actually different? To answer these I worked with a corpus of 18 science fiction texts from Project Gutenberg and used two methods: the Stylo package in R and a pre-computed TF-IDF visualization using PCA.

These two methods look at completely different things. Stylo tracks function words such as "the" and "and" to detect writing style. TF-IDF ignores those and focuses on distinctive words to detect themes. This means Stylo is about how something is written, while TF-IDF is about what is being talked about. When you compare these 2, you start to see something important. Style and content could be separated mathematically, but they are always connected in actual writings.

Before doing the analysis, I had some expectations. I thought most of the texts would cluster together as they come from the same era however that turned out to be wrong. The authors in this corpus write very differently. Leigh Brackett mixes science fiction with a noir like tone and focuses more on atmosphere and character than technical detail. Philip K. Dick focuses on paranoia and control. H.G. Wells is much earlier and writes more like philosophical science fiction, dealing with ethics and evolution. Andre Norton writes in a more straightforward and immersive way, focusing on survival and exploration. Marion Zimmer Bradley blends science fiction with fantasy and often includes themes of identity and social structure. Henry Kuttner is inconsistent because he worked across genres and often collaborated, which already suggests his style might not be stable.

This further pushes the agenda that authors in this corpus write in very different ways, and that difference becomes much clearer when you use computational tools.

---

### Methodological Mechanics: Function Words vs. Content Words

To understand the results, we need to understand what each method is actually doing.

Stylo works by analyzing the most frequent words (MFWs) which are usually mainly function words. These are words like "the," "of," and "and." They often don't carry meaning, but they form the structure of language. Writers use them unconsciously and consistently which makes them very useful for identifying style. This means Stylo is strong for authorship detection.

TF-IDF isn't very similar. It reduces the significance of common words and highlights distinctive ones. It looks at how often a word appears in one text compared to the whole corpus. This makes it useful for identifying themes and topics. When visualized with PCA, it places texts in a space where distance reflects their thematic similarity.

This basically means:

* Stylo is driven by function words
* TF-IDF is driven by content words

These two methods are not competing, they are measuring different aspects of the same texts.

---

### Analyzing the Stability of Style

At 100 MFWs, the dendrogram is noisy. The clusters are not very clear, and some authors do not group properly. This happens because the feature set is too small. The model does not have enough data to capture consistent stylistic patterns. Small things like repeated names or formatting differences can affect the results. This shows that parameter choice matters a lot in computational analysis.

![Figure 1: Cluster Analysis-100 mfws.]({{ site.baseurl }}/assets/images/Cluster Analysis-100 mfws.png)

At 500 MFWs, the clustering becomes much clearer. Authors group together in a more stable way. Philip K. Dick's texts form a tight cluster, showing that his writing style is consistent across different works. Andre Norton also forms a clear group. H.G. Wells is separated from the rest, which reflects his earlier time period and different style.

![Figure 2: Cluster Analysis-500 mfws.]({{ site.baseurl }}/assets/images/Cluster Analysis - 500 mfws.png)

This confirms what Eder argues: increasing the number of features improves reliability.

One of the most interesting results is Henry Kuttner. His texts do not cluster as tightly. This can be explained by two things:

1. He writes across genres (horror, sci-fi)
2. He collaborates with other authors

This answers another guiding question: yes, co-authored texts affect clustering. Stylo struggles because the grammatical patterns are mixed between authors.

The Bootstrap Consensus Tree confirms which clusters are stable. Authors like Dick and Norton show strong consistency, while Kuttner shows less. This proves that style is stable when the author is consistent, but unstable when multiple influences are involved.

![Figure 3: Bootstrap Consensus Tree from 100-500 mfw.]({{ site.baseurl }}/assets/images/Bootstrap Consensus Tree.jpg)

---

### Thematic Gravity through TF-IDF

At 100 MFWs, the PCA plot is scattered. The loadings are very specific—character names, unique objects, and rare terms. This pushes texts apart in a way that does not reflect broader themes. This answers a key question: no, loadings are not the same across different MFW levels.

![Figure 4: PCA Graph using 100 MFWS.]({{ site.baseurl }}/assets/images/MFW100.png)

At higher MFW levels (3000), the clusters become more meaningful. The loadings now include more general but still distinctive words like "radiation," "empire," and "spaceship." This causes texts to group by theme instead of individual details.

![Figure 4: PCA Graph using 3000 MFWS.]({{ site.baseurl }}/assets/images/MFW3000.png)

This reveals clear patterns:

* Brackett and Bradley move closer together because they both use planetary romance vocabulary
* Philip K. Dick remains isolated (yet somewhat similar to Norton) because of his focus on war, machines, and control
* H.G. Wells is again an outlier because his vocabulary reflects earlier scientific concerns

These results argue that female authors do not cluster together because of gender. They cluster when they share similar themes or similar genres.

---

### The Value and Literacies of the Macro View

When we compare Stylo and TF-IDF, we see both similarities and differences.

Similarities:

* Some authors (like Wells) are outliers in both models
* Some authors (like Dick and Norton) are consistent in both

In simple terms:

* Stylo clusters by author
* TF-IDF clusters by theme

This leads to one of the most important insights in this assignment:
**style is individual, content is collective.**

This also explains cases where the methods disagree. For example:

* Brackett and Bradley are separated in Stylo but close in TF-IDF
* Kuttner is unstable in Stylo but more stable in TF-IDF

So one method captures personal writing habits, while the other captures shared genre language.

---

### Limits and Implications

Ted Underwood argues that distant reading can be risky since it reduces literature to numbers. While this is true to some extent, these models do not understand meaning. They only measure patterns. For example, TF-IDF can show that the word "fear" appears often, but it cannot understand the meaning or emotions that are held behind it.

However, this does not mean the method is useless, computational analysis provides a scale of observation "unavailable to close-readers" (Jockers). It shows patterns that humans cannot easily see simply by close reading. No reader can track thousands of word frequencies across 18 texts at once.

There are also clear limitations:

* Results depend heavily on parameters (especially MFW count)
* Stylo struggles with co-authorship
* TF-IDF can be too sensitive at low MFW levels

It's not all negatives though, these limitations are part of the analysis. They show that computational reading requires careful interpretation.

---

### Broader Insights and Thought Questions

This analysis changed how I think about science fiction. I expected all the texts to be similar, but they are actually very different in both style and theme.



## Conclusion

This project shows that Stylo and TF-IDF reveal two different sides of literature. Stylo shows that writing style is stable and tied to individual authors. TF-IDF shows that themes are shared and shaped by the genre.

When used correctly, these methods do not replace close reading, they expand on it. They allow us to see patterns across many texts at once and understand how a genre evolves over time.

Instead of reducing literature, distant reading makes its structure more visible. It has to work together alongside close-reading to reach it's full potential and help the reader go more in depth than before.

---

## Works Cited

Eder, Maciej. "Does Size Matter? Authorship Attribution, Small Samples, Big Problem." *Digital Scholarship in the Humanities*, vol. 30, no. 2, 2015, pp. 167-182.

Jockers, Matthew L. "On Distant Reading and Macroanalysis." *Matthew Jockers*, 1 July 2011.

Underwood, Ted. "The Risks of Distant Reading." *Distant Horizons: Digital Evidence and Literary Change*, University of Chicago Press, 2019, pp. 143-169.


**READY FOR GRADING**

