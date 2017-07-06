# Text Regenerator

Automatically generates variations of texts through synonym matching with WordNet. This can be imported and used as a library, or run with a single command in Terminal / Command Prompt. More advanced NLP features plan to be added, like expanding to a more advanced thesaurus, analyzing sentence syntax for parts of speech, and adding a weighting system to the synonym matching. Included in the Emoter library.


### Prerequisites

Tested on Python 2.7. Requires NLTK library and corpus texts. Make your virtual environment, and install NLTK and its corpus.

```
pip install nltk
python
import nltk
nltk.download()
```


## Running Text Regenerator as a script

Run the Python script with the string you wish to generate variations of as the first argument. The second argument is optional, and takes another string, parsing what should be a list of words separated by commas and spaces, and also is enclosed in quotes. The second argument adds stop (ignored) words to the default list.

For example:
```
python text_regenerator.py "i really want to make a bunch of illiterate versions of this sentence" "i, really, to, a, of, sentence"
```
gives you..
```
Final list of stop words: ['i', 'really', 'to', 'a', 'of', 'sentence', 'the', 'in', 'at', 'long', 'does']

	Now generating variations of: "i really want to make a bunch of illiterate versions of this sentence"..
		i really want to make a bunch of illiterate versions of this sentence
		i really privation to brand a clump of illiterate person version of this sentence
		i really deprivation to shuffle a cluster of nonreader variant of this sentence
		i really neediness to shuffling a clustering of ignorant variation of this sentence
		i really lack to do a crowd of ignorant edition of this sentence
		i really deficiency to get a crew of ignorant adaptation of this sentence
		i really need to create a gang of ignorant translation of this sentence
		i really wish to induce a lot of ignorant interlingual rendition of this sentence
		i really wishing to stimulate a caboodle of ignorant rendering of this sentence
		i really desire to cause a bunch together of ignorant interpretation of this sentence
```

### Using TRGNR as library

TRGNR has a basic API to return a list of the string variations.

```
from TextRegenerator import trgnr
trgnr.addStopWords("add, more, words, if, it, says, stupid, things")
trgnr.generateStrVariations("should i add more words if your program is too stupid to understand the things i say"
```
returns
```
['should i add more words if your program is too stupid to understand the things i say', 'should iodine add more words if your plan be excessively stupid to realize the things iodine state', 'should iodin add more words if your programme exist overly stupid to realise the things iodin tell', 'should I add more words if your broadcast equal to_a_fault stupid to see the things I allege', 'should atomic_number_53 add more words if your platform constitute besides stupid to read the things atomic_number_53 aver', 'should one add more words if your political_platform represent also stupid to interpret the things one suppose', 'should 1 add more words if your political_program make_up likewise stupid to translate the things 1 read', 'should ace add more words if your course_of_study comprise as_well stupid to infer the things ace order', 'should single add more words if your curriculum follow as_well stupid to sympathize the things single enjoin', 'should unity add more words if your syllabus embody as_well stupid to sympathise the things unity pronounce', 'should ane add more words if your computer_program personify as_well stupid to empathize the things ane articulate', 'should ane add more words if your computer_programme live as_well stupid to empathise the things ane enounce', 'should ane add more words if your computer_programme cost as_well stupid to empathise the things ane sound_out', 'should ane add more words if your computer_programme cost as_well stupid to empathise the things ane enunciate']
```


## Built With

* WordNet
* NLTK

## Authors

* **Johnny Dunn** - *Initial work* - [jddunn](https://github.com/jddunn)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Synonym matching code (WordNet calls) from [nickloewen](https://github.com/nickloewen/thesaurus)
