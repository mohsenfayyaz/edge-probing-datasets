# Semantic Proto-Roles v2

This archive contains data from the experiments described in Section 4 of the following paper.

White, A. S., D. Reisinger, K. Sakaguchi, T. Vieira, S. Zhang, R. Rudinger, K. Rawlins, & B. Van Durme. 2016. [Universal decompositional semantics on universal dependencies](http://aclweb.org/anthology/D/D16/D16-1177.pdf). In *Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing*, pages 1713–1723, Austin, Texas, November 1-5, 2016.

If you make use of this data set in a presentation or publication, we ask that you please cite this paper.

There are two files: `protoroles_eng_ud1.2_11082016.tsv` and `adjunct_eng_ud1.2_11082016.tsv`. The first contains the core dataset, which includes annotations of only NP arguments. The second contains an auxiliary dataset aimed at ascertaining whether particular PP are arguments or adjuncts. 

Both files have the same set of columns, though some of the set of values found in some columns differs between the two. The most important difference between the two datasets lies in the `Property` column.

The column descriptions and values for `protoroles_eng_ud1.2_11082016.tsv` can be found below. 

| Column            | Description       | Values            |
|-------------------|-------------------|-------------------|
| Dataset           | Dataset described in paper | `bulkfiltered`, `bulkunfiltered`, `pilot1`, `pilot2`, `pilot3`, `pilot4`, `pilot5` |
| Is.Pilot          | Whether the annotation was part of a pilot (True) or bulk HIT (False) | `True`, `False` |
| Passes.Filters    | Whether the sentence passes Reisinger et al.'s filters as described in the paper | `True`, `False` |
| Protocol          | The protocol used to annotate the data | `spr1`, `spr2`, `spr2.1` |
| Split             | The train-dev-test split from the English Web Treebank | `train`, `dev`, `test` |
| Annotator.ID      | The annotator that provided the response | `0`, ..., `93` |
| Sentence.ID       | The file and sentence number of the sentence in the English Universal Dependencies v1.2 treebank with the format `LANGUAGE-CORPUS-SPLIT.ANNOTATION SENTNUM` |  |
| Pred.Token        | The index of the predicate in the white-spaced tokenized sentence | `0`, ..., `135` |
| Pred.Lemma        | The predicate lemma | see data |
| Gram.Func         | The grammatical function of the argument obtained from the UD dependency label | `nsubj`, `nsubjpass`, `dobj`, `iobj` |
| Arg.Phrase        | The argument phrase |  |
| Arg.Tokens.Begin  | The index in the white-spaced tokenized sentence at which the argument phrase begins | `0`, ..., `134` |
| Arg.Tokens.End    | The index in the white-spaced tokenized sentence at which the argument phrase ends | `0`, ..., `134` |
| Property          | The proto-role property being annotated | `awareness`, `change_of_location`, `change_of_possession`, `change_of_state`, `change_of_state_continuous`, `existed_after`, `existed_before`, `existed_during`, `instigation`, `partitive`, `sentient`, `volition`, `was_for_benefit`, `was_used`, `changes_possession`, `exists_as_physical`, `location_of_event`, `makes_physical_contact`, `predicate_changed_argument`, `stationary` |
| Response          | The 5-point Likert scale annotation of the property (Note: an extremely rare javascript error produced null responses for 7 rows) | `1`, `2`, `3`, `4`, `5`, `nan` |
| Applicable        | Whether the property is applicable in principle to the argument in question | `yes`, `no` |
| Sent.Grammatical  | Whether the sentence being annotated is grammatically acceptable; not applicable for pilots 1 and 2 (Note: a javascript coding error in the HIT collapses `2`, `3`, and `4` responses to `2` in the `bulkfiltered` and `pilot3` datasets) | `1`, `2`, `3`, `4`, `5`, `nan` |

The column descriptions and values for `adjunct_eng_ud1.2_11082016.tsv` can be found below. Some columns contain a uniform value. We retain these columns to make it easy to concatenate the two files easily.

| Column            | Description       | Values            |
|-------------------|-------------------|-------------------|
| Dataset           | Dataset described in paper | `adjunct` |
| Is.Pilot          | Whether the annotation was part of a pilot (True) or bulk HIT (False) | `False` |
| Passes.Filters    | Whether the sentence passes Reisinger et al.'s filters as described in the paper | `False` |
| Protocol          | The protocol used to annotate the data | `adjunct` |
| Split             | The train-dev-test split from the English Web Treebank | `train`, `dev`, `test` |
| Annotator.ID      | The annotator that provided the response | `0`, ..., `93` |
| Sentence.ID       | The file and sentence number of the sentence in the English Universal Dependencies v1.2 treebank with the format `LANGUAGE-CORPUS-SPLIT.ANNOTATION SENTNUM` |  |
| Pred.Token        | The index of the predicate in the white-spaced tokenized sentence | `0`, ..., `66` |
| Pred.Lemma        | The predicate lemma | see data |
| Gram.Func         | The grammatical function of the argument obtained from the UD dependency label | `nmod` |
| Arg.Phrase        | The argument phrase | see data |
| Arg.Tokens.Begin  | The index in the white-spaced tokenized sentence at which the argument phrase begins | `0`, ..., `68` |
| Arg.Tokens.End    | The index in the white-spaced tokenized sentence at which the argument phrase ends | `0`, ..., `97` |
| Property          | The proto-role property being annotated | `location`, `manner`, `purpose`, `time` |
| Response          | The 5-point Likert scale annotation of the property | `1`, `2`, `3`, `4`, `5` |
| Applicable        | Whether the property is applicable in principle to the argument in question | `yes`, `no` |
| Sent.Grammatical  | Whether the sentence being annotated is grammatically acceptable; not applicable for pilots 1 and 2 (Note: the grammatical acceptability judgment was not set to required, and so some annotators did not give a response) | `1`, `2`, `3`, `4`, `5`, `nan` |
