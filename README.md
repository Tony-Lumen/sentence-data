# Japanese–English sentence pairs from Tatoeba

A selection of Japanese sentences from Tatoeba with their English translations, published free of charge and
without DRM.

- Source: Tatoeba (https://tatoeba.org), sentences written by the Tatoeba contributors named in each row. Each
  sentence is at `https://tatoeba.org/en/sentences/show/<id>`.
- Licence: **CC BY 2.0 FR** (https://creativecommons.org/licenses/by/2.0/fr/), see `LICENSE.md`.
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

## Notes

**Your rights.** Whoever gets these sentences, from here or from an app that uses them, has the full rights of
CC BY 2.0 FR. No app's terms of use or "all rights reserved" notice restricts them.

**What was changed.** The sentences were selected, a few readings corrected and some English translations newly
written (the `changes` column), and some sentences rewritten (`tatoeba-adapted.tsv`). The Japanese texts in
`tatoeba-subset.tsv` are unchanged. The rewrites and the new translations are under the same licence as the
originals.

**No endorsement.** This dataset is not affiliated with, sponsored or endorsed by Tatoeba or its contributors.
