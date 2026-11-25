# Japanese–English sentence pairs from Tatoeba, RealPersonaChat, JMRD and JMultiWOZ

A selection of Japanese sentences with English translations, published free of charge and without DRM: sentences
from Tatoeba, and lines from three corpora of Japanese text chats: RealPersonaChat, JMRD and JMultiWOZ.

- Sources: Tatoeba (https://tatoeba.org), sentences written by the Tatoeba contributors named in each row; each
  sentence is at `https://tatoeba.org/en/sentences/show/<id>`. RealPersonaChat
  (https://github.com/nu-dialogue/real-persona-chat), JMRD (https://github.com/ku-nlp/JMRD) and JMultiWOZ
  (https://github.com/nu-dialogue/jmultiwoz), see their files below.
- Licences: **CC BY 2.0 FR** (https://creativecommons.org/licenses/by/2.0/fr/) for the Tatoeba files, **CC BY-SA 4.0**
  (https://creativecommons.org/licenses/by-sa/4.0/) for the three chat files; see `LICENSE.md`.
- Format: UTF-8, tab-separated, one sentence per line, with a header line.

## `tatoeba-subset.tsv`

The selected Tatoeba pairs. Columns:
`ja_id  ja_text  ja_furigana  ja_author  en_id  en_text  en_author  use  changes`.

- `use` is `practice` for a sentence of the selection, and `original of a rewrite` for a sentence that one in
  `tatoeba-adapted.tsv` was rewritten from. A sentence that is both has a line for each.
- `ja_furigana` is the sentence with readings above the kanji, written `{漢字|かんじ}`. They come from Tatoeba's
  transcriptions. It is empty for the original of a rewrite.
- `changes` names what was changed in the pair: `reading corrected` (a reading in `ja_furigana` differs from
  Tatoeba's transcription) or `new English` (the English was newly written, because none of Tatoeba's translations
  fitted; such a line has no `en_id` and no `en_author`). The Japanese text is never changed.
- Otherwise, an empty author means the sentence has no owner on Tatoeba.

## `tatoeba-adapted.tsv`

Sentences rewritten from Tatoeba sentences. Columns: `ja_text  ja_furigana  en_text  from_ja_id  from_en_id`.

In a rewrite, one verb or adjective of the Tatoeba sentence was put into another form and the rest of the sentence
adjusted to fit, and the English was newly written. `from_ja_id` and `from_en_id` are the Tatoeba sentence and
translation it started from, which are in `tatoeba-subset.tsv` with their authors.

## `realpersonachat-subset.tsv`

Lines from RealPersonaChat (https://github.com/nu-dialogue/real-persona-chat, v1.0.0), a corpus of Japanese text
chats by Sanae Yamashita, Koji Inoue, Ao Guo, Shota Mochizuki, Tatsuya Kawahara and Ryuichiro Higashinaka, under
**CC BY-SA 4.0** (https://creativecommons.org/licenses/by-sa/4.0/). Columns:
`ja_text  ja_furigana  en_text  dialogue_id  utterance_id  changes`.

- Each line is one sentence of the utterance `utterance_id` in `real_persona_chat/dialogues/<dialogue_id>.json`
  (the id padded to five digits).
- `en_text` and `ja_furigana` were newly written for this selection. They are under CC BY-SA 4.0 too.
- `changes` is `final 。 added` (or `final ？ added`) where the chat line had no final mark; the Japanese text is
  otherwise unchanged.

## `jmrd-subset.tsv` and `jmultiwoz-subset.tsv`

Lines from JMRD (https://github.com/ku-nlp/JMRD), the Japanese Movie Recommendation Dialogue dataset by Takashi
Kodama, Ribeka Tanaka and Sadao Kurohashi, and from JMultiWOZ (https://github.com/nu-dialogue/jmultiwoz, v1.0), a
corpus of travel-desk dialogues by Atsumoto Ohashi, Ryu Hirai, Shinya Iizuka and Ryuichiro Higashinaka, both under
**CC BY-SA 4.0**. Columns as in `realpersonachat-subset.tsv`:
`ja_text  ja_furigana  en_text  dialogue_id  utterance_id  changes`.

- JMRD: `dialogue_id` is a dialogue's `dialog_id` in `data/{train,valid,test}.json`, `utterance_id` the number after
  the underscore in its utterance's `utterance_id`. Only the crowdworkers' own words are in it: no sentence that
  shares a stretch of twelve characters with the plot summaries and reviews the dialogue came with.
- JMultiWOZ: `dialogue_id` is a dialogue's `dialogue_id` in `dialogues.json`, `utterance_id` its turn's `turn_id`.
- `en_text`, `ja_furigana` and `changes` as in `realpersonachat-subset.tsv`.

## Notes

**Your rights.** Whoever gets these sentences, from here or from an app that uses them, has the full rights of
CC BY 2.0 FR (the Tatoeba files) or CC BY-SA 4.0 (the RealPersonaChat, JMRD and JMultiWOZ files). No app's terms of use or "all rights reserved" notice restricts them.

**What was changed.** The sentences were selected, a few readings corrected and some English translations newly
written (the `changes` column), and some sentences rewritten (`tatoeba-adapted.tsv`). The Japanese texts in
`tatoeba-subset.tsv` are unchanged. The rewrites and the new translations are under the same licence as the
originals.

**No endorsement.** This dataset is not affiliated with, sponsored or endorsed by Tatoeba or its contributors, or by
the authors of RealPersonaChat, JMRD or JMultiWOZ.
