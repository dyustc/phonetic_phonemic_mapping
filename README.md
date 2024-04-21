# phonetic_phonemic_mapping

## Introduction
This repo is intended for the two popular Enghlish phonetic symbol system, one is DJ, more of British style, the other is K.K., the American style, to map to the widely used CMU phonemic set in the data annotation of ASR tasks or pronunciation tasks. 

Especially, given the fact that L2 learners often face 2 phonetic systems in the learning process, while almost every phonemic dataset is only in CMU, ARPA styles, or their derivatives, all in American styles, some adjustments is made to the final criterion for what should be considered correct with their actual pronunciation. 

We made this adjustments according to the practical education scene in elementary, middle, high school in China.

## Explanation
This mapping is focused on those words which have similar but different phonetic symbols in UK and US systems, both vowels and consonants are being compared, but stress and length and other suprasegmental symbols aren't the focus here, whereas all of them should make up the full syllable annotation of a word.

DJ phonetic Symbol is used as the basis for the comparsion. Here is the explanation for each column.
- DJ Phonetic Symbol: 44 symbols in total, adding four extras, that is 'ts', 'tr', 'dr', 'dz' also considered to be a constant phonetic symbol, so 48 in a wider definition.
- K.K. phonetic symbol: 41 symbols in total, there is a mapping to DJ symbols in each circumstance, and we combine 2 symbols to form a corresponding symbol if there is no single mapping, e.g, [ɪ] + [r] to ɪə
- UK-style annotation in Cambridge/LONGMAN Dictionary : Almost same as DJ Phonetic Symbol, except that a length symbol is appended to certain vowels.
- US-style annotation in Cambridge/LONGMAN Dictionary : the corresponding annotation from the dictionary to UK-style, mostly they are the same as K.K. phonetic symbol, except for the r syllable appended to certain vowels or printing convienience,  e.g, [ɑ] to ɑːr, [ɚ] to ər.
- Examples: example words
- CMU Phoneme Set: 39 in total, not counting varia due to lexical stress. It's a mapping to US-style annotation, and we combine 2 phonemes to form a corresponding symbol if there is no single mapping, e.g, IH + R to [ɪ] + [r] to ɪə.
- CMU Phoneme Set + 2 Extra: 41 in total, counting AH0 and ER0, given the fact that these 2 vowels sound a lot different with or without stress symbol.
- Adjusted Phoneme Set regardding to DJ Phonetic Symbol: this column takes actual use of syllables in education system into consideration,  given the total negelect of British syllables and accent in multiple datasets such as Timit, LibriSpeech, while British accent and annotation is mixed a lot in L2 Learners' learning.

## Something more

- For those words which have different syllable annotations in UK or US style, such as tomato, garage, we don't add them to this list, because their difference lies in word level but not a single phonetic level.
- For those words which have multiple pronunciations in either system, e.g, suspect, we also remove them to simplify the mapping.
- For those words whose actual pronunciation don't strictly follow the syllable annotation, like in US accent, a lot short vowels are pronunced as ə, like good, but, we don't add these rules in this list.


## Reference
https://en.wikipedia.org/wiki/CMU_Pronouncing_Dictionary

https://en-yinbiao.xiao84.com/2014/1277.html

https://en-yinbiao.xiao84.com/2014/16141.html
