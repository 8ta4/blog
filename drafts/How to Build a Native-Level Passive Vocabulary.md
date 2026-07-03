If you want to understand English at a native level, you don't need to memorize every obscure word in the dictionary. You just need a way to target the vocabulary that most native speakers know.

That's where the [`wiktionary.tsv`](https://github.com/8ta4/prevalence-data/raw/c79fd1ee936a5b05ad4fecc99b5232d2b9f14b4d/wiktionary.tsv) dataset comes into play. The file was built by running a large language model on more than a million Wiktionary entries.

Check out a sample of the `wiktionary.tsv` data:

| entry         | prevalence        | lemma | space |
| ---           | ---               | ---   | ---   |
| 1             | 100.0             | true  | false |
| stop sign     | 99.66468861406302 | true  | true  |
| I love you    | 99.37727885468848 | true  | true  |
| potatoes      | 99.27349199713656 | false | false |
| single parent | 97.50911541875394 | true  | true  |
| humvee        | 83.65356993557272 | true  | false |
| heterodontid  | 4.700793319016159 | true  | false |

This dataset helps fill the gaps left by language textbooks and frequency lists.

- Textbooks usually skip brand names. You don't normally hear about brand names such as Kleenex in English textbooks. But pretty much every American knows them.

- Frequency lists tend to underrepresent phrasal verbs. Phrases that break up to include objects, like "took him for a ride", can get missed.

The columns in `wiktionary.tsv` are set up to make it easy for you to customize your lists.

The `lemma` column shows whether an entry is a lemma in Wiktionary. By filtering where `lemma` is true, you can focus on low-hanging roots of the language.

The `space` column spots entries with spaces so you can tell single words apart from multi-word phrases. You can use this to study single vocabulary words and multi-word phrases in separate sessions.

The code used to build this dataset is linked here.

Feel free to share any feedback.
