# LitDialogSilver
This repository contains the "silver data" for automatic speech identification in Swedish literature described in:

Sara Stymne. 2024. [Direct Speech Identification in Swedish Literature and an Exploration of Training Data Type, Typographical Markers, and Evaluation Granularity](https://aclanthology.org/2024.latechclfl-1.25/). In *Proceedings of the 8th Joint SIGHUM Workshop on Computational Linguistics for Cultural Heritage, Social Sciences, Humanities and Literature (LaTeCH-CLfL 2024)*, pages 253–263, St. Julians, Malta. Association for Computational Linguistics.

The data contains automatically annotated speech segments and speech tags from 88 Swedish novels and collections of short stories where quotation marks are used for speech marking, from the period: 1821–1931. The following heuristics are used:
* Speech segments:
  * Text between quotation marks
* Speech tags:
  * If the first speech segment is preceded by a colon (either within the paragraph or in the previous paragraph), we search for the preceding punctuation mark or the start of a line and mark the tokens in this stretch as a speech tag.
  * If the first speech segment of a line is not followed by a period, we mark any tokens up until a sentence-final punctuation mark or another quotation mark as a speech tag.
 
The works are filtered to remove works that also use dashes for speech marking, that have very little text marked as speech (less than 20% of tokens), or has few speech tags compared to speech segments (less than 1 speech tag per 5 speech segments).

All texts are from [Litteraturbanken](https://litteraturbanken.se/)https://litteraturbanken.se/, available as XML-files produced from proofread OCR of the original works. 

We release this data under the Creative Commons CC BY-NC-SA license.
