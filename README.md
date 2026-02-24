**Quantifying Harmonic Surprise**

This little project effectively explores how typical of Beethoven each of his sonatas are by measuring the cross entropy/surprise in each sonata against his entire entire sonata output. We also plotted the changing levels of entropy across the work so see where the most dramatic moments are. We only investigated the harmonic component of the work. 

**Method/Discussion**

- The DCML files were parsed for their chord data (Roman Numerals)

- We then created probability tables for each of the chord transitions across this corpus for both consecutive chords and 4-grams.

- From this, we calculated cross entropy for each movement to broadly compare how unexpected the harmonic progressions are within it.

  Shannon entropy formula: $$h(x) = -\log_2(P(x))$$

 <img width="800" height="600" alt="average_entropy_by_sonata_first_movements" src="https://github.com/user-attachments/assets/aed914bd-8f0e-4a02-90bb-55f06025c30e" />

It is nice to see Beethoven's Op.49, No.2 as (equal) lowest on the entropy levels as this is widely considered his most simple sonata. Important to consider that standard western classical harmony will make up a large part of all the sonatas, so this exploration could be improved by adding cut-offs and/or weightings to downplay standard harmonic progressions.

 Then, for each movement, we also explored the changing information dynamics of the movement using a sliding window of chords. 

<img width="800" height="600" alt="cross_entropy_Op057(Appassionata)_movement_1" src="https://github.com/user-attachments/assets/25d6b6da-8617-4144-be4b-8701ac7eabd9" />

The Appassionata 1st movement is a particularly nice example as you can clearly see a birotational form in the movement through the repeated entropy pattern. It is insightful to get a quantification of tension and release across the work as this can inform thinking on musical structure and interpretations (particularly if information content varies across parameters, which we didn't have time to explore).
