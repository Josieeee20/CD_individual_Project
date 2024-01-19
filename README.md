# CD_individual_Project
This repository is crated for the final individual project of collecting data
# Corpus Documentation

## 1. The Corpus 
The corpus is extracted from the press releases on the Chinese Ministry of Foreign Affairs website in December 2023, with spokespersons Mao Ning and Wang Wenbin.

## 2. Target Audience and Intended Use
The primary target audience for this corpus is political enthusiasts interested in Chinese politics. The press releases mainly cover the responses of the Ministry of Foreign Affairs to international affairs in December, providing readers with valuable insights into China's political perspectives and positions.

## 3. Text Selection Criteria
The text content primarily consists of press releases from the Ministry of Foreign Affairs in December 2023. Prior to text analysis, the text underwent cleaning, removing unnecessary punctuation and characters, retaining only the main content of the articles. Simultaneously, the text is saved in the format of "txt_01", following the structure of txt_01, and metafile indicates the corresponding titles for each text. These preparations facilitate a more effective analysis of the text using spaCy.

## 4. Data Collection Process
Utilizing the functionalities of `re`, `os`, `csv`, `BeautifulSoup`, and `requests` for data retrieval.
- requests: Used for making HTTP requests to fetch data from web servers. BeautifulSoup: A library for parsing HTML and XML documents, commonly used in web scraping.
- csv: A built-in module for reading and writing CSV files, simplifying handling tabular data. urllib.parse: Provides functions for parsing and manipulating URLs.
- re: The regular expressions module for powerful string pattern matching and manipulation.
- os: Interacts with the operating system, often used for file and directory manipulation. unicodedata: Provides access to the Unicode Character Database, useful for working with Unicode characters and strings.

## 5. Cleaning and Preprocessing Steps
Performed initial cleaning on the collected documents, which involved tasks such as removing whitespace, standardizing text format, handling missing data, and addressing case sensitivity.

## 6. Annotations and Tools
we use spacy to annotate the text: coarse-grained tagging, which predicts the simple universal part-of-speech of each token (e.g., noun, verb), and detailed tagging, which uses a more fine-grained set of part-of-speech tags (e.g., 3rd person singular present verb). The tags are determined by the English language model used, and the example mentions the usage of the small English model.

To extract part-of-speech tags, the text suggests creating a function that can extract both coarse- and fine-grained part-of-speech for each token in a spaCy Doc object. The function is expected to utilize token.pos_ for coarse-grained tagging and token.tag_ for fine-grained tagging. The recommendation is to apply this function to each Doc object in a DataFrame containing text data.

## 7. Format of Files in the Corpus
we firstly use txt format to collect all the text then use csv format to analysis it.
| Column            | Description                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------|
| Filename    | The name of the original text file in the data folder, serving as a unique identifier for each document.                                        |
| Title  | Column containing titles associated with the texts, providing additional context or information about the content of each document.  |
| Date | Stores the date of each txt file
|Spokesman| Stores the spokesman of the speech
| Doc            | Stores the original text exactly as it appears in the text file, preserving the raw, unprocessed content of each document.                             |
| Text  |  Column containing preprocessed text of each document, including cleaned or modified versions of the original text.                      |
| Tokens         | Stores the tokenized text of each document, representing individual units such as words or punctuation after tokenization.                           |
| Lemmas         | Stores the lemmatized text of each document, containing base or dictionary forms of words obtained through lemmatization.                            |
| Parts-of-speech | Contains information about the parts of speech of all the tokens in each document, including either coarse-grained (universal) or fine-grained part-of-speech tags. |
