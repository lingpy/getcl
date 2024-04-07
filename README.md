# `getcl`: Mapping Lexical Data from CLDF Dictionaries to Wordlists

`getcl` offers the code for mapping lexical data from a CLDF dictionary to a wordlist as described in the following paper:

> Blum, Frederic and Englisch, Johannes and Hermida Rodriguez, Alba and van Gijn, Rik and List, Johann-Mattis (2024). To be published in the Proceedings of the 2nd Meeting of the ELRA/ISCA Special Interest Group on Under-Resourced Languages.

To install the tool, just clone this repository and then type:

```
pip install -e .
```

This will provide a new command `conceptlist` that you can use to map concepts in the sense descriptions of a dictionary to Concepticon.

To test the package, you can just run the following code:

```
$ git clone https://github.com/dictionaria/kalamang.git
$ conceptlist --data kalamang/cldf/cldf-metadata.json --conceptlist Swadesh-1955-100 --output kalamang.tsv | wc -l
```
The output should be 197. This means that 196 matches for the 100 concepts of Swadesh's concept list could be identified. To get a useful concept list of these matches (that contain duplicates and potential errors), you would not look at the file `kalamang.tsv` and modify it manually to arrive at a Swadesh list derived from the dictionary.
